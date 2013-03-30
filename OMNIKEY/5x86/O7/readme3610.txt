                             README.TXT File
     README file for OMNIKEY CardMan 3610 PC/SC Driver, Version 1.0.2.2
                    (C) Copyright OMNIKEY AG, 2002

This document describes the release notes of the CardMan 3610 PC/SC Driver
==========================================================================


I. Installation
***************

Microsoft Windows NT 4.0:
-------------------------

To install the CardMan 3610 PC/SC Interface Device Handler run 'setup.exe'
and follow the instructions in the setup program.

Make sure that you reboot the system before using the CardMan 3610.


Microsoft Windows 95, Windows 98, Windows ME, Windows 2000 & Windows XP:
------------------------------------------------------------------------

The installation will be done by PnP.

1. Connect your CardMan 3610 to a free serial port and to the front of the
   keyboard plug and reboot your machine.

2. Windows 95/98/ME/2000/XP opens a "New Hardware Found" box and prompts for an INF-file.

3. Select "CMTS3WDM.INF"

4. Reboot (is not necessary for Windows 2000/XP)


CardMan Diagnostic Tool:
------------------------

The CardMan Diagnostic Tool is installed automatically on your system by the
driver files.
This tool is listed in the Control Panel and displays version and status
information.

You can remove the CardMan Diagnostic Tool by deleting the following files:

For Windows 95/98/ME: cmdiag.cpl and cmdiag.ini in the SYSTEM directory.
For Windows 2000/XP: cmdiag.cpl and cmdiag.ini in the SYSTEM32 directory.

For Windows NT 4.0: Use the 'Add/Remove Programs' utility in the Control Panel
to uninstall the PC/SC IFD Handler for CardMan 3610


Delay Service for Windows 95/98/ME:
-----------------------------------

The driver files also install a Delay Service for the Resource Manager.
Otherwise, it would start too early and would not find any PnP
Smart Card Reader.


Microsoft Smart Card Base Components:
-------------------------------------

The CardMan 3610 needs the Microsoft Smartcard Base Components for proper
operation.
The Microsoft Smartcard Base Components are already integrated in
Windows 2000/XP and are automatically installed by the driver files for
Windows 95, Windows 98, Windows Millennium Edition and Windows NT 4.0.


II. Uninstalling
****************

Microsoft Windows NT 4.0:
------------------------

You can uninstall the PC/SC driver for CardMan 3610 by using the
'Add/Remove Programs' utility displayed in the Control Panel.
After uninstalling the IFD handler, it is necessary to reboot
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
It is only loaded if a CardMan 3610 is connected.


III. General hints:
*******************

Standby mode:
-------------

The PC/SC handler for Windows 95/98/ME will not allow to go into standby mode,
because the Resource Manager is not capable of this feature.
Otherwise, after returning from standby mode, the reader would not be able
to communicate with the Smart Card any more.
As soon as the Resource Manager supports standby mode, a new PC/SC handler
will be provided by OMNIKEY.



Release date: 04-26-2002

-------------------------------- END OF FILE -------------------------------
