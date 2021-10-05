# Bluetooth Connect at Startup

## Problem
Bluetooth service only starts when logged in which means that bluetooth keyboard cannot
be used to enter the login password. 


## How to fix
- Make sure the bluetooth service is enabled. `sudo systemctl enable bluetooth.service`
- Edit the bluetooth configuration file `sudo vim /etc/bluetooth/main.conf`.
- Set `AutoEnable=true`.

