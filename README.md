ScreenLayout
============

A tiny script to make handling screenlayouts with non-desktop-environment window managers,
such as `i3` and `xmonad`, better.

Make sure you have `zenity` and `xrandr` installed, then make a directory in your homedir called
`.screenlayout`, and for each desired screen arrangement, put one scripts in there which uses `xrandr` to make it so.

This program prompts you to choose a layout, and then runs it.

Tips
----

The quickest way to make this directory and these scripts is an almost as tiny python GUI called `arandr`.

If you find yourself switching configurations between different physical workspaces often, add this to your `.xinitrc`, e.g.
```
xterm &
~/.local/bin/screenlayout &
exec i3
```

Bugs
----

Does not do the 15s "set it back!" deadman's timer that Windows, Gnome, and KDE do on screen switching.
 ..though zenity could probably be forced into doing that too.

This is worth factoring into a subroutine which takes a directory of scripts and asks you to choose one.
