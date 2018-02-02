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
- https://elementaryos.stackexchange.com/questions/8362/how-to-set-alternative-terminal-as-default
- https://elementaryos.stackexchange.com/questions/38/configure-files-to-use-double-click/39#39
- https://elementaryos.stackexchange.com/questions/797/how-to-get-gnu-emacs-work-on-elementary-os

*Command Line*

- [Set up default terminal emulator (Ubuntu)](http://www.howtogeek.com/howto/ubuntu/set-the-default-terminal-emulator-on-ubuntu-linux/)
- [Set up tmux](https://robots.thoughtbot.com/a-tmux-crash-course)
- [Set up fish](http://fishshell.com/docs/current/index.html)
- [Mount a USB/CD/etc.](https://askubuntu.com/questions/37767/how-to-access-a-usb-flash-drive-from-the-terminal)

*Extras*

- [Set up Nitrogen and have it maintain state in i3 .config (pt1)](https://www.maketecheasier.com/nitrogen-a-background-setter-for-lightweight-desktop-manager/)
- [Set up Nitrogen and have it maintain state in i3 .config (pt2)](https://faq.i3wm.org/question/6/how-can-i-set-a-desktop-background-image-in-i3/)
- [Set up ncmpcpp/mpd](http://www.linuxandlife.com/2012/01/simple-guide-to-set-up-mpd-with-ncmpcpp.html)

- How to install fonts (google noto): https://www.google.com/get/noto/help/install/

- How to open up ports on AWS: https://stackoverflow.com/questions/5004159/opening-port-80-ec2-amazon-web-services/10454688
- slack in irc (weechat): https://robots.thoughtbot.com/weechat-for-slacks-irc-gateway

#### How to get screen brightness controls working

Using the following links:
- https://unix.stackexchange.com/questions/301724/xbacklight-not-working/385116
- https://faq.i3wm.org/question/3747/enabling-multimedia-keys.1.html

I followed [this](https://unix.stackexchange.com/questions/301724/xbacklight-not-working/385116) to figure out my screen identifiers and get my `xorg.conf` file set up/written from scratch. I then copied the i3 config entries displayed [here](https://faq.i3wm.org/question/3747/enabling-multimedia-keys.1.html).

#### How to get Audio working

Using the following links:
- https://ubuntuforums.org/showthread.php?t=1537375
- https://askubuntu.com/questions/632285/what-process-is-responsible-for-media-keys-in-unity

I installed PulseAudio and ALSA utilities (as described in the first link) and set my i3 config to the example displayed in the second link.

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

- - -

comfy mac tips:

required:
install iTerm2 (look up how to recompile with padding and rounded edges)
install homebrew even if you don't into programming, it's useful for updating software
install a browser that isn't safari

top/menu bar (if you don't just hide it):
bitbar lets you put custom text from script output onto the bar
Bartender lets you hide menu bar icons, get a cracked copy
there's a program called Übersicht I think that lets you re implement the menu bar overlayed on the desktop as widgets but it's literally a web browser so I avoid it

video and media:
install IINA
if you don't stream music then setup ncmpcpp + mpd for terminal music

window managers:
chunkwm is a more unixy config WM with good features
Amethyst has a little bar icon and handy config gui but fewer tiling modes and features
windows kinda snap to each other so manually tiling is possible too

one of the comfiest thing about OSX is that GUIs are scriptable with AppleScript, even if it's the worst language since JS
I used it to write a """theming""" script that changes wallpapers, system dark/light mode, and terminal theme on the fly

Good advice, here's some other stuff:

Install IceFloor, a frontend for the firewall pf (openbsd software) which is shipped with macOS. It's amazing.

Textual is the greatest IRC client ever made, it costs money unless you build it yourself, instructions are here: https://blog.vortigaunt.net/how-to-compile-textual-in-2017/

iTunes is amazing and integrated really well into the macOS environment, especially if you use Apple Music. Give it a shot.

Terminal.app works fine most of the time compared to iTerm2's bloat, and it's not written by someone who accidentally leaked a ton of users passwords over http to their DNS servers. It's what I use.

Macports is also better than homebrew if you're a programmer/have more intricate library/program needs, especially with X11. Homebrew is better if you're inexperienced.

Safari is a great browser, I use it for uni/work/netflix and Firefox for the rest of my internet needs.

Also join the macOS discord

- - - 

thanks for adding good points, I've been thinking of throwing together a ricing/application guide for macOS in the style of the W7 and W10 ones, especially since there's lots of good foss software for mac but sometimes it gets drowned out among the $30 App Store trash

>safari
I used safari for quite a while but got sick of it being selectively sluggish on certain sites, although I miss the webkit css selectors

also could you hmu with a macOS discord link pls
 
