# Introduction

This is my personal Gentoo Portage Configuration for my Dell Inspiron 15 3535 laptop. It is designed around freedom, accepting @FREE licenses. It may not be a pure FSF freedom configuration, since the linux-firmware package requires non-free firmware for my laptop to work properly. The non-free firmware in question is related to the AX210 wifi PCIe card and an AMD Micro Controller (Barcelo) for displaying content on the screen. Due to this, using Linux-Libre breaks GUI and essential Desktop features.

As far as freedom, there are some exceptions which I have made, being sure to read their related licenses (ex. Steam for games). Such propiertary programs are install via flatpak from flathub for isolation and host safety. I do make sure to check that the flathub packages are from the original authors and are verified to prevent malware from being installed.

I do use some AppImages, but I do make use of flatpak when a verified package of it is avialable on flathub, in favor of isolation, security, and convenience (ex. updates are handled automatically by flatpak instead of manually with AppImages).

Other configuration files which I use are found in other repos on my Github profile. Links will be provided at the end of this README.

# Notes on Secureboot

Secureboot key paths are provided inside of make.conf. Unfortunately, I can't do Secureboot support for you on your own machine.

I use Shim as a pre-loader for GRUB2. Shim is pre-signed with microsoft certificates, being a safe and effective option for enabling Secureboot, unlike registering keys into the UEFI firmware directly with sbctl or other methods of custom key registration.

**NOTE:** Before trying to get Secureboot working on your machine, you MUST check if it has the Secureboot option in the BIOS setup menu. Also check if you are on UEFI firmware (https://wiki.archlinux.org/title/Installation_guide, step 1.6):

To verify the boot mode, check the UEFI bitness:

```bash
sudo cat /sys/firmware/efi/fw_platform_size
```

- If the command returns 64, the system is booted in UEFI mode and has a 64-bit x64 UEFI.
- If the command returns 32, the system is booted in UEFI mode and has a 32-bit IA32 UEFI. While this is supported, it will limit the boot loader choice to those that support mixed mode booting.
- If it returns No such file or directory, the system may be booted in BIOS (or CSM) mode.

If the system did not boot in the mode you desired (UEFI vs BIOS), refer to your motherboard's manual. 

### Gentoo Wiki Docs for Secureboot

I highly suggest reading the optional Secureboot sections in the Gentoo AMD64 Handbook during the Gentoo installation process to get Secureboot working.

https://wiki.gentoo.org/wiki/Handbook:AMD64

# Installation

```bash
cd /etc/
sudo rm portage
sudo git clone https://github.com/CyberAlstor/CyberAlstor_Gentoo_Portage_Config_x86-64-v3.git portage
```

After installing it, be sure to read [Gentoo_Setup_And_Apps.md](./Gentoo_Setup_And_Apps.md) for further installation and configuration instructions. It will tell you what tools (ex. bootloader, filesystem, etc) and apps I suggest installing. However, it is your choice to install whatever you want. This is what works for me.

# Other Config files I use:

- https://github.com/CyberAlstor/CyberAlstor-s_GNU_Emacs_Config
