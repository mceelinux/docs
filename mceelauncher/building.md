---
layout: default
title: Building
parent: MCEELauncher
nav_order: 1
---

# Building MCEELauncher


### Clone the repository
```bash
git clone https://github.com/mceelinux/mceelauncher mceelauncher
cd mceelauncher
```

### Make `buildmgr` executable
```bash
chmod +x buildmgr
```

### Run clean and build
```bash
./buildmgr clean
./buildmgr build
```

### Run `mceelauncher`
```bash
./build/mcpelauncher-client/mcpelauncher-client --help
```

<!-- 
Build MCEELauncher by following the MCPELauncher instructions, but in the game launcher files, replace <code>libc-shim</code> and <code>minecraft-imported-symbols</code> with the ones on our GitHub organizaiton.
-->