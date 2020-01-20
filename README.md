# i3gaps-ubuntu-19.10

These are the steps I used to make i3 gaps work on ubuntu 19.10. I started with the instructions from [dabroder](https://gist.github.com/dabroder/813a941218bdb164fb4c178d464d5c23) and fiddled them for the newer ubuntu version:

```
sudo apt install -y libxcb1-dev libxcb-keysyms1-dev libpango1.0-dev libxcb-util0
-dev libxcb-icccm4-dev libyajl-dev libstartup-notification0-dev libxcb-randr0-dev libev
-dev libxcb-cursor-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommo
n-x11-dev autoconf libxcb-xrm0 libxcb-xrm-dev automake xcb xcb-xkb xcb-xinerama xcb-randr xcb-shape libxcb-shape0-dev i3status suckless-tools

cd /tmp
git clone https://www.github.com/Airblader/i3 i3-gaps
cd i3-gaps

./configure --prefix=/usr --sysconfdir=/etc --disable-sanitizers
cd x86_64-pc-linux-gnu
make -j8
sudo make install
```

You need the folowing, but you can adjust to taste, in your ~/.config/i3/config: 
```
gaps inner 15
gaps outer 15
for_window [class=".*"] border pixel 0
bindsym Mod4+l exec /usr/bin/gnome-screensaver-command -l
```

Although not necessary, I also set my background to grey with: 
```
cp /etc/X11/Xsession ~/.xinitrc
echo 'xsetroot -solid "#808080"' >> ~/.xinitrc
```
