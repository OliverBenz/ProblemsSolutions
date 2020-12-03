# Github Build Errors

## Problem
Automated Actions suddenly fail installing the necessary dependencies.

## Notes
These changes are done in the `.yaml` files inside the `.github` subfolder of the project.

## How to fix
This problem can usually be fixed by updating the packet manager before installing the dependencies.
`sudo apt install libsdl2` would therefore be changed to
`sudo apt update; sudo apt install libsdl2`
