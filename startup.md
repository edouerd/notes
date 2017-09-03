#### Startup
###### How to set up various devices (To be ordered properly some day)

—

Index

1. [Linux Environment](#linux-environment)
2. [MacOS Environment](#macos-environment)
3. [Windows Environment](#windows-environment)
4. [Misc.](#misc)

—

##### Linux Environment

*Window Management and Input*

- [Convert Unity (Ubuntu WM) into i3](http://walther.io/how-to-replace-unity-with-i3-window-manager-on-ubuntu-1204/)
  - http://i3wm.org/docs/userguide.html#configuring
- [Re-map Caps Lock into Control (Ubuntu)](http://askubuntu.com/questions/33774/how-do-i-remap-the-caps-lock-and-ctrl-keys)
  - http://ubuntuforums.org/showthread.php?t=1793250
- [Fix volume and brightness keys in i3](https://askubuntu.com/questions/632285/what-process-is-responsible-for-media-keys-in-unity)
- [i3 - enabling multimedia keys](https://faq.i3wm.org/question/3747/enabling-multimedia-keys.1.html)
- [i3 + media keys](https://askubuntu.com/questions/632285/what-process-is-responsible-for-media-keys-in-unity)
- [i3 + media keys](https://bbs.archlinux.org/viewtopic.php?id=154838)
- [i3 + media keys](https://wiki.archlinux.org/index.php/Backlight)

*Command Line*

- [Set up default terminal emulator (Ubuntu)](http://www.howtogeek.com/howto/ubuntu/set-the-default-terminal-emulator-on-ubuntu-linux/)
- [Set up tmux](https://robots.thoughtbot.com/a-tmux-crash-course)
- [Set up fish](http://fishshell.com/docs/current/index.html)

*Extras*

- [Set up Nitrogen and have it maintain state in i3 .config (pt1)](https://www.maketecheasier.com/nitrogen-a-background-setter-for-lightweight-desktop-manager/)
- [Set up Nitrogen and have it maintain state in i3 .config (pt2)](https://faq.i3wm.org/question/6/how-can-i-set-a-desktop-background-image-in-i3/)
- [Set up ncmpcpp/mpd](http://www.linuxandlife.com/2012/01/simple-guide-to-set-up-mpd-with-ncmpcpp.html)

```
# bindsym XF86AudioRaiseVolume exec pactl set-sink-volume 0 +5%
# bindsym XF86AudioLowerVolume exec pactl set-sink-volume 0 -- -5%
# bindsym XF86AudioMute exec pactl set-sink-mute 0 toggle

# Pulme Audio controls
bindsym XF86AudioRaiseVolume exec --no-startup-id pactl -- set-sink-volume 0 +5% #increase sound volume
bindsym XF86AudioLowerVolume exec --no-startup-id pactl -- set-sink-volume 0 -5% #decrease sound volume
bindsym XF86AudioMute exec --no-startup-id pactl set-sink-mute 0 toggle # mute sound

# Screen brightness controls
bindsym XF86MonBrightnessUp exec xbacklight -inc 5 # increase screen brightness
bindsym XF86MonBrightnessDown exec xbacklight -dec 5 # decrease screen brightness

# Nitrogen - keep state across startup
exec --no-startup-id nitrogen --restore
```

##### macOS Environment 

*dev setup*

- [Homebrew](https://brew.sh/)
- [Javascript Stack](https://github.com/verekia/js-stack-from-scratch)


##### Misc.

*Twitter Bots*

- [Phython Script](https://github.com/tommeagher/heroku_ebooks)
- [How-to article](https://medium.com/science-friday-footnotes/how-to-make-a-twitter-bot-in-under-an-hour-259597558acf#.htlgy8fqw)
