---
layout: default
title: Compatibility and Issues
parent: Wine
nav_order: 1
---

# Compatibility and Issues

### 1.21.51 and 1.21.80.01 Previews
Loads using Wine, but users cannot log in due to "Error 1001".

<img src='https://gist.github.com/user-attachments/assets/81a64096-e8cf-4a84-8f63-81de0bb8c0ca' style="height:250px !important;">
<img src='https://gist.github.com/user-attachments/assets/b29d3c92-8283-43f4-b21d-58af8814644e' style="height:250px !important;">
<img src='https://gist.github.com/user-attachments/assets/c3c4e7c1-cfc7-43da-bb67-585d48bfeb19' style="height:250px !important;">

### 1.21.05, 1.21.06 and 1.21.10
Do not launch, no game window opens. No fix known.

### 1.20.12 and 1.20.13
Game opens, but login still doesn't work. Login window shows, and is correct size and in 1.20.13, sometimes displays Chinese characters.

### 1.19.53
Game opens, login window works and is the correct size but doesn't fully load the login page.

### 1.19.51/52 Microsoft.Identity.Client.*.dll`
Game opens, login no longer works due to change to Microsoft Authentication Library (MSAL), using `Microsoft.Identity.Client.*.dll` libraries.

### 1.18.45
MCEE works as it should, Code Builder can crash the game.

<!--

**_Microsoft_** decided to change the way users log in in Minecraft Education (but they didn't for Bedrock, why?), which uses the `Microsoft.Identity.Client.*.dll` libraries, which Wine does not support.
This issue affects the following versions:

| Version         | Status                                                                                      |
|:----------------|:--------------------------------------------------------------------------------------------|
| 1.18.45         | **Not affected**. Works as intended.                                                        |
| 1.19.51/52      | **Affected**. Opens to the login page, where the login window is a blank, unclosable window.|
| 1.19.53         | **Affected**. Window behaves the same as 1.19.51/52, but is the correct size.               |
| 1.20.12         | **Affected**. Window behaves the same as 1.19.53, but with a close button                   |
| 1.20.13         | **Affected**. Same as 1.20.12. The login window displays 4 or 5 Chinese characters.         |
| 1.21.05/1.21.06 | **Doesn't even launch.**                                                                    |
| 1.21.50 Preview | Loads, opens login screen but cannot complete login process, error 1001.                    |

It is _recommended_ that you use [Waydroid](https://mceelinux.github.io/docs/installing/waydroid.html) for later versions.-->