TF101
=====

Each code is just a script to do a task, you need to map a shortcut key to do the task..
How I have been doing it is as the below:
xev
find the keycode I want to map.. 
(key code 68 is touchpad button on the TF101 dock)

xmodmap -e "keycode 68 = F14"

Then save the config:
xmodmap -pke > .Xmodmap

Then edit the openbox config:
File: ~/.config/openbox/lubuntu-rc.xml

Add this code in the <keyboard> 

<keybind key="F14">
  <action name="Execute"><execute>/usr/bin/touchpadtrigger</execute></action>
</keybind>





Repo for TF101 scripts and codes for key mapping
