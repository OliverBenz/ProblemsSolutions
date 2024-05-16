# Wifi Connection via Sway

## Problem
Trying to connect to the university wifi does not work.
Gives the error:
`Could not activate connection: Failed to determine AP security information`.

## How to fix
Use the `nm-connection-editor` program to get a graphical overview of your connection.
Manually enter:
 - Wifi > SSID: "UIBK"
 - Wifi-Security > Security: "WPA/WPA2"
 - Wifi-Security > Authentication: "Tunnelled TLS"
 - No CA certificate is required: check true
 - Wifi-Security > Inner Authentication: "PAP"
 - Wifi-Security > Username: "username"
 - Wifi-Security > Password: "password"

Source:
https://forum.artixlinux.org/index.php/topic,2990.0.html