# Introduction

This is my personal Gentoo Portage Configuration for my Dell Inspiron 15 3535 laptop. It is designed around freedom, accepting @FREE licenses. It may not be a pure FSF freedom configuration, since the linux-firmware package requires non-free firmware for my laptop to work properly. The non-free firmware in question is related to the AX210 wifi PCIe card and an AMD Micro Controller (Barcelo) for displaying content on the screen. Due to this, using Linux-Libre breaks GUI and essential Desktop features.

As far as freedom, there are some expections which I have made, being sure to read their related licenses (ex. Steam for games). Such propiertary programs are install via flatpak from flathub for isolation and host safety. I do make sure to check that the flathub packages are from the original authors and are verified to prevent malware from being installed.

I do use some AppImages (listed in My_Apps_To_Install.txt), but I do make use of flatpak when a verified package of it is avialable on flathub, in favor of isolation, security, and convenience (ex. updates are handled automatically by flatpak instead of manually with AppImages).

The provided My_Apps_To_Install.txt file provides a list of most of the packages/apps which I use personally on my machine (ex. LibreOffice). Still supporting free and open source values.

Other configuration files which I use are found in other repos on my Github profile. Links will be provided at the end of this README.

# Installation

```bash
cd /etc/
sudo rm portage
sudo git clone https://github.com/CyberAlstor/CyberAlstor_Gentoo_Portage_Config_x86-64-v3.git portage
```

# Other Config files I use:

- https://github.com/CyberAlstor/CyberAlstor-s_GNU_Emacs_Config
