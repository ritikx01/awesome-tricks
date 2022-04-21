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
