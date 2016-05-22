# openag_phalange
Firmware for microcontrollers (e.g. Arduino Mega2560) to interface peripherals (sensors &amp; actuators) with a single board computer (e.g. Raspberry Pi 3).

# Install Instructions
1. *Clone repo:* git clone \<repo name\> 
2. *Configure git update:* git config --global alias.update '!git pull && git submodule update --init --recursive'
3. *Update repo:* git update


# Update Submodule To Later Commit
* git submodule init
* git submodule update
* cd \<submodule dir\>
* git checkout master
* git pull
* cd \<mainmodule dir\>
* git commit
* git push

# Platformio Commands
*compile:* pio run

*compile & upload:* pio run -t upload

*serial monitor:* pio serialports monitor

# Links
https://gist.github.com/gitaarik/8735255

https://chrisjean.com/git-submodules-adding-using-removing-and-updating

http://platformio.org/
