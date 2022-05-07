Default install: Apache 2.4.51 - PHP 5.6.40/7.3.33/7.4.26/8.0.13/8.1.0 - MySQL 5.7.36[|8.0.27 for 64 bit] - MariaDB 10.5.12|10.6.5
PhpMyAdmin 4.9.7/5.1.1 - Adminer 4.8.1 - PhpSysInfo 3.3.3
As an option : PHP 7.0.33/7.1.33/7.2.34

--- Installation of Wampserver ---
Wampserver requires a disk or formatted NTFS partition. Does not support FAT32 or exFAT
BEFORE proceeding with the installation of Wampserver, you must ensure that certain elements are installed on your system, otherwise Wampserver will absolutely not run, and in addition, the installation will be faulty and you need to remove Wampserver BEFORE installing the elements that were missing.
Make sure you are "up to date" in the redistributable packages VC9, VC10, VC11, VC13, VC14, VC15, VS16, VS17
See --- Visual C++ Packages below.
--- Do not install Wampserver OVER an existing version, follow the advice:
Install a new version of Wampserver: http://forum.wampserver.com/read.php?2,123606
If you install Wampserver over an existing version, not only it will not work, but you risk losing your existing databases.

--- Install Wampserver in a folder at the root of a disk, for example C:\wamp or D:\wamp. Take an installation path that does not include spaces or diacritics; Therefore, no installation in c:\Program Files\ or C:\Program Files (x86\

--- Install Wampserver "as an administrator" i.e Right-Click on installer file then Run as an administrator.

We must BEFORE installing, disable or close some applications:
- Close Skype or force not to use port 80
Item No. 04 of the Wampserver TROUBLESHOOTING TIPS http://forum.wampserver.com/read.php?2,134915
- Disable IIS
Item No. 08 of the WampserverTROUBLESHOOTING TIPS http://forum.wampserver.com/read.php?2,134915

- Visual C++ Packages
The MSVC runtime libraries VC9 to VS16 are required for Wampserver 3.0
-- VC9 Packages (Visual C++ 2008 SP1) - To use PHP 5.3 or 5.4
Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)
http://www.microsoft.com/en-us/download/details.aspx?id=5582'>
Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)
http://www.microsoft.com/en-us/download/details.aspx?id=2092
-- VC10 Packages (Visual C++ 2010 SP1)
Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)
http://www.microsoft.com/en-us/download/details.aspx?id=8328
Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)
http://www.microsoft.com/en-us/download/details.aspx?id=13523
-- VC11 Packages (Visual C++ 2012 Update 4)
The two files VSU4\\vcredist_x86.exe and VSU4\\vcredist_x64.exe to be download are on the same page:
Visual C++ Redistributable for Visual Studio 2012 Update 4
http://www.microsoft.com/en-us/download/details.aspx?id=30679
-- VC13 Packages] (Visual C++ 2013[)
The two files VSU4\\vcredist_x86.exe and VSU4\\vcredist_x64.exe to be download are on the same page:
Visual C++ Redistributable Packages for Visual Studio 2013
https://www.microsoft.com/en-us/download/details.aspx?id=40784
-- VC14 Packages (Visual C++ 2015) Replaced by VC15
-- VC15 Redistribuable (Visual C++ 2017) Replaced by VS16
-- VCS6 Redistribuable (Visual C++ 2015-2019) Replaced by VS 17
Visual C++ Redistributable Packages for Visual Studio 2015-2022 x86
https://aka.ms/vs/17/release/VC_redist.x86.exe
Visual C++ Redistributable Packages for Visual Studio 2015-2022 x64
https://aka.ms/vs/17/release/VC_redist.x64.exe
VC2015-2022 (VS17) is backward compatible to VC14, VC15 and VS16. That means, a VC14, VC15 or VS16 module can be used inside a VS17 binary. Because this compatibility the version number of the Redistributable is 14.3x.xx and after you install the Redistributable VC2015-2022, the Redistributable packages VC2015 (VC14), VC2017 (VC15) or VS16 are eventually deleted but you can still use VC14, VC15 and VS16.

If you have a 64-bit Windows, you must install both 32 and 64bit versions, even if you do not use Wampserver 64 bit.
This is item number 20 of TROUBLESHOOTING TIPS http://forum.wampserver.com/read.php?2,134915
To check if the required VC packages are installed properly, you can use the program 'Checks VC++ packages installed' available in section Tools of http://wampserver.aviatechno.net/ and then download and install the missing packages. All VC++ packages can be downloaded from the Visual C++ Redistribuable Packages section of the same page.
If these prerequisites are not in place, Press the Cancel button to cancel the installation, then apply the prerequisites and restart the installation.

------ After Installation ------
--- PhpMyAdmin
When starting phpMyAdmin, you will be asked for a user name and password.
After installing Wampserver 3, the default username is "root" (without quotes) and there is no password, which means that you must leave the form Password box empty.
There will be a warning:
You are connected as 'root' with no password, which corresponds to the default MySQL privileged account. Your MySQL server is running with this default, is open to intrusion, and you really should fix this security hole by setting a password for user 'root'.
This is not a problem as long as access to Phpmyadmin remain locally.
However, some web applications or CMS asking that the MySQL user has a password. In which case, you will create a user with password via the PhpMyAdmin Accounts Users tab.

--- Using the menus and submenus of Wampmanager
Do not use the keyboard to navigate through the menus and submenus of Wampmanager icon.

--- For questions regarding Wampserver 3
Please use the specific English forum http://forum.wampserver.com/list.php?2
(Or French forum http://forum.wampserver.com/list.php?1 )
Do not use an existing discussion, but create your own thread: New Topic (French : Nouvelle discussion) after having read  http://forum.wampserver.com/read.php?2,129067 READ BEFORE YOU ASK A QUESTION in this forum.

Nota : It is possible to do silent install by command line 'as an administrator':
wampserver3.2.0_x86.exe /DIR="C:\wamp" /VERYSILENT /SUPPRESSMSGBOXES
or
wampserver3.2.0_x64.exe /DIR="C:\wamp" /VERYSILENT /SUPPRESSMSGBOXES
Yoy may replace install dir.