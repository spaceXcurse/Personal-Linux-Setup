## ANYTHING
This repo was supposed to be for arch-based systems.  Anyways, it is my grand (but not final) solution to resolve my suffering of having to manually type commands to anything needed and important in my arch-based setup (reason is mainly for Archcraft). That's all. Forget the damn title.

## set(TF)up
### FOR STARTERS
* Update
```
sudo pacman -Syu && yay -Syu
```
* To use fonts, put in .fonts
```
fc-cache -f -v
```
* For firefox pinch-to-zoom
```
sudo nano /etc/security/pam_env.conf
MOZ_USE_XINPUT2=1
MOZ_USE_XINPUT2 DEFAULT=1
```
* For inverted touchpad scrolling
```
sudo nano /usr/share/X11/xorg.conf.d/40-libinput.conf
```
```
Section "InputClass"
   Identifier "mytouchpad"
   Driver "libinput"
   MatchIsTouchpad "on"
   NaturalScrolling "true"
EndSection
```
* Brightness Settings (Use program Power Manager)
  * (openbox) Change `brightness  --inc` to `xbacklight -inc 2' and 'xbacklight -dec 2'
  * (BSPWM) Put # on first row of `brightness`
* To watch pretty much anything, don't forget to change to `glx`from `xrender` in `.config/picom.conf`
* Grub bootloader themes para sheeeeeeeesh
```
git clone https://github.com/ChrisTitusTech/Top-5-Bootloader-Themes
cd Top-5-Bootloader-Themes
sudo ./install.sh
```
### PROGRAMS & SH8T
* Dew it
```
sudo pacman -S flatpak
yay -S discord spotify thunderbird qbittorrent vlc microsoft-edge-stable auto-cpufreq
sudo pacman -S noto-fonts-emoji noto-fonts-cjk
```
* How-to autostart
  * (openbox) put program name then & i.e discord &
### IT'S GAMING TIME MGA BROSKII
* Enable multilib
```
/etc/pacman.conf
--------------------------------------------------------------------------------------
[multilib]
Include = /etc/pacman.d/mirrorlist
```
* Install latest GPU driver (Intel)
```
sudo pacman -S --needed lib32-mesa vulkan-intel lib32-vulkan-intel vulkan-icd-loader lib32-vulkan-icd-loader
```
* Update then install wine
```
sudo pacman -Syu
sudo pacman -S --needed wine-staging giflib lib32-giflib libpng lib32-libpng libldap lib32-libldap gnutls lib32-gnutls \
mpg123 lib32-mpg123 openal lib32-openal v4l-utils lib32-v4l-utils libpulse lib32-libpulse libgpg-error \
lib32-libgpg-error alsa-plugins lib32-alsa-plugins alsa-lib lib32-alsa-lib libjpeg-turbo lib32-libjpeg-turbo \
sqlite lib32-sqlite libxcomposite lib32-libxcomposite libxinerama lib32-libgcrypt libgcrypt lib32-libxinerama \
ncurses lib32-ncurses opencl-icd-loader lib32-opencl-icd-loader libxslt lib32-libxslt libva lib32-libva gtk3 \
lib32-gtk3 gst-plugins-base-libs lib32-gst-plugins-base-libs vulkan-icd-loader lib32-vulkan-icd-loader
```
* Ito lang kaya natin mga broskii (yung anime game)
```
yay -S an-anime-game-launcher-bin
```
