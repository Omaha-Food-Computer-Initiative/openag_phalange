# openag_phalange
Firmware for microcontrollers (e.g. Arduino Mega2560) to interface peripherals (sensors &amp; actuators) with a single board computer (e.g. Raspberry Pi 3).

# Install Instructions
1. *Clone repo:* git clone \<repo name\> 
2. *Configure git update:* git config --global alias.update '!git pull && git submodule update --init --recursive'
3. *Update repo:* git update
4. *Install platformio:* pip2 install -U platformio
5. *Connect arduino to rpi w/USB cable*
6. *Compile and upload:* pio run -t upload


# Update Submodule To Later Commit
1. git submodule init
2. git submodule update
3. cd \<submodule dir\>
4. git checkout master
5. git pull
6. cd \<mainmodule dir\>
7. git commit
8. git push

# Platformio Commands
*compile:* pio run

*compile & upload:* pio run -t upload

*serial monitor:* pio serialports monitor

# Links
https://gist.github.com/gitaarik/8735255

https://chrisjean.com/git-submodules-adding-using-removing-and-updating

http://platformio.org/
