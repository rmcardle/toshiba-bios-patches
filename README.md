# toshiba-bios-patches

*toshiba-bios-patches* provides patched BIOS files for 90s-era Toshiba laptops.

These patches have had very limited testing and are provided "as is". They may cause data loss, corruption, unrecoverable hardware failure, or other harms. Please read and understand the [license terms](LICENSE.txt), especially section 15, Disclaimer of Warranty, and section 16, Limitation of Liability, before your use of them.

## Related Repositories

* [toshiba-bios-tools-python](https://github.com/rmcardle/toshiba-bios-tools-python) &ndash; Python tools for reverse engineering and patching Toshiba BIOS files.
* [toshiba-bios-tools-dos](https://github.com/rmcardle/toshiba-bios-tools-dos) &ndash; DOS tools for reverse engineering Toshiba BIOS code.
* [toshiba-sp430c-disassembly](https://github.com/rmcardle/toshiba-sp430cdt-disassembly) &ndash; Partial disassembly of the BIOS code and related utilities for the Toshiba Satellite Pro 430C Series.

## Included Patches

### Toshiba Satellite 110CS/110CT/115CS

[Patched BIOS version 5.21](Satellite%20110C%20Series/5.21%20Patched/) based on [original BIOS version 5.20](Satellite%20110C%20Series/5.20%20Original/) (Recommended)  
[Patched BIOS version 5.11](Satellite%20110C%20Series/5.11%20Patched/) based on [original BIOS version 5.10](Satellite%20110C%20Series/5.10%20Original/)  

* Skip memory test &ndash; This patch removes the memory test during POST so that booting is much faster.

### Toshiba Satellite Pro 430CDS/430CDT/435CDS/435CDT

[Patched BIOS version 6.51](Satellite%20Pro%20430C%20Series/6.51%20Patched) based on [original BIOS version 6.50](Satellite%20Pro%20430C%20Series/6.50%20Original)

* Fix ~8GiB hard disk size limit &ndash; This patch fixes the int 13 function 48 handler to return the correct hard drive size.
* Skip memory test &ndash; This patch removes the memory test during POST so that booting is much faster.
* Text mode stretch &ndash; This patch sets text mode stretch to be enabled by default.

## Installation Instructions

As a precaution, before flashing the patched BIOS, it is recommended that you copy the original unpatched `BIO????T.COM` and `CHGBIOS.EXE` files to a separate double-density (720KB) floppy disk for recovery purposes. You can use that floppy disk with the F12 Boot ROM installation method to revert to the original BIOS if you encounter any problems with the patched BIOS.

### F12 Boot ROM Installation Method (Recommended)

This method uses the low-level Boot ROM to flash the BIOS and can be used to recover a system with a corrupted BIOS. It requires a working floppy drive and a blank, MS-DOS formatted, double-density (720KB) floppy disk. A high-density (1.44MB) floppy disk will not work.

The laptop must be set to Boot Mode not Resume Mode. Press Fn-F3 to toggle between Boot Mode and Resume Mode or configure it in MaxTime, the Toshiba System control panel, or `TSETUP`.

1. Copy `BIO????T.COM` and `CHGBIOS.EXE` to the floppy disk.
2. Power off the laptop.
3. Press and hold the `F12` key on the laptop's internal keyboard while powering on the laptop.
4. Follow the on-screen instructions.

### MS-DOS Installation Method

This method requires a bootable copy of MS-DOS. A DOS prompt inside Windows or OS/2 will not work. No memory manager (such as EMM386) can be loaded. It is recommended that you bypass `CONFIG.SYS` and `AUTOEXEC.BAT` to prevent anything else from loading as well. On MS-DOS 5.0 or above, reboot and hold the `Shift` key while "Starting MS-DOS..." is displayed to bypass `CONFIG.SYS` and `AUTOEXEC.BAT`.

1. Copy `BIO????T.COM` and `CHGBIOS.EXE` to the laptop.
2. Type `CHGBIOS` followed by the name of the `BIO????T.COM` file and press the `Enter` key.  
    For example:
    > CHGBIOS BIOFCD7T.COM
3. Follow the on-screen instructions.

## Thanks

Special thanks to the following people for providing tools and information that helped in this reverse engineering project:

* Ralf Brown for [Ralf Brown's Interrupt List](https://www.ctyme.com/rbrown.htm).
* Jonathan Buzzard <<jonathan@buzzard.org.uk>> for [technical documentation](http://www.buzzard.me.uk/toshiba/docs.html) of the Toshiba System Configuration Interface and Hardware Configuration Interface.
* Charles Schwieters <<charles@schwieters.org>> for [toshset](https://schwieters.org/toshset/).
* Wilhelm Bockey <<lds100ct@bockey.ipcon.de>> for [LDS100ct](https://web.archive.org/web/20060303082306/http://bockey.ipcon.de:80/MB_DOS/LDS100CT.HTM).
* [LongSoft](https://github.com/LongSoft/) for [ToshibaComExtractor](https://github.com/LongSoft/ToshibaComExtractor/).

## Legal

Original BIOS files and related content  
Copyright &copy; 1991-99 Toshiba Corporation  
All Rights Reserved

BIOS patches and patch documentation  
Copyright &copy; 2024-26 Riley McArdle <<riley@mcardle.org>>  
Distributed under the terms of the [GNU General Public License version 3](LICENSE.txt)

Toshiba is a registered trademark of Kabushikigaisha Toshiba. This software is not authorized or endorsed by Kabushikigaisha Toshiba or Dynabook Inc.
