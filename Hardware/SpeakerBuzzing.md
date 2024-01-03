# Speakers Buzzing when idle

## Problem
The speakers (connected to the sound card or via USB) are buzzing when no sound is playing from the PC.

## Note
It seems the issue is due to capacitor discharge inside the speakers.
When the sound card goes into power saving mode, not enough power is supplied to the speakers to keep the capacitors charged.
These capacitors then slowly discharge.
This part is speculation: The slight power supply to the empty capacitory causes a constant power change in the speakers which results in a constant buzzing.


## How to fix
The fix is simply to disable the power saving mode of the sound card which allows for the capacitory to stay charged.

The active system modules can be found uder `/sys/module/` where my sound card was named `snd_hda_intel`.
A USB speaker setup can be accessed via the `snd_usb_audio` module.

You can check the `power_save` setting via
`cat /sys/module/snd_hda_intel/parameters/power_save`.
If the value is != 0, the power save mode is on.
The power saving mode can be changed by updating the value in this file to 0.

### Permanent solution
Under `/etc/modprobe.d`, create a file called `audio_disable_powersave.conf` with the content `options snd_hda_intel power_save=0`.
If you are dealing with USB speakers, make sure to set this option for `snd_usb_audio`.


Source: https://itsfoss.com/buzzing-noise-speaker-linux/