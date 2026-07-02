# 1 Basic Setup Refernce for Gentoo AMD64 Handbook

- KDE Plasma
- GRUB2 + Shim
- OpenRC
- ext4 FileSystem w/ encrypted LUKS2 root
- networkmanager

# 2. Portage Emerge:

These are trusted free and open source packages installed directly onto the host.

## 2.1 Gentoo tools

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
- gentoolkit

## 2.2 Security
- tor (configure w/ meek bridge)
- proxychains
- lynis
- ClamAV (**Author's NOTE:** don't analyze on open in ~/Documents and ~/Music)
- Clamtk (ClamAV GUI)
- rkhunter
- chkrootkit
- KeePassXC
- Apparmor
- Firewalld (use **drop** zone)
- exiftool
- networkmanager-openvpn (for .ovpn configs)

## 2.3 Development Tools & Libraries

- valgrind
- glfw
- glm
- mg
- ranger
- podman
- podman-compose
- GNU Emacs (requires libvterm package)
- git (use Tor)

## 2.4 Personal Applications

- GNU Icecat (use Tor)
- LibreOffice
- Dolphin
- Kitty
- Ark
- Elisa
- Kdenlive
- Filelight
- Flatpak
- links
- VLC Media Player
- Wireshark
- Btop
- qBittorrent
- Godot
- Blender
- GIMP
- feh

# 3. Flatpak (Flathub)

Some free and open source applications that are not available through Portage, so they're installed on here for better package management (appimages are only used if the flathub option is unverified or problemactic).

**NOTE:** All flathub packages that are installed are distributed by verified authors. Flathub packages that are provided by unverified authors are prohibited from installation. This is to avoid malware and bad code form running on your personal machines.

- Flatseal
- SimpleX Chat (use Tor)
- Podman Desktop
- Jami a GNU Package
- FreeTube (use Tor)

# 4. Appimages (+ others ex. .jar, .sh, etc)

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

# 5. Games

- Beyond All Reason (flatpak via flathub)
- sauerbraten (portage)
- supertuxkart (portage)
