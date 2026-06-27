# 1 Basic Setup Refernce for Gentoo AMD64 Handbook

- KDE Plasma
- GRUB2 + Shim
- OpenRC
- ext4 FileSystem w/ encrypted LUKS2 root

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

## 2.2 Security
- tor
- lynis
- ClamAV
- Clamtk (ClamAV GUI)
- rkhunter
- chkrootkit
- KeePassXC
- Apparmor
- Firewalld

## 2.3 Development Tools & Libraries

- valgrind
- glfw
- glm
- neovim
- ranger
- podman
- podman-compose
- GNU Emacs
- git

## 2.4 Personal Applications

- Librewolf
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
- SimpleX Chat
- Beyond All Reason
- Podman Desktop
- Jami a GNU Package
- Prism Launcher (Minecraft is proprietary, so keep in flatpak for isolation purposes)
- Steam
- Heroic

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
- Zcode
