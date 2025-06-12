---
layout: default
title: Wine
parent: Installing MCEE
nav_order: 1
has_children: true
---

# Wine Method

## IMPORTANT
See [here](https://mceelinux.github.io/docs/installing/wine/compatibility.html) for details on Minecraft Education version compatibility in Wine.

----
## Downloads
- [Minecraft Education (Extracted from the installer)](https://github.com/techguy16/files-for-projects/releases/download/me/ME-1.18.45-Extracted.zip)
- [Visual C++ Redist 2017, x86](https://aka.ms/vs/15/release/vc_redist.x86.exe)
- ~~[Microsoft Data Access Components 2.8 SDK](https://download.microsoft.com/download/9/a/1/9a1256c9-d301-4fdc-93b9-370c5b2f9827/mdac28sdk.msi)~~ (No longer needed)
- [dxvk](https://github.com/doitsujin/dxvk/releases/download/v2.6.2/dxvk-2.6.2.tar.gz)


## Steps
1. #### Add the Wine repository to your system
   
   Ubuntu:
   ```bash
   sudo dpkg --add-architecture i386
   sudo mkdir -pm755 /etc/apt/keyrings
   sudo wget -O /etc/apt/keyrings/winehq-archive.key https://dl.winehq.org/wine-builds/winehq.key
   sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/$(lsb_release -cs)/winehq-$(lsb_release -cs).sources
   sudo apt update
   ```
   (Linux Mint users will need to replace `$(lsb_release -cs)` with the version of Ubuntu their version is based on, for example: 20.2 Uma -> `focal`)


2. #### Install Wine Stable + winbind
   Install Wine Stable using the following command
   ```bash
   sudo apt install winehq-stable wine-stable wine-stable-i386 wine-stable-amd64 winbind
   ```


3. #### Open Wine Configuration
   Type `winecfg` to open Wine's configuration. If any dialogs pop up saying that something needs installing, press 'Install'.
   Once `winecfg` has opened, select the drop down box labeled 'Windows Version: ' and select Windows 7.

   
4. #### Install dxvk
   To install dxvk, run the following commands:
   ```bash
   wget https://github.com/doitsujin/dxvk/releases/download/v2.6.2/dxvk-2.6.2.tar.gz
   tar -zxvf dxvk-*.tar.gz
   mv dxvk-*/x32/* $WINEPREFIX/drive_c/?indows/syswow64
   mv dxvk-*/x64/* $WINEPREFIX/drive_c/?indows/system32
   rm -r dxvk-*
   ```
   
   
5. #### Extract Minecraft Education
   Type `unzip ME-1.18.45-Extracted.zip` to extract the files.
   
  
6. #### Install Visual C++ Redist 2017
   Open your file manager and right click on each executable and open it with *Wine Windows Program Loader*

  
7. #### Launch Minecraft Education
   Navigate to the 'ME-1.18.45-Extracted' directory using `cd ME-1.18.45-Extracted`
   
   Then launch Minecraft Education using `wine Minecraft.Windows.exe`

  
# Thanks to
- WineHQ Community
- Unix StackExchange