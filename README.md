# C-OS-APPS

Downloadable Linux app packs for [C-OS](https://github.com/kawanakatomoya374-pixel/Claude-Workspace). C-OS itself does not contain them: the Launcher's **Linux** tab downloads, verifies and installs a pack with one click.

| Pack | Folder | Download | Installed |
|---|---|---|---|
| Firefox 136 (with an X server, TigerVNC, and the Ubuntu 20.04 libraries they need) | `firefox/` | about 331 MiB | about 956 MiB |

- Each folder holds `linuxpack.manifest` (signed with the C-OS release key) and zlib-compressed chunks `*.pNNNN.bin`. The installer refuses a pack whose signature or any chunk's SHA-256 does not match.
- Served through GitHub Pages: `https://kawanakatomoya374-pixel.github.io/C-OS-APPS/firefox/`.
- Do not edit the files by hand; packs are produced by `tools/linux_pack.py` and `tools/sign_linuxpack.py` in the C-OS repository (see `docs/LINUX_COMPAT.md`, "App packs").

## Licences

The packs redistribute unmodified third-party software under its own licences: Mozilla Firefox (MPL 2.0 and others; Mozilla trademarks apply), TigerVNC/X.Org (GPL/MIT), GNU C Library (LGPL), and the other Ubuntu 20.04 (focal) packages, whose copyright files are in the original packages. Source code is available from the Ubuntu archive (`apt source <package>`) and from mozilla.org.
