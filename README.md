# openag_phalange
Firmware for microcontrollers (e.g. Arduino Mega2560) to interface peripherals (sensors &amp; actuators) with a single board computer (e.g. Raspberry Pi 3).

# Install Instructions
clone repo

initialize submodules: git submodule update --init

to make life easier in the future run: git config --global alias.update '!git pull && git submodule update --init --recursive'

now all that is needed to initialize / update entire repo is to run: git update

# Info
for more info on submodules goto: 

https://gist.github.com/gitaarik/8735255

https://chrisjean.com/git-submodules-adding-using-removing-and-updating


# Other Useful Commands
git submodule foreach git pull origin master
