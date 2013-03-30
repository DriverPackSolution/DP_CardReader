
                             README.TXT File
   README file for OMNIKEY CardMan 8630 PC/SC Driver, Version 1.0.4.0
                    (C) Copyright OMNIKEY AG, 2000 - 2004

This document describes the release notes of the OMNIKEY CardMan 8630 Driver
============================================================================


I. General
**********

PLEASE NOTE: NEVER INSTALL THE MICROSOFT SMART CARD BASE COMPONENTS (scbase.exe and smclib.exe)
             MANUALLY!!



Supported Operating Systems:
----------------------------
Windows 98
Windows ME
Windows 2000
Windows XP


Card Interfaces:
----------------
The CardMan 3620 is able to use the PC/SC and the EMV Card Interface.




II. Installation:
*****************

The installation will be done by PnP.
The 'New Hardware Found' dialog box will appear and you will be asked for
the driver location, where you have to select the source directory of the
driver files.

At the same time, the CardMan Diagnostic Tool and the CardMan Configuration Tool
will be installed. These tools are listed in the Control Panel.
The Diagnostic Tool displays version and status information, the Configuration
Tool lists the installed non PnP readers, enables to change their COM
ports and to delete or add non PnP readers. It also allowes experienced users
to choose the Card Interface out of EMV or PC/SC (default).

You can remove the CardMan Diagnostic Tool and the CardMan Configuration Tool
by deleting the following files:

Diagnostic Tool:
For Windows 98 and Windows ME: cmdiag.cpl in the
SYSTEM directory.
For Windows 2000 and Windows XP: cmdiag.cpl in the SYSTEM32 directory.

Configuration Tool:
For Windows 98 and Windows Millennium Edition: cardman.cpl in the
SYSTEM directory.
For Windows 2000 and Windows XP: cardman.cpl in the SYSTEM32 directory.



Microsoft Smartcard Base Components:
------------------------------------

The Microsoft Smartcard Base Components are automatically installed by the
driver files for Windows 98 and Windows Millennium Edition.

The Microsoft Smartcard Base Components are already integrated in Windows
2000 and Windows XP and must not be installed again.

If you have accidentally installed the Base Components under Windows
2000, you can recover the smartcard subsystem with the following commands on
an administrator's console window:
Regsvr32 %windir%\system32\scardssp.dll
Scardsvr reinstall
NOTE: This commands do not work for Windows XP !


What is new in this release ?
------------------------------------
- bug fix for writing 0xF6 bytes to the card


Release date: 06/09/2004

-------------------------------- END OF FILE -------------------------------
