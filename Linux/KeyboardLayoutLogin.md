# Keyboard Layout Login

## Problem
The keyboard layout at login is "en" and only changes to de after login.


## Note
Check the locale settings with:
`localectl status `

Check the Arch wiki for more information on
[Locale](https://wiki.archlinux.org/index.php/Locale)
and
[XORG Keyboard Configuration](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration).


## How to fix
Simply change the X11 keyboard layout; not just the system keyboard layout.
Update x11-layout: `localectl set-x11-keymap de`

