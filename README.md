# Some Scripts for Mac user using Ubuntu i3wm for some reason

I could not use ```xbacklight``` to change the brightness, so I wrote a script for that

### Dependency
Macbook, Ubuntu(not sure which version, but I am using 18.04), i3

### Usage
1. copy incBrightness, decBrightness, fnmode2 to ```/bin/```
2. ```sudo chmod +x /bin/*Brightness /bin/fnmode2```
3. ```sudo chmod 777 /sys/class/backlight/acpi_video0/brightness```
3. ```sudo chmod 777 /sys/module/hid_apple/parameters/fnmode```
4. In ```~/.config/i3/config```, add 
```
exec --no-startup-id fnmode2
bindsym $mod+Fn1 exec decBrightness 
bindsym $mod+Fn2 exec incBrightness
```


This would allow you to modify brightness by pressing Cmd + F1/F2.

incBrightness
: Increments brightness by 5%

decBrightness
: Decrements brightness by 5%


