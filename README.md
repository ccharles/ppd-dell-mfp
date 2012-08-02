# PKGBUILD for Dell multifunction printer drivers #

This is a `PKGBUILD` for Arch Linux to install the Dell multifunction
print driver bundle.

Only the PPD files and spooler binaries are installed. Printers can
then be added via your regular printer management tools.

## Supported printers ##

* dp5330
* mfp2335ps
* mfp1815ps
* dp1130n
* mfp1135n
* mfp2145ps
* dp1130
* mfp1133

Note that I only have access to the mfp1135n on a 64-bit system for
testing, and that I have only tested network printing. Feedback for
other devices and setups is welcome.

## Notes ##

Network printing with the mfp1135n does not seem to work over IPP or
LPD/LPR, though the device claims to support these
protocols. AppSocket / Jetdirect does work using a URL scheme like

    socket://192.168.1.30:9100
