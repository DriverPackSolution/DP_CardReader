                             README.TXT File
    README file for OMNIKEY CardMan 4040, Version 1.2.1.2
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
Windows Server 2008
Windows 7

The installation of the driver is done by Plug and Play under all operating 
systems.



II. New Installation:
*********************

Plug the OMNIKEY CardMan 4040 into a free USB port.

A 'New Hardware Found' dialog box will appear and you will be asked to select the 
directory where the driver files are stored.

The OMNIKEY Diagnostic Tool is not part of this installation package. It is 
available as a separate installation file.



Microsoft Smart Card Base Components
------------------------------------

The OMNIKEY CardMan 4040 needs the Microsoft Smart Card Base Components for 
proper operation.

CAUTION:
-------
BE AWARE THAT, SINCE WINDOWS 2000, ON ALL WINDOWS OPERATING SYSTEMS THE SMART 
CARD BASE COMPONENTS ARE PART OF THE OPERATING SYSTEM. THERE IS NO NEED TO 
INSTALL THEM MANUALLY AND THEREFORE THEY ARE NOT PART OF THE DRIVER PACKAGE !

If you have accidentally installed the Base Components under Windows 2000 or XP, 
you can recover the smart card subsystem with the following commands on an 
administrator's console window:

Regsvr32 %windir%\system32\scardssp.dll
Scardsvr reinstall

To recover the smartcard subsystem on Windows Vista, Server 2003, Server 2008 and 
Windows 7 the following commands need to be
typed in:

Regsvr32 C:\Windows\system32\scardmgr.dll
Scardsvr reinstall

Note: For Windows XP, Server 2003, Server 2008 and Windows 7 you must 
additionally create a .reg file.
      DO NOT TRY THIS UNDER W2000 !

      To create this file do the following:

      a) Open an editor (e. g. Notepad)

      b) Type in the text as listed below:

		Windows Registry Editor Version 5.00

		[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\SCardSvr]
		"ObjectName"="NT AUTHORITY\\LocalService"

		[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\SCardDrv]
		"ObjectName"="NT AUTHORITY\\LocalService"

      c) Click on 'File' --> 'Save as', choose a directory and name the file
         (e. g. 'Scard_xp.reg'.
         Note: It's necessary that the file extension is '.reg'!),
         click on 'Save'
	
      d) Open Windows Explorer change to the directory where you have stored the
         *.reg file and doubleclick the file.
	
      e) Reboot your computer.

      f) Open an administrator's console window again and type in:

         net start scardsvr

	 to start the smart card services manually.



III. Updating:
**************

Step By Step Instructions To Update The Driver:
-------------------------------------------------------------------

The newest driver versions are always available at 
http://www.hidglobal.com/omnikey.

The files on this web page are selfextracting archives, which are extracted by 
doubleclicking the downloaded .exe file. Please keep the directory structure for 
extraction.


Step 1:
-------

Download the drivers for your smart card reader from 
http://www.hidglobal.com/omnikey.

Change to the directory where you have stored the downloaded file.

Doubleclick on the downloaded .exe file.

When you are asked, where to unpack the files, choose a directory to expand the 
files to (e. g. c:\drivers\OMNIKEY\).



Step 2:
-------

Windows 2000:
-------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the 
'Systemicon', the 'System Properties window' appears.
Click on the 'Hardware' Tab-Sheet and then click on the 'Device Manager' button 
in the middle of the window.

Click on the '+'-sign on the left side of the 'Smart Card Readers' entry to 
display all installed smart card readers.
Then click on the 'OMNIKEY xxxx' entry with the right mouse button and click on 
the 'Properties' entry in the appearing context menue.

Click on the 'Driver' Tab-Sheet and then click on the 'Update Driver' button.
The 'Upgrade Device Driver Wizard' window appears, click 'Next' to continue.

Select 'Display a list ....' and click 'Next'.
Click on the 'Have Disk...' button. In the 'Install From Disk' window click on 
the 'Browse' button and select the '*.inf' file in the directory where you have 
unpacked the downloaded file and click 'Open'.

Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. A message is shown that the wizard is ready 
to install the driver for the shown hardware device. Click 'Next'.

A window may appear that the chosen driver is not digitally signed, you will be 
asked if you want to continue the installation. Click on the 'Yes' button.

After Windows has copied the driver files a message appears that windows has 
finished installing the software. Click on the 'Finish' button and close all the 
windows you don't need.

Now the smart card reader is ready for use, because under Windows 2000 it is not 
necessary to reboot the computer.


Windows XP / Server 2003:
-------------------------

Click on 'Start' --> 'Control Panel', doubleclick on the 'Systemicon', the 
'System Properties' window appears.
Click on the 'Hardware' Tab-Sheet and then click on the 'Device Manager' button 
in the middle of the window.

Click on the '+'-sign on the left side of the Smart Card Readers-entry to display 
all installed smart card readers.
Then click on the 'OMNIKEY xxxx' entry with the right mouse button and click on 
the 'Update Driver' entry in the appearing context menue.

The 'Hardware Update Wizard' window appears, select 'Display a list ... I can 
choose a specific driver' and click 'Next' to continue.

Select 'Choose a specific driver' and click 'Next'. Click on the 'Have Disk...' 
button.

In the 'Install From Disk' window click on the 'Browse' button and select the 
'*.inf' file in the directory where you have unpacked the downloaded file and 
click 'Open'.

Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. Click 'Next'.

After Windows has copied the driver files a message appears that the software for 
the listed device has been installed. Click on the 'Finish' button and close all 
the windows which are not needed anymore.

Now the smart card reader is ready for use, because under Windows XP it is not 
necessary to reboot the computer.


Windows Vista / Windows Server 2008 / Windows 7:
------------------------------------------------

Click on 'Start' --> 'Control Panel', doubleclick on the 'Device Manager' icon.
If you are prompted to enter your Administrator password in the 'User Account 
Control' window do this, if not select 'Continue'.

Click on the '+'-sign on the left side of the Smart Card Readers-entry to display 
all installed smart card readers.
Then click on the 'OMNIKEY xxxx' entry with the right mouse button and click on 
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

Now the smart card reader is ready for use, because under these operating systems 
it is not necessary to reboot the computer.


IV. General Hints
*****************


Synchronous Smartcards:
-----------------------

The synchronous smartcards SLE 4418/4428, SLE 4432/4442 and I2C cards are 
supported in this release of the CardMan 4040 driver.


OMNIKEY Diagnostic Tool:
------------------------

The OMNIKEY Diagnostic Tool is not part of this installation package. It is 
available as a separate installation file.



V. FCC Information:
********************
CardMan 4040 is certified according to the FCC standard. The user must not modify 
reader because otherwise the FCC certification is not valid any longer.
IMPORTANT SAFETY INSTRUCTION! CAUTION - USE THIS DEVICE ONLY WITH LISTED PERSONAL 
COMPUTERS


VI. What is new in this release ?
********************************
- support for Windows 7


Release date: 06/30/2009

--------------------------------- END OF FILE ------------------------------
