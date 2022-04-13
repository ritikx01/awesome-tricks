1. Make QR code of your clipboard
	`xclip -o -s c | qrencode -o - | feh --force-aliasing -ZF -`
2. Use xclip to copy from terminal
	`xclip file_name`		<Only paste with middle mouse button>
	`xclip -sel clip file_name`	<Paste with Ctrl + V>
