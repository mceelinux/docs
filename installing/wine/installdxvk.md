---
layout: default
title: Install dxvk
parent: Wine
nav_order: 2
---

# Install dxvk

To install dxvk, run the following commands:

   ```bash
   wget https://github.com/doitsujin/dxvk/releases/download/v2.6.2/dxvk-2.6.2.tar.gz
   tar -zxvf dxvk-*.tar.gz
   mv dxvk-*/x32/* $WINEPREFIX/drive_c/?indows/syswow64
   mv dxvk-*/x64/* $WINEPREFIX/drive_c/?indows/system32
   rm -r dxvk-*
   ```