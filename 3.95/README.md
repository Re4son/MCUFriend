# Drivers for the mcufriend 3.95 inch tftlcd display for Raspberry Pi

### Installation:

sudo wget -O /etc/modprobe.d/fbtft_device.conf https://raw.githubusercontent.com/Re4son/MCUFriend/master/3.95/fbtft_device.conf
sudo wget -O /etc/modprobe.d/flexfb.conf https://raw.githubusercontent.com/Re4son/MCUFriend/master/3.95/flexfb.conf
sudo wget -O /etc/modules https://github.com/Re4son/MCUFriend/raw/master/3.95/modules
sudo wget -O /usr/share/X11/xorg.conf.d/99-fbturbo.conf https://github.com/Re4son/MCUFriend/raw/master/3.95/99-fbturbo.conf

sed -i 's/rootwait/rootwait fbcon=map:10 fbcon=font:VGA8x8 fbcon=rotate:3/g' "/boot/cmdline.txt"
