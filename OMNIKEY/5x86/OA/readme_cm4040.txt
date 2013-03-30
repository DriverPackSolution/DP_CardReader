                             README.TXT File
    README file for OMNIKEY CardMan 4040, Version 1.1.2.2
               Copyright (c) 2000 - 2007 OMNIKEY

This document describes the release notes of the OMNIKEY CardMan 4040 Driver
============================================================================

NOTE: please do not mix up CardMan 4040 and CardMan 4009.

      a) CardMan 4040 is described in this document

      and

      b) Cardman 4009 Smart Card Holder (S26361-F2432-V600) is a passive
         smartcard holder and can only be used with Fujitsu Siemens LIFEBOOK -
	 Notebooks.


I. General
**********


Supported Operating Systems:
----------------------------

This driver supports the operating systems
Windows 2000
Windows XP
Windows Server 2003
Windows Vista

The installation of the driver is done by Plug and Play under all operating 
systems.



II. Installation and Uninstalling
*********************************


Microsoft Smartcard Base Components:
------------------------------------

The CardMan 4040 needs the Microsoft Smartcard Base Components for proper 
operation.

The Microsoft Smartcard Base Components are already integrated in Windows 2000 
and Windows XP. If you have accidentally installed the Base Components under 
Windows 2000 or Windows XP, you can recover the smartcard subsystem with the 
following commands on an administrator's console window:
Regsvr32 %windir%\system32\scardssp.dll
Scardsvr reinstall

NOTE: Only for Windows XP you must additionally create a .reg file.
      DO NOT DO THIS UNDER W2000 !

      To create this file do the following:

      a) Open an editor (e. g. Notepad)
      b) Type in the text as listed below:

		Windows Registry Editor Version 5.00

		[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\SCardSvr]
		"ObjectName"="NT AUTHORITY\\LocalService"

		[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\SCardDrv]
		"ObjectName"="NT AUTHORITY\\LocalService"

      c) Click on 'File' --> 'Save as', choose a directory and name the file
         (e.g. 'Scard_xp.reg'. Note: It's necessary that the file extension is
	 '.reg'!), click on 'Save'
      d) Open Windows Explorer change to the directory where you have stored
         the *.reg file and doubleclick the file.
      e) Reboot your computer.
      f) Open an administrator's console window again and type in:

         net start scardsvr

	 to start the Smartcard services manually.



II.I Updating:
**************

Step By Step Instructions To Update The Driver:
-------------------------------------------------------------------

The newest driver versions are always available under http://www.omnikey.com.
The files on this web page are selfextracting archives, which are extracted by 
doubleclicking the downloaded .exe file. Please keep the directory structure for 
extraction.


Step 1:
-------

Download the drivers for your CardMan 4040 from http://www.omnikey.com.
Change to the directory where you have stored the downloaded file. Doubleclick on 
the downloaded .exe file. When you are asked, where to unpack the files, choose a 
directory to expand the files to (e. g. c:\drivers\CardMan\).


Step 2:
-------

Windows 2000:
-------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the 'System' 
icon, the 'System Properties window' appears. Click on the 'Hardware' Tab-Sheet 
and then click on the 'Device Manager' button in the middle of the window.
Click on the '+'-sign on the left side of the 'Smart Card Readers' entry to 
display all installed smart card readers. Then click on the 'CardMan 4040' entry 
with the right mouse button and click on the 'Properties' entry in the appearing 
context menue.
Click on the 'Driver' Tab-Sheet and then click on the 'Update Driver' button. The 
'Upgrade Device Driver Wizard' window appears, click 'Next' to continue.
Select 'Display a list ....' and click 'Next'. Click on the 'Have Disk...' 
button. In the 'Install From Disk' window click on the 'Browse' button and select 
the '*.inf' file in the directory where you have unpacked the downloaded file and 
click 'Open'.
Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. A message is shown that the wizard is ready 
to install the driver for the shown hardware device. Click 'Next'.
After Windows has copied the driver files a message appears that windows has 
finished installing the software. Click on the 'Finish' button and close all the 
windows you don't need.
Now the CardMan 4040 is ready for use, because under Windows 2000 it is not 
necessary to reboot the computer.


Windows XP / Server 2003:
-------------------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the 'System' 
icon, the 'System Properties' window appears. Click on the 'Hardware' Tab-Sheet 
and then click on the 'Device Manager' button in the middle of the window.
Click on the '+'-sign on the left side of the Smart Card Readers-entry to display 
all installed smart card readers. Then click on the 'CardMan 4040' entry with the 
right mouse button and click on the 'Update Driver' entry in the appearing 
context menue.
The 'Hardware Update Wizard' window appears, select 'Display a list ... I can 
choose a specific driver' and click 'Next' to continue.
Select 'Choose a specific driver' and click 'Next'. Click on the 'Have Disk...' 
button.
In the 'Install From Disk' window click on the 'Browse' button and select the 
'*.inf' file in the directory where you have unpacked the downloaded file and 
click 'Open'.
Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. Click 'Next'. A message is shown that the 
driver didn't pass the Windows Logo Test confirm the message by clicking on the 
'Continue Installation' button.
After Windows has copied the driver files a message appears that the software for 
the listed device has been installed. Click on the 'Finish' button and close all 
the windows which are not needed anymore.
Now the CardMan 4040 is ready for use, because under Windows XP it is not 
necessary to reboot the computer.


Windows Vista:
--------------

Click on 'Start' --> 'Control Panel', doubleclick on the 'Device Manager' icon.
If you are prompted to enter your Administrator password in the 'User Account 
Control' window do this, if not select 'Continue'.
Click on the '+'-sign on the left side of the Smart Card Readers-entry to display 
all installed smart card readers.
Then click on the 'CardMan xxxx' entry with the right mouse button and click on 
the 'Update Driver Software...' entry in the appearing context menue.
The 'Hardware Update Wizard' window appears, select 'Browse my computer for 
driver software'.
Select 'Let me pick from a list of device drivers on my computer'. Click on the 
'Have Disk...' button.
In the 'Install From Disk' window click on the 'Browse' button and select the 
'*.inf' file in the directory where you have unpacked the downloaded file and 
click 'Open'.
Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. Click 'Next'.
After Windows has copied the driver files a message appears that the software for 
the listed device has been installed. Click on the 'Close' button and close all 
the windows which are not needed anymore.
Now the CardMan is ready for use, because under Windows Vista it is not necessary 
to reboot the computer.


III. General Hints
******************


Synchronous Smartcards:
-----------------------

The synchronous smartcards SLE 4418/4428, SLE 4432/4442 and I2C cards are 
supported in this release of the CardMan 4040 driver.


CardMan Diagnostic Tool:
------------------------

The driver files install also the CardMan Diagnostic Tool on your system.
This tool is listed in the Control Panel and displays version and status 
information.

You can remove the CardMan Diagnostic Tool by deleting the following files:
cmdiag.cpl, cmdiag.ini, cmabout.dll, cmabout.ini and ok.bmp in the SYSTEM32 
directory.



IV. FCC Information:
********************
CardMan 4040 is certified according to the FCC standard. The user must not modify 
reader because otherwise the FCC certification is not valid any longer.
IMPORTANT SAFETY INSTRUCTION! CAUTION - USE THIS DEVICE ONLY WITH LISTED PERSONAL 
COMPUTERS


V. What is new in this release ?
********************************
- Vista support
- minor bug fixes for non ISO compliant cards
- bug fix for shared interrupt handling


Release date: 06/05/2007

--------------------------------- END OF FILE ------------------------------
