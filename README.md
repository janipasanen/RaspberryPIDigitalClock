# RaspberryPIDigitalClock
Raspberry PI Digital Clock

Instructions from: http://qassoom.me/techie/2012/12/09/raspberry-pi-digital-clock/


We need to

start-up the Raspberry Pi with this HTML file.
Hide the mouse once the clock appears.
Disable the screen saver from working.
Step by step,

Modify the /etc/xdg/lxsession/LXDE/autostartlocated in your Raspberry Pi SD Card (do not mistaken it with the one you have on your computer! make sure that you don’t edit the one in your Linux operating system, but the one located WITHIN your SD Card) with your favourite text editor. I would go again with Bluefish. Add a line to the end of the file with the following script
@midori -e Fullscreen -a /home/pi/digitalclock.html
Install Unclutter
sudo apt-get install unclutter
Disable the Screen Saver by installing xset
sudo apt-get install x11-xserver-utils
Now open up your ~/.xinitrc file (if you don’t have one then create it) and enter this:

xset s off # don’t activate screensaver
xset -dpms # disable DPMS (Energy Star) features.
xset s noblank # don’t blank the video device
exec /etc/alternatives/x-session-manager # start lxde
We are done here! I hope you enjoyed this tutorial, and if you have any question in mind regarding any step, a suggestion in mind to make this application better or a completely different idea don’t hesitate to post it as a comment here, or even better open a topic at the forums in The Assembly.
