# Basic Setup Refernce for Gentoo AMD64 Handbook

- KDE Plasma
- GRUB2 + Shim
- OpenRC
- ext4 FileSystem w/ encrypted LUKS2 root

# Portage Emerge:

These are trusted free and open source packages installed directly onto the host.

### Gentoo tools

- sysklogd
- cronie
- mlocate
- bash-completion
- chrony
- e2fsprogs
- cryptsetup
- io-scheduler-rules
- doas
- sys-fs/fuse:0 (for proper appimage functionality)
- openjdk:21 (Ghidra requires Java 21 runtime)

### Personal Applications

- Librewolf
- LibreOffice
- Dolphin
- Kitty
- Konsole
- KeePassXC
- Mg
- Mc
- Podman
- Podman-compose
- GNU Emacs
- Git
- Ark
- Elisa
- Kdenlive
- Filelight
- Firewalld
- Flatpak
- Apparmor
- links
- VLC Media Player
- Wireshark
- Btop
- qBittorrent
- Godot
- Blender
- Tor
- GIMP

# Flatpak (Flathub)

Less trusted applications like proprietary programs are installed via flatpak for isolation and security. Also, some free and open source applications that are not available through Portage, are installed on here for better package management (appimages are only used if the flathub option is unverified).

**NOTE:** All flathub packages are installed are distributed by verified authors. Flathub packages that are provided by unverified authors are prohibited from installation as the maintianer of this configuraiton. This is to avoid malware and bad code form running on your personal machines.

**NOTE-2:** Heroic is on Portage and is free and open source. However, since it installs proprietary games, it is untrusted by default, and placed inside of flatpak.

- Flatseal
- SimpleX Chat
- Heroic
- Steam
- Beyond All Reason
- Podman Desktop
- Jami a GNU Package
- Prism Launcher
- Sober

# Appimages (+ others ex. .jar, .sh, etc)

Appimages and other forms of executables are an unpreferred method of installation, due to the requirements of manual updating and file handling. But, when it is the only or best option, it is used.

**NOTE:** Tor Browser is not installed via flatpak, even though the authors are verified. This is for personal reasons. It is completely your choice to do otherwise.

- ExifCleaner
- Kiwix Reader
- debloat (https://github.com/Squiblydoo/debloat)
- Ghidra
- llama.cpp
- Logisim Evolution
- Tor Browser
- Ventoy
