---
layout: default
title: Waydroid
parent: Installing MCEE
nav_order: 1
---

# Waydroid Method

{:toc}

1. #### Add Waydroid Repository

   Add the Waydroid repository to your system (**Debian** and **Ubuntu**-based distros)
   ```bash
   grep -E 'Ubuntu|Debian|Pop|Mint|Elementary|Zorin' /etc/os-release && sudo apt update && sudo apt install curl ca-certificates -y && curl -s https://repo.waydro.id | sudo bash
   ```
   
2. #### Install Waydroid

   ```bash
   sudo (dnf install waydroid || apt install waydroid -y || yay -S waydroid || paru -S waydroid)
   ```
   
3. #### Install GApps build of Android

   ```bash
   sudo waydroid init -s GAPPS
   ```
   
4. #### Google Play Services Registration

   Open the Waydroid Shell by typing:
   ```bash
   sudo waydroid shell
   ```
   
   You should see a prompt that resembles `:/ #`. At that prompt, paste the following command:
   ```bash
   ANDROID_RUNTIME_ROOT=/apex/com.android.runtime ANDROID_DATA=/data ANDROID_TZDATA_ROOT=/apex/com.android.tzdata ANDROID_I18N_ROOT=/apex/com.android.i18n sqlite3 /data/data/com.google.android.gsf/databases/gservices.db "select * from main where name = \"android_id\";"
   ```
   
   Copy the string of numbers after `android|`, then type `exit` into the Waydroid shell.
   
   Paste the copied string of numbers into the textbox of the following website, and then press Register:
   https://www.google.com/android/uncertified
   Note: _You will need to be logged in for this to work_
   
   Open the terminal again, and then type:
   ```bash
   sudo waydroid session stop
   ```
   
   Then open Waydroid again.
   
5. #### Log in to Google Play

   Once Waydroid has booted again, open Google Play and sign in like you would on an Android phone. Ignore the on-screen keyboard for now.


6. #### Download and Install Minecraft Education

   Once you have logged in to Google Play, search for `Minecraft Education` or `com.mojang.minecraftedu`. Select the first option, and click install.


7. #### Open Minecraft Education

   Once it has installed, go to your apps launcher and find `Minecraft Education`. Then click it. It should open in the Waydroid environment, and ready to sign in.

----
## Thanks to
- Waydroid's docs