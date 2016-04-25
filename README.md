# RaspberryPIDigitalClock
Raspberry PI Digital Clock

Instructions from: http://qassoom.me/techie/2012/12/09/raspberry-pi-digital-clock/


We need to

start-up the Raspberry Pi with this HTML file.
Hide the mouse once the clock appears.
Disable the screen saver from working.

Install a the lightweight webbrowser for rasphian

sudo apt-get install midori

Install Unclutter

sudo apt-get install unclutter



Disable the Screen Saver by installing xset
sudo apt-get install x11-xserver-utils


Modify the ~/.config/xdg/lxsession/LXDE/autostart file located in your Raspberry Pi SD Card. 
Add these lines of settings to the end of the file.

@xset s off # don’t activate screensaver
@xset -dpms # disable DPMS (Energy Star) features.
@xset s noblank # don’t blank the video device

@midori -e Fullscreen -a /home/pi/digitalclock.html # Run midori in full screen mode and display contents of the html file

