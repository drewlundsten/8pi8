# 8pi8
 Python on Pi on 8x8 ASIC EVB

Config your Pi:
1) Install Raspbian or other distro. Enable SSH, VNC; set new password and hostname.

2) Install pigpio
sudo apt-get install pigpio python3-pigpio
sudo pigpiod

3) Start pigpiod at startup:
sudo systemctl start pigpiod