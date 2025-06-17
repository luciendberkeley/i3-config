# i3-config and instructions on setting up arch

## Abridged version is below but here are the videos I followed:
https://youtu.be/DbeL7ehxpZ0?si=HYXv5YTD35P8ehog
and
https://youtu.be/v-aFfLiUm9g?si=jqRGRQ6ZVVT-ziSp

For the arch setup, make sure to run:
```
pacman -Sy
pacman -S archlinux-keyring
pacman -S archinstall

archinstall
```

Make sure to use Xorg and lightdm

Using terminator for my terminal emulator
Startup with startx
When setting up arch, make sure to run once so the display size works:
```
sudo pacman -Syu virtualbox-guest-utils
sudo systemctl enable vboxservice
sudo systemctl start vboxservice
```

For getting i3, do this:

```
pacman -S i3
nano -w .xinitrc
// Add these lines inside:
setxkbmap us -variant colemak
exec i3

// Finally
sudo systemctl disable lightdm.service
reboot
```
