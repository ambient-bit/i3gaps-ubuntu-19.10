# i3gaps-ubuntu-19.10

These are the steps I used to make i3 gaps work on ubuntu 19.10. I started with the instructions from [dabroder](https://gist.github.com/dabroder/813a941218bdb164fb4c178d464d5c23) and fiddled them for the newer ubuntu version:

```
sudo apt install -y libxcb1-dev libxcb-keysyms1-dev libpango1.0-dev libxcb-util0
-dev libxcb-icccm4-dev libyajl-dev libstartup-notification0-dev libxcb-randr0-dev libev
-dev libxcb-cursor-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommo
n-x11-dev autoconf libxcb-xrm0 libxcb-xrm-dev automake

cd /tmp
git clone https://www.github.com/Airblader/i3 i3-gaps
```
