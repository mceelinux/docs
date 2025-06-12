---
layout: default
title: Compatibility
parent: Wine
nav_order: 1
---

# Compatibility

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

It is _recommended_ that you use [Waydroid](https://mceelinux.github.io/docs/installing/waydroid.html) for later versions.