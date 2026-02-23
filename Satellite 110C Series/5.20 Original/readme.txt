README.TXT                                                     05-12-1999 CDC
Flash BIOS version 5.20 for Satellite 110C Series
=============================================================================

This BIOS is applicable to the following models:

Satellite 110CS
Satellite 110CT
Satellite 115CS

For purposes of this document, the term "Satellite 110C Series"
is used to generically refer to all of the models listed above.
=============================================================================

This archive contains the following files:

README.TXT      Installation/usage instructions in ASCII text format
README.COM      Self-displaying version of installation/usage instructions
1002D520.EXE    Self-extracting diskette image of BIOS install diskette
BIOFCDDT.COM    Flash BIOS 5.20 image for Satellite 110C Series
                (provided here for installation methods 2 and 3)
CHGBIOS.EXE     Flash BIOS update utility for Satellite 110C Series
                (provided here for installation methods 2 and 3)
INSTINFO.BAT    DOS batch file that creates install disk and displays README
                file

This BIOS version is Windows 95 compatible and supports Plug and Play
functionality.

********************************** CAUTION! *********************************
*****************************************************************************

During the upgrading of your computers BIOS, if the computer loses power or
fails to complete the process of upgrading the BIOS, the existing BIOS in
the computer may become damaged. In the event of this occurring, the
F12 Installation Method, described below, can be used to recover from
this error condition.

If you are upgrading a number of computers with this BIOS, the F12
installation method is the quickest, but does require a separate low
density (720 KB) diskette.

It is recommended that all PCMCIA cards be removed from the system prior to
upgrading the BIOS.  Also advisable is removing the computer from an attached
DeskStation V or DeskStation V Plus or NoteDock Enhanced Port Replicator.

It is not unusual to see a CMOS error when you first reboot the computer after
installing the new BIOS.  If you see this message on your screen, press F1 as
instructed.  This displays the "TSETUP" screen. Press <End> to save the CMOS
data.  You won't see the CMOS error again.


******************** BIOS INSTALLATION INSTRUCTIONS *************************
*****************************************************************************

There are three ways to install this BIOS version:

1) Use the bootable diskette that is automatically created by the Windows
   UnZip process (Recommended)

2) At startup by holding down the F12 key.

3) Run CHGBIOS.EXE at the command prompt.

*****************************************************************************


1) BOOT DISKETTE INSTALLATION METHOD (Recommended)
--------------------------------------------------

This release of the electronic distribution BIOS utilizes a self-extracting
ZIP file that, when run under Windows or Win-OS2, creates a bootable BIOS
installation diskette.

Since you're reading this, you were obviously able to extract the downloaded
file.  If you also created the BIOS installation diskette as a part of the
extraction process, you're ready to follow the installation instructions
below.

If you didn't create the installation diskette during the extraction phase,
or if you extracted the downloaded file with PKUnZip or WinZip, you can
create the installation diskette by executing the INSTINFO program from the
DOS command prompt.

Install this BIOS using the following steps:

WINDOWS 95/98 or Windows NT 4.x:

      o Close all open programs
      o Insert the BIOS installation diskette into your diskette drive (A:)
      o Click Start
      o Click Shutdown
      o Click the radio button next to "Restart the computer?"
      o Click Yes

WINDOWS 3.x:

      o Close all open programs
      o From Program Manager, click on File/Exit Windows
        Windows exits to a MS-DOS command prompt
      o Insert the BIOS installation diskette into your diskette drive (A:)
      o Press Ctrl-Alt-Del (press and hold the <Ctrl> and <Alt> keys and press
        the <Del> key) to restart the system

OTHER OPERATING SYSTEMS

      o Close all open programs
      o Shut down the operating system
      o Insert the BIOS installation diskette into your diskette drive (A:)
      o Restart the computer by pressing Ctrl-Alt-Del or turning the computer
        OFF then on again

The computer will boot MS-DOS from the BIOS installation diskette, and
initiate the Flash BIOS installation routine.  When the Flash BIOS
installation is complete, the success message is displayed:


        Please push the RESET SW (or turn AC power OFF/ON) to restart!

                             ROM Write Successful!
                               Utility Finished!


Eject the diskette from drive A: and turn the computer OFF then ON, or press
the reset switch to restart your computer.


ADDITIONAL INFORMATION REGARDING THIS RELEASE
---------------------------------------------

If you are unable to use the Windows self-extractor, the self-extracting
ZIP archive can be extracted by executing it from a DOS prompt or it can be
extracted using PKUNZIP 2.04G or an equivalent UnZIP utility.  A DOS batch
file, INSTINFO.BAT is provided in the ZIP archive which will create the BIOS
installation diskette.  If all else fails, you can execute the
self-extracting diskette image manually.  This file is named 1002D520.EXE, and
needs a parameter of A: (1002D520 A:) to successfully create the diskette in
drive A:

The self-extracting diskette image, 1002D520.EXE, will run under MS-DOS or a
command prompt under Windows 95/98, NT, or OS/2.  PLEASE NOTE that long
directory names in  the path where the self-extracting image file is stored
under Windows 9x or NT will cause the self-extracting image to abort.  Long
directory names are supported under OS/2.



2) F12 INSTALLATION METHOD
---------------------------

Your Toshiba computer has a special keyboard function to install an
updated BIOS image.

IMPORTANT!
----------
To use this function, both the CHGBIOS.EXE program and the BIOS image file,
BIOFCDDT.COM, must be placed on a LOW DENSITY (720 KB) diskette.  A high
density (1.44 MB) floppy disk will not work.

To use this function, hold down the F12 while the computer is powered on.
The computer MUST be in BOOT mode, not Resume mode.

The F12 installation method will only work with the internal keyboard.  If
your computer is docked with the display closed and you are using an external
keyboard, the computer will need to be undocked and the internal keyboard's
F12 key used.

When the computer starts up with the F12 key depressed, the following
message appears:

'Ready for BIOS update. Place the BIOS diskette in the drive, and press
any key when ready to proceed.'

Insert the diskette that contains CHGBIOS.EXE and BIOFCDDT.COM,
and press any key.  The CHGBIOS program will automatically load the
BIOFCDDT.COM file.

3) RUN CHGBIOS.EXE AT THE COMMAND PROMPT
-----------------------------------------

The CHGBIOS program is designed to be run from the MS-DOS command
prompt.  It cannot be run in a DOS box inside of Windows 3.x, Windows 9x,
OS/2 or other operating systems.  It also will not run if a Memory Manager,
like EMM386, is loaded.  The CHGBIOS program can be run from a
floppy disk, hard drive, or PCMCIA drive.  However, you will need a floppy
diskette (high or low density) in your A: drive at the time the CHGBIOS
program is run.

When the CHGBIOS program is executed by itself, it will prompt you
to specify where the BIOS image file, BIOFCDDT.COM is located.  Enter
the complete path and file name. Example: C:\1110CV52\BIOFCDDT.COM.

NOTE!
-----

If your path for BIOFCDDT.COM is anywhere other than the root directory
of the A: drive (A:\BIOFCDDT.COM), CHGBIOS will copy the BIOS image
file from its current location to the root directory of A: drive.


Optionally, the CHGBIOS program can also be run from a single command
which includes the path to the BIOFCDDT.COM file.

   Example: CHGBIOS C:\1110CV52\BIOFCDDT.COM


CHANGE HISTORY
--------------

Version 5.20  05-07-1999
  o  Corrected a problem where, when using an incorrect key floppy
     diskette, the password would be canceled.


 **end**

