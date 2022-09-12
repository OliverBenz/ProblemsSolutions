# Pacman Invalid Packages

## Problem
When trying to upgrade the system or a specific package, an error occurs that says the package is damaged or the "signature is of marginal trust".

## How to fix
The solution is described in the 
[Endeavouros Wiki](https://forum.endeavouros.com/t/issues-with-signature-is-marginal-trust-signature-is-unknown-trust-or-invalid-or-corrupted-package/6756).

This issue has happened to me multiple times and there were three different fixes:
 - Change the Date&Time setting to "Set date and time automatically".
 - Install the _archlinux-keyring_ which was not done before.
 - Clear the _archlinux-keyring_ and repopulate it.