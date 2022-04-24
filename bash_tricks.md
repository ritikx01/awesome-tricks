1. Make QR code of your clipboard
	`xclip -o -s c | qrencode -o - | feh --force-aliasing -ZF -`

2. Use xclip to copy from terminal
	`xclip file_name`		<Only paste with middle mouse button>
	`xclip -sel clip file_name`	<Paste with Ctrl + V>

3. Make touchpad, touch to click work (Arch)
```bash
cd /etc/X11/xorg.conf.d/
wget https://gist.githubusercontent.com/ritikx01/c8ca6095a8d8e09008fb7fdbae7b0438/raw/397fd9ed6d901e5c6edfd81ddeeb0dfd31f41fae/99-synaptics-overrides.conf
```

4. Execute a previous command again:
    Get position of command from history.
    Command: !\<number\>
```bash
history
1 echo "Hello people"
2 ls
3 touch .hushlogin
!1			// We want to execute the command at position 1
Hello people		// Command gets executed
```

5. Add Date and Time to history. (Even previous ones)
`HISTTIMEFORMAT="  %Y-%m-%d %T  "`
Make it persistent:
```bash
echo 'HISTTIMEFORMAT="  %Y-%m-%d %T  "' >> ~/.bashrc
source ~/.bashrc
```

6. Hide a command from history: Add a space before command.
