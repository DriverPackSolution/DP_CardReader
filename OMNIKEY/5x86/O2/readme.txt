                             README.TXT File
     README file for OMNIKEY CardMan 2011 PC/SC Driver, Version 1.0.1.1
                    (C) Copyright OMNIKEY AG, 2000 - 2002

This Document Describes the Release Notes of the CardMan 2011 PC/SC Driver
==========================================================================


I. General
**********

PLEASE NOTE: NEVER INSTALL THE MICROSOFT SMART CARD BASE COMPONENTS
MANUALLY!!(scbase.exe and smclib.exe)

Because the CardMan 2011 needs the Microsoft Smart Card Base Components for
proper operation, the Microsoft Smart Card Base Components are already
integrated in Windows 2000 and Windows XP. Under all other operating systems
they will be installed automatically with the driver.


Supported Operating Systems:
----------------------------

This driver supports following operating systems :
Windows 95
Windows 98
Windows ME
Windows NT4.0
Windows 2000
Windows XP

II. Installation
***************

Microsoft Windows NT 4.0:
-------------------------

To install the CardMan 2011 PC/SC Interface Device Handler run 'setup.exe'
on disk1 and follow the instructions in the setup program.

Make sure that you reboot the system before you try to use the CardMan 2011.


Microsoft Windows 95, Windows 98, Windows ME , Windows 2000 & Windows XP :
--------------------------------------------------------------------------

The installation will be done by PnP.

1. Connect your CardMan 2011 to a free serial port and to the front of the
   keyboard plug and reboot your machine.

2. Windows 95/98/ME/2000/XP opens a "New Hardware Found" box and prompts for
   an INF-file.

3. Please select the INF-file in the W9x_2k folder

4. Reboot the system (not necessary for Windows 2000/XP)


CardMan Diagnostic Tool:
------------------------

The CardMan Diagnostic Tool is installed automatically on your system by the
driver files.
This tool is listed in the Control Panel and displays version and status
information.

You can remove the CardMan Diagnostic Tool by deleting the following files:
For Windows 95/98/ME: cmdiag.cpl in the SYSTEM directory.
For Windows NT 4.0/2000/XP: cmdiag.cpl in the SYSTEM32 directory.


Delay Service for Windows 95/98/ME:
-----------------------------------

The driver files also install a Delay Service for the Smart Card Resource
Manager.
Otherwise, the Resource Manager would start too early and would not find
any PnP Smart Card Reader.


Microsoft Smart Card Base Components:
-------------------------------------
If you have installed the Base Components under Windows 2000,
you can recover the smart card subsystem with the following commands on an
administrator's console window:

Regsvr32 %windir%\system32\scardssp.dll
Scardsvr reinstall


II. Uninstalling
****************

Microsoft Windows NT 4.0:
-------------------------

You can uninstall the PC/SC driver for CardMan 2011 by using the
'Add/Remove Programs' utility displayed in the Control Panel.
After uninstalling the IFD Handler it is necessary to reboot
the machine.
Then the changes will take effect.

If the Microsoft Resource Manager cannot find any PC/SC Smart Card Reader
during boot, the service control manager will display the message box
'At least one service failed to start..'.
You can avoid this error message by manually changing the following value
in the Registry:

Old value:
HKLM\System\CurrentControlSet\Services\ScardSvr\ErrorControl=0x00000001

New value:
HKLM\System\CurrentControlSet\Services\ScardSvr\ErrorControl=0x00000000


Microsoft Windows 95/98/ME/2000/XP:
-----------------------------------

Due to the PnP mechanism, it is not necessary to uninstall the driver.
It is only loaded if a CardMan 2011 is connected.


III. General hints:
*******************

Standby mode:
-------------

The PC/SC handler for Windows 95/98/ME will not allow to go into standby mode,
because the Resource Manager is not capable of this feature.
Otherwise, after returning from standby mode, the reader would not be able
to communicate with the Smart Card anymore.
As soon as the Resource Manager supports standby mode, a new PC/SC Handler
will be provided by OMNIKEY.


Update Driver with Device Manager under Windows 95/98/ME:
---------------------------------------------------------

Because the Resource Manager is not capable of detecting PnP devices,
two error messages
(1. Reader removal monitor error ...
 2. Reader monitor ' OMNIKEY CardMan 2011' received uncaught error code ...)
occur if the driver is updated by using the Device Manager.
Just click 'OK', reboot and the CardMan 2011 is ready again.



IV. What is new in this release?
********************************
- bug fix for Easyflex smart card



Release date: 11-15-2002

-------------------------------- END OF FILE -------------------------------
