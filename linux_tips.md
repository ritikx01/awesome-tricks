1. Make QR code of your clipboard
	`xclip -o -s c | qrencode -o - | feh --force-aliasing -ZF -`

2. Use xclip to copy from terminal
	`xclip file_name`		<Only paste with middle mouse button>
	`xclip -sel clip file_name`	<Paste with Ctrl + V>3. Make touchpad, touch to click work (Arch)
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

7. Execute a previous command with sudo: `!!`.

8. In zsh, run previous command again `r`.

9. Suppress python requests, insecure ssl warning. `export PYTHONWARNINGS="ignore:Unverified HTTPS request"`

10. Install a ca-certificate (.crt) system wide. 
```bash
sudo cp certificate.crt /usr/local/share/ca-certificates
sudo update-ca-certificates
```
To istall a .pem or .cer format certificate we need to convert it to .crt format.
```bash
# To convert pem
openssl x509 -in foo.pem -inform PEM -out foo.crt
# To convert cer
openssl x509 -inform DER -in foo.cer -out foo.crt
```
