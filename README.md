## Preview
---
![[LegionThemePreviev.png]]

## Installing
---
### Ubuntu
copy the extracted theme to `/boot/grub/themes`
```
sudo cp CyberRe\ 1.0.0/CyberRe /boot/grub/themes/ -r

sudo nano /etc/default/grub
```

At the bottom of the file, paste the following, updating the path to the theme.txt file
`GRUB_THEME=/boot/grub/themes/Legion-grub-theme/theme.txt`

Press CTRL+O, Enter, CTRL+X to write the changes

Update grub
```
sudo update-grub
```
If everything is setup correctly, a line that reads Found theme: `/boot/grub/themes/Legion-grub-theme/theme.txt` should show in the update-grub output

Reboot to see the new theme in action
```
sudo reboot
```
---
### Linux Mint
Easy way to install theme:
```
sudo nano /etc/default/grub.d/90_custom.cfg
```
add the lines:
```
GRUB_TIMEOUT="5"
GRUB_TIMEOUT_STYLE="menu"
```

```
apt install --reinstall -o Dpkg::Options::="--force-confmiss" grub2-theme-mint
```
Then replace theme folder in /boot/grub/themes
```
sudo open /boot/grub/themes
```
Update grub
```
sudo update-grub
```
Reboot
```
sudo reboot
```

 *You may also install it via Ubuntu way*
 
---
## Removing the Theme

```
cd /boot/grub/themes/
```
```
ls
```
```
sudo rm Legion-grub-theme -r
```
```
sudo update-grub
```
```
reboot
```