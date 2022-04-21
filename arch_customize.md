# Customise arch with blur effects and more (KDE)
## Apps used:
- kitty (Terminal emulator)
- picom (Composiitor)
- Sweet KDE (Theme)

## Setup Apps
### picom
1. Install picom
	1. Build manually from jonaburg fork `https://github.com/jonaburg/picom`
	2. Use paru (Arch) to install jonaburg fork
```bash
paru picom-jonaburg-git
```
2. Disable KDE compositor. ` Settings > Hardware > Display and Monitor > Compositor > Uncheck Enable on startup`
3. Get default picom config and modify it
```bash
mkdir ~/.config/picom
cp /etc/xdg/picom.conf.example ~/.config/picom
```
or get my config from my dotfiles repo
```bash
mkdir ~/.config/picom
cd ~/.config/picom
wget <link>
```
4. Set picom for autostart
```bash
cd ~/.config/autostart
wget <link>
```
- In picom config, check for opacity rules if some applications don't get the desired blur effect. Reduce the opacity or just comment out the application name from opacity rules.
