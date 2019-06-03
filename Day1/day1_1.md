# Day1 Installation of Ubuntu on Windows  
Original version written by Yoshitake sensei is on suikou information website.

## Confirmation of windows version  
Left-click the Windows logo on the lower left of the screen, enter “winver” and press Enter. Make sure that the version of Windows is 1803 or later.  
![winver](https://github.com/kijiy/image_stock/blob/master/winver.png)  
![after winver](https://github.com/kijiy/image_stock/blob/master/AfterWinver.png)

## Excution of WSL activation  
Right-click the Windows logo at the bottom left of the screen to launch “Windows PowerShell (Administrator)”. Paste the following on PowerShell and execute it to enable WSL. (Perheps computer restart is required)  
Excute the command below and activate the WSL.  
``` bash
    Enable-Windows Optional Feature-Online-Feature Name Microsoft-Windows-Subsystem-Linux
```  
![power shell](https://github.com/kijiy/image_stock/blob/master/winpowshell.png)  
![wsl_on](https://github.com/kijiy/image_stock/blob/master/wsl_on.png)

## Installation of ubuntu  
Launch the Microsoft Store app, search for “Ubuntu 18.04 LTS” and install.  
![ubuntu installation](https://github.com/kijiy/image_stock/blob/master/ubuntu_install.png)

## Settings  
Launch ubuntu and set your name and password.

## Optional  
There is a bug in the current Windows terminal, so please install a terminal software called wsltty.

