u-boot scripts
==============

This folder contains all the boot scripts for u-boot:
* `boot_counting`: boot script for POWER ON/OFF test

Those `bootcmd` files need to be transformed into u-boot scripts (`.scr`) using `mkimage`.

Here is an example for generating a `boot.scr` for 32-bit platforms running boot counting scripts:
```
mkimage -A arm -T script -C none -n 'u-boot Power ON/OFF counting script' -d bootcmd boot.scr
```

Here is an example for generating a `boot.scr` for 64-bit platforms running boot counting scripts:
```
mkimage -A arm64 -T script -C none -n 'u-boot Power ON/OFF counting script' -d bootcmd boot.scr
```
