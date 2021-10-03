# Gnome Terminal Locale

## Problem
Cannot open the gnome terminal because of a locale issue. No error is reported when trying
to open it the normal way but using 'xterm' you get the issue.


## Note
You probably setup the system locale for language/keyboard input/etc in the settings already.
One of the locales you used is not yet enabled in the etc/locale.gen file.

## How to fix
[Arch Locale Documentation](https://wiki.archlinux.org/title/Locale)

- Run `locale -a` to see which locales you have enabled.
- Run `locale` to see which locales you actually use. 

At this point you should see a locale in the second output that is not listed in the first one.

- Edit your locale.gen file: `sudo vim /etc/locale.gen`
- Enable the locale you need. (Uncomment the locale)
- Run `sudo locale-gen` to install the locales.

If the locale you want does not exist in the locale.gen file, you can either install the language
pack or setup a different locale on your system.

