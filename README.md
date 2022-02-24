# 8pi8
Python on Pi on 8x8 ASIC EVB

Config your Pi:
1) Install Raspbian or other distro. Enable SSH, VNC; set new password and hostname.

2) Install pigpio
> sudo apt-get install pigpio python3-pigpio
> sudo pigpiod

3) Start pigpiod at startup:
> sudo systemctl start pigpiod

4) Clone this git
> sudo git clone https://github.com/drewlundsten/8pi8.git

5) Run in interactive python session
> python3 -i 8pi8/8pi8.py 

6) Useful Python command-line functions:
> swr(num, reg) # read switch <num, 0-7> register <reg, 0x00-0xff>
> sww(num, reg, dat) # write switch <num> register <reg> with data <dat, 0x00-0xff>
> swdump(num) # dump register map of switch <num>
> swmap(num, inport, outport) # update switch <num> with <inport, 0-7> mapped to <outport, 0-7>
> swsave('./path/to/filename.xtn') # store all switch registers in <filename>
> swload('./path/to/filename.xtn') # restore switch configuratoin from <filename>
