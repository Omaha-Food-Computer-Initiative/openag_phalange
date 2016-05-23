# openag_phalange
Firmware for microcontrollers (e.g. Arduino Mega2560) to interface peripherals (sensors &amp; actuators) with a single board computer (e.g. Raspberry Pi 3).

# Compatibility 
This code should be able to be relatively hardware agnostic but has only been tested on Arduino Mega 2560 as of May 22, 2016. 
The idea is that this repo can be cloned / downloaded and be able to run on the ArduinoIDE AND platformio. ArduinoIDE users will need to add the submodules found in this repo's /lib to ~/Documents/Arduino/library.

The example code in the submodules (i.e. openag_am2315) should function properly in both the ArduinoIDE (File/Examples/\<submodule name\>/example) and in platformio (openag_phalange/lib/\<submodule\>/example). This means that each example functions as a standalone platformio package. 


# Install Instructions
1. *Clone repo:* git clone \<repo name\> 
2. *Configure git update:* git config --global alias.update '!git pull && git submodule update --init --recursive'
3. *Update repo:* git update
4. *Install platformio:* pip2 install -U platformio
5. *Connect arduino to rpi w/USB cable*
6. *Compile and upload:* pio run -t upload

# Update Submodule
1. cd \<submodule dir\>
2. git checkout master
3. git pull
4. cd \<module dir\>
5. git commit

# Remove Submodule
1. git submodule deinit asubmodule    
2. git rm asubmodule # Note: asubmodule (no trailing slash)
3. git rm --cached asubmodule
4. rm -rf .git/modules/asubmodule

# Submodule Push
1. cd your_submodule
2. git checkout master
3. \<hack,edit\>
4. git commit -a -m "commit in submodule"
5. git push
6. cd ..
7. git add your_submodule
8. git commit -m "Updated submodule"

# Platformio Commands
* *compile:* pio run
* *compile & upload:* pio run -t upload
* *serial monitor:* pio serialports monitor

# Links
* https://gist.github.com/gitaarik/8735255
* https://chrisjean.com/git-submodules-adding-using-removing-and-updating
* http://platformio.org/
* http://stackoverflow.com/questions/29850029/what-is-the-current-way-to-remove-a-git-submodule
* http://stackoverflow.com/questions/5814319/git-submodule-push
