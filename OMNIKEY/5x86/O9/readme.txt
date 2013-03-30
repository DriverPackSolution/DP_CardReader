                              README.TXT File
        README file for OMNIKEY CardMan 4000 Driver, Version 3.5.0.12
                Copyright (c) 2000 - 2005 OMNIKEY

This document describes the release notes of the OMNIKEY CardMan 4000 Driver
============================================================================

NOTE: please do not mix up CardMan 4000 and CardMan 4009.

      a) CardMan 4000 is described in this document

      and

      b) Cardman 4009 Smart Card Holder (S26361-F2432-V600) is a passive
         smartcard holder and can only be used with Fujitsu Siemens LIFEBOOK -
	 Notebooks.


I. Installation and Uninstalling
********************************


Microsoft Windows NT 4.0:
-------------------------

To install the CardMan 4000 PC/SC Interface Device Handler run 'setup.exe' and 
follow the instructions in the setup program.
Make sure that you reboot the system before you try to use the CardMan 4000.

Uninstalling of the driver can be done via the Control Panel - Add/Remove
Programs - by choosing PC/SC IFD handler for CardMan 4000.


Microsoft Windows 98, Windows Millennium Edition, Windows 2000 and Windows XP:
------------------------------------------------------------------------------

The installation will be done by PnP.
The 'New Hardware Found' dialog box will appear and you will be asked for the 
driver location, where you have to select the source directory of the driver 
files.
Now reboot the system with the inserted CardMan 4000. (This is not necessary 
for Windows 2000 and Windows XP)


Microsoft Windows 95:
---------------------

The installation will be done by PnP.
The 'New Hardware Found' dialog box will appear and you will be asked for the 
driver location, where you have to select the source directory of the driver 
files.
Now reboot the system with the inserted CardMan 4000.
If the Microsoft Smartcard Base Components are not already installed, it may 
need a little bit of extra time to boot the system the first time, so please 
be patient.
Then you will have to boot again, so that the CardMan 4000 is ready for use.


Microsoft Smartcard Base Components:
------------------------------------

The CardMan 4000 needs the Microsoft Smartcard Base Components for proper 
operation.

The Microsoft Smartcard Base Components are automatically installed by the 
driver files for Windows 95, Windows 98, Windows Millennium Edition and 
Windows NT 4.0.

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



I.I Updating:
*************

Step By Step Instructions To Update The Driver:
-------------------------------------------------------------------

The newest driver versions are always available under http://www.omnikey.com.
The files on this web page are selfextracting archives, which are extracted by 
doubleclicking the downloaded .exe file. Please keep the directory structure 
for extraction.


Step 1:
-------

Download the drivers for your CardMan 4000 from http://www.omnikey.com.
Change to the directory where you have stored the downloaded file. Doubleclick 
on the downloaded .exe file. When you are asked, where to unpack the files, 
choose a directory to expand the files to (e. g. c:\drivers\CardMan\).


Step 2:
-------

Windows 98/ME:
--------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the 
'System' icon, the System Properties window appears.Click on the 'Device 
Manager' Tab-Sheet.
Click on the '+'-sign on the left side of the Smart Card Readers-entry to 
display all installed smart card readers. Then click on the 'CardMan 4000' 
entry to highlight it. The next step is to click on the 'Properties' button 
below.
Click on the 'Driver' Tab-Sheet and then click on the 'Update Driver' button. 
Verify that the device you want to update is shown in the 'Update Device 
Driver Wizard window and click 'Next'.
Select 'Display a list ....' and click 'Next'. Click on the 'Have Disk...' 
button. In the 'Install From Disk' window click on the 'Browse' button and 
select the '*.inf' file in the directory where you have unpacked the 
downloaded file and click 'OK'. Verify that the correct path to the file is 
shown in the 'Copy manufacturer's files from:' window and click 'OK' again.
Click 'Next' and confirm the 'Update Driver Warning' window by clicking on the 
'Yes' button.
The 'Update Device Driver' Window tells you that Windows is now ready to 
install the selected driver. Click 'Next' and Windows will copy the driver 
files.
The 'System Settings Change' window appears and tells you that the device has 
been successfully installed and that you will have to reboot the computer 
before you can use it. Click 'OK'. In the 'Update Device Driver Wizard' window 
click 'Finish'. Confirm the question for rebooting with 'Yes'.
After the reboot CardMan 4000 is ready for use.


Windows 2000:
-------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the 
'System' icon, the 'System Properties window' appears. Click on the 'Hardware' 
Tab-Sheet and then click on the 'Device Manager' button in the middle of the 
window.
Click on the '+'-sign on the left side of the 'Smart Card Readers' entry to 
display all installed smart card readers. Then click on the 'CardMan 4000' 
entry with the right mouse button and click on the 'Properties' entry in the 
appearing context menue.
Click on the 'Driver' Tab-Sheet and then click on the 'Update Driver' button. 
The 'Upgrade Device Driver Wizard' window appears, click 'Next' to continue.
Select 'Display a list ....' and click 'Next'. Click on the 'Have Disk...' 
button. In the 'Install From Disk' window click on the 'Browse' button and 
select the '*.inf' file in the directory where you have unpacked the 
downloaded file and click 'Open'.
Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. A message is shown that the wizard is 
ready to install the driver for the shown hardware device. Click 'Next'.
A window may appear that the chosen driver is not digitally signed, you will 
be asked if you want to continue the installation. Click on the 'Yes' button.
After Windows has copied the driver files a message appears that windows has 
finished installing the software. Click on the 'Finish' button and close all 
the windows you don't need.
Now the CardMan 4000 is ready for use, because under Windows 2000 it is not 
necessary to reboot the computer.


Windows XP:
-----------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the 
'System' icon, the 'System Properties' window appears. Click on the 'Hardware' 
Tab-Sheet and then click on the 'Device Manager' button in the middle of the 
window.
Click on the '+'-sign on the left side of the Smart Card Readers-entry to 
display all installed smart card readers. Then click on the 'CardMan 4000' 
entry with the right mouse button and click on the 'Update Driver' entry in 
the appearing context menue.
The 'Hardware Update Wizard' window appears, select 'Display a list ... I can 
choose a specific driver' and click 'Next' to continue.
Select 'Choose a specific driver' and click 'Next'. Click on the 'Have 
Disk...' button.
In the 'Install From Disk' window click on the 'Browse' button and select the 
'*.inf' file in the directory where you have unpacked the downloaded file and 
click 'Open'.
Verify that the correct path to the file is shown in the 'Copy manufacturer's 
files from:' window and click 'OK'. Click 'Next'. A message is shown that the 
driver didn't pass the Windows Logo Test confirm the message by clicking on 
the 'Continue Installation' button.
After Windows has copied the driver files a message appears that the software 
for the listed device has been installed. Click on the 'Finish' button and 
close all the windows which are not needed anymore.
Now the CardMan 4000 is ready for use, because under Windows XP it is not 
necessary to reboot the computer.



II. General Hints
*****************


Removal and Reinsertion of CardMan 4000:
----------------------------------------

Although several operating systems and card enablers are capable of 
configuring the PCMCIA cards, if a CardMan 4000 is inserted AFTER the boot up 
procedure of the operating system, only the Windows 2000 and Windows XP 
Smartcard Resource Manager is able to recognize it.
This means that it is necessary to reboot the computer after the CardMan 4000 
has been inserted, if you are running one of the following operating systems:
Windows NT 4.0, Windows 95, Windows 98 and Windows Millennium Edition.
It also means that in case you have removed the CardMan 4000 and you want to 
use it again, you must reboot your system one more time.


Standby Mode:
-------------

The standby mode is supported in Windows 98 Second Edition, Windows Millennium 
Edition, Windows 2000 and Windows XP.
The standby mode is disabled for Windows 95 and Windows 98.


Card Enabler:
-------------

The CardMan 4000 has been successfully tested with the following card enablers 
under Windows NT 4.0:

    Award Cardware 6.0.011
    Systemsoft Card Wizard 5.00.12
    Softex Card Services 2.0

The CardMan 4000 works fine with these card enablers, but it is only possible 
to work with one CardMan 4000 in this configuration.


Synchronous Smartcards:
-----------------------

The synchronous smartcards SLE 4418/4428, SLE 4432/4442 and I2C cards are 
supported in this release of the CardMan 4000 driver.


CardMan Diagnostic Tool:
------------------------

The driver files install also the CardMan Diagnostic Tool on your system.
This tool is listed in the Control Panel and displays version and status 
information.

You can remove the CardMan Diagnostic Tool by deleting the following files:
For Windows 95, Windows 98 and Windows Millennium Edition: cmdiag.cpl, 
cmdiag.ini, cmabout.dll, cmabout.ini and ok.bmp in the SYSTEM directory.
For Windows NT 4.0, Windows 2000 and Windows XP: cmdiag.cpl, cmdiag.ini, 
cmabout.dll, cmabout.ini and ok.bmp in the SYSTEM32 directory.




Release date: 05/18/2005

--------------------------------- END OF FILE ------------------------------
