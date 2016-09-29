# icsrandr

```
icsrandr [left|right|below] [--no-sound]
```
A simple bash script to automatically manage "xrandr" stuff.
If you launch it when you connect a second display, it automatically provide to extend desktop (this is not to clone, but to extend).

The default behaviour extend the new space above the original display, but you can append "right" or "left" or "below" arguments to extend in another way:

The script automatically manages HDMI sound (NOTE: YOU MUST HAVE pulseaudio INSTALLED!), unless you add the --no-sound argument: in this case it doesn't do anything related to sound.

The script stays open till you disconnect the display. In that moment, it refreshes a "mono-display" configuration, restores sound configuration (in case it was set to HDMI) and exits. I didn't think this as a daemon because sometime people just wants to use custom setup and I don't want it to be too "invasive". Maybe if I have time (or if anyone which wants to contribute has time!) I can add a "-d" option in the future, so that it can be just put in .xinitrc or .xprofile or whatever, and act as a daemon.

NOTE: If you have Awesome WM installed, the script provides to refresh it so that the background can be automatically fixed. If you don't use Awesome, simply remove that line.
