# C-OS-APPS

Downloadable Linux app packs for [C-OS](https://github.com/kawanakatomoya374-pixel/Claude-Workspace). C-OS itself does not contain them: the Launcher's **Linux** tab downloads, verifies and installs a pack with one click.

| Pack | Folder | Download | Installed |
|---|---|---|---|
| Firefox 136 (with an X server, TigerVNC, and the Ubuntu 20.04 libraries they need) | `firefox/` | about 331 MiB | about 956 MiB |

- Each folder holds `linuxpack.manifest` (signed with the C-OS release key) and zlib-compressed chunks `*.pNNNN.bin`. The installer refuses a pack whose signature or any chunk's SHA-256 does not match.
- Served through GitHub Pages: `https://kawanakatomoya374-pixel.github.io/C-OS-APPS/firefox/`.
- Do not edit the files by hand; packs are produced by `tools/linux_pack.py` and `tools/sign_linuxpack.py` in the C-OS repository (see `docs/LINUX_COMPAT.md`, "App packs").

## C-OS Apps (`apps/`)

The store app **C-OS Apps** reads `apps/catalog.manifest` (signed with the C-OS release key) and installs the packs next to it. Each app folder has `linuxpack.manifest`, `icon.png` and chunks; the catalog names every icon's SHA-256.

| App | Folder | Download | Source / licence |
|---|---|---|---|
| mc-classic-c (Minecraft Classic 0.0.11a to 0.30 rewritten in C) | `apps/minecraft/` | about 11 MiB | GPL-3.0, github.com/degradka/mc-classic-c; the C-OS port is in the C-OS repository (`userland/programs/mcclassic`) |
| Sprint examples and icon (the Sprint interpreter is part of C-OS) | `apps/sprint/` | a few KiB | github.com/kawanakatomoya374-pixel/Sprint; the C-OS port is `ports/sprint` in the C-OS repository |
| PSXFunkin (the game data is downloaded on the device from the PSXFunkin repository, not from here) | `apps/psxfunkin/` | about 0.9 MiB | MPL-2.0, github.com/IgorSou3000/PSXFunkin; the C-OS port is `ports/psxfunkin` in the C-OS repository |

## Licences

The packs redistribute unmodified third-party software under its own licences: Mozilla Firefox (MPL 2.0 and others; Mozilla trademarks apply), TigerVNC/X.Org (GPL/MIT), GNU C Library (LGPL), and the other Ubuntu 20.04 (focal) packages, whose copyright files are in the original packages. Source code is available from the Ubuntu archive (`apt source <package>`) and from mozilla.org.
