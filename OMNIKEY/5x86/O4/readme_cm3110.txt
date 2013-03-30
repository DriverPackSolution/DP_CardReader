
                             README.TXT File
    README file for OMNIKEY CardMan 3110, Version 1.0.2.3
                Copyright (c) 2000 - 2003 OMNIKEY AG

  This document describes the release notes of the OMNIKEY CardMan 3110 Driver
=================================================================================



I. General
**********


PLEASE NOTE: NEVER INSTALL THE MICROSOFT SMART CARD BASE COMPONENTS
MANUALLY!!(scbase.exe and smclib.exe)


Supported Operating Systems:
----------------------------

This driver supports the operating systems
Windows 95
Windows 98
Windows ME
Windows NT4.0
Windows 2000
Windows XP

Under NT4.0 the installation is done by a setup program, under all other operating
systems by Plug And Play.


II. New Installation:
*********************

Windows 98SE/Me/2000/XP:
------------------------

The installation will be done by PnP.
The 'New Hardware Found' dialog box will appear and you will be asked for the
driver location, where you have to select the source directory of the driver
files.

At the same time, the CardMan Diagnostic Tool will be installed. This tool is
listed in the Control Panel and displays version and status information.

You can remove the CardMan Diagnostic Tool by deleting the following files: For
Windows 98 and Windows Millennium Edition: : cmdiag.cpl, cmdiag.ini, cmabout.dll,
cmabout.ini and ok.bmp in the SYSTEM directory.
For Windows 2000: cmdiag.cpl and cmdiag.ini in the SYSTEM32 directory.



Windows NT 4.0:
---------------

To install the CardMan 3110 PC/SC Interface Device Handler run 'setup.exe'
and follow the instructions in the setup program.


MS Smart Card Base Components
-----------------------------

The CardMan 3110 needs the Microsoft Smartcard Base Components for proper
operation.

The Microsoft Smartcard Base Components are automatically installed by the driver
files for Windows 95, Windows 98, Windows Millennium Edition and Windows NT 4.0.

The Microsoft Smartcard Base Components are already integrated in Windows 2000
and XP.
If you have accidentally installed the Base Components under Windows 2000, you
can recover the smartcard subsystem with the following commands on an
administrator's console window:

Regsvr32 %windir%\system32\scardssp.dll
Scardsvr reinstall

Note: Only for Windows XP you must additionally create a .reg file.
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

	 to start the Smartcard services manually.


III. Updating:
**************

Step By Step Instructions To Update The Drivers From The Internet:
-------------------------------------------------------------------

The newest driver versions are always available under www.omnikey.com.

The files on this web page are selfextracting archives, which are extracted by
doubleclicking the downloaded .exe file. Please keep the directory structure
for extraction.


Step 1:
-------

Download the drivers for your CardMan from http://www.omnikey.com.

Change to the directory where you have stored the downloaded file.

Doubleclick on the downloaded .exe file.

When you are asked where to unpack the files choose a directory to expand the
files to (e. g. c:\drivers\CardMan 3110\).

After unpacking the driver files you will get some folders in the directory
you have chosen to unpack the files. These folders contain the driver files for
the different operating systems.


Step 2:
-------

Windows 98/ME:
--------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the
'System' icon, the 'System Properties' window appears.
Click on the 'Device Manager' Tab-Sheet.

Click on the '+'-sign on the left side of the 'Smart Card Readers' entry
to display all installed smart card readers.

Then click on the 'CardMan 3110' entry to highlight it. The next step is to
click on the 'Properties' button below.

Click on the 'Driver' Tab-Sheet in the 'CardMan 3110 Properties' window and then
click on the 'Update Driver' button.
Verify that the device, you want to update, is shown in the 'Update Device
Driver Wizard' window and click 'Next'.

Select 'Display a list ...' and click 'Next'.
Click on the 'Have Disk...' button. In the 'Install From Disk' window click on
the 'Browse' button, go to the folder where you have unpacked the downloaded file,
look for a folder that has a name according to the operating system you are using,
select the '*.inf' file in this directory and click 'OK'.

Verify that the correct path to the file is shown in the 'Copy manufacturer's
files from:' window and click 'OK' again.

Click 'Next' and confirm the 'Update Driver Warning' window by clicking on the
'Yes' button.

The 'Update Device Driver' Window tells you that Windows is now ready to install
the selected driver. Click 'Next' and Windows will copy the driver files.

Confirm the 'Reader removal ...' error messages from Smart Card System by clicking
'OK' two times.

The 'System Settings Change' window appears and tells you that the device has been
successfully installed and that you will have to reboot the computer before you can
use the device.

Click 'OK'. In the 'Update Device Driver Wizard' window click 'Finish'.
Confirm the question for rebooting with 'Yes' and restart your machine.

After the reboot of your computer you can use your CardMan 3110.



Windows NT 4.0:
---------------

Open your Windows Explorer, go to directory where you have unpacked the downloaded
files, open the folder called 'Nt4', doubleclick on the 'setup.exe' file and follow
the instructions displayed on the screen.



Windows 2000:
-------------

Click on 'Start' --> 'Settings' --> 'Control Panel', doubleclick on the
'System' icon, the 'System Properties' window appears.
Click on the 'Hardware' Tab-Sheet and then click on the 'Device Manager'
button in the middle of the window.

Click on the '+'-sign on the left side of the 'Smart Card Readers' entry
to display all installed smart card readers. Then click on the
'CardMan 3110' entry with the right mouse button and click on the
'Properties' entry in the appearing context menue.

Click on the 'Driver' Tab-Sheet and then click on the Update Driver button.
The 'Upgrade Device Driver Wizard' window appears, click 'Next' to continue.

Select 'Display a list ...' and click 'Next'.
Click on the 'Have Disk' button.
In the 'Install From Disk' window click on the 'Browse' button, go to the folder
where you have unpacked the downloaded file, look for a folder that has a name
according to the operating system you are using, select the '*.inf' file in this
directory and click 'OK'.

Verify that the correct path to the file is shown in the 'Copy manufacturer's
files from:' window and click 'OK'. A message is shown that the wizard is ready
to install the driver for the shown hardware device. Click 'Next'.

A window may appear that the chosen driver is not digitally signed, you will
be asked if you want to continue the installation. Click on the 'Yes' button.

After Windows has copied the driver files a message appears that Windows has
finished installing the software. Click on the 'Finish' button and close all
the windows you don't need.

Now the CardMan 3110 is ready for use, because under Windows 2000 it is not necessary
to reboot the computer.


Windows XP:
-----------

Click on 'Start' --> 'Control Panel', doubleclick on the
'System' icon, the 'System Properties' window appears.
Click on the 'Hardware' Tab-Sheet and then click on the 'Device Manager'
button in the middle of the window.

Click on the '+'-sign on the left side of the 'Smart Card Readers' entry
to display all installed smart card readers. Then click on the
'CardMan 3110' entry with the right mouse button and click on the 'Update
Driver' entry in the appearing context menue.

The 'Hardware Update Wizard' window appears, select 'Display a list ... I can
choose a specific driver' and click 'Next' to continue.

Select 'Choose a specific driver' and click 'Next'. Click on the 'Have Disk'
button.

In the 'Install From Disk' window click on the 'Browse' button,
go to the folder where you have unpacked the downloaded file, look for a folder
that has a name according to the operating system you are using, select the
'*.inf' file in this directory and click 'OK'.

Verify that the correct path to the file is shown in the 'Copy manufacturer's
files from:' window and click 'OK'. Click 'Next'.
A message is shown that the driver didn't pass the Windows Logo Test confirm the
message by clicking on the 'Continue Installation' button.

After Windows has copied the driver files a message appears that the software for
the listed device has been installed. Click on the 'Finish' button and close all
the windows which are not needed anymore.

Now the CardMan 3110 is ready for use, because under Windows XP it is not necessary
to reboot the computer.


Release date: 10/21/2003

-------------------------------- END OF FILE -------------------------------
