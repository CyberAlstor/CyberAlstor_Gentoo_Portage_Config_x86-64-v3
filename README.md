# About the Author:

I am a free software advocate. I've more recently, at the time of writing this, have started taking my software freedom much more seriously.
I've uninstalled or completely avoided proprietary video games, applications, and even system tools that violate my freedoms. It took me a 
long while to get to this stage of freedom for myself, since giving up proprietary convenience was difficult. So don't feel bad that you 
couldn't do it yourself yet, it takes time to find freedom.

My journey took me a lot of time. It all started when I got my first laptop, the Dell Inspiron 15 3535, which I am still using at the 
time of writing this. I immediately went striaght to Arch GNU/Linux as my first Distro. Which was clearly ambitious from what I already
knew about GNU/Linux. Being successful on installing Arch Linux, I've used it a couple of months, until I switched to CachyOS, then trying
a Debian-based system like ParrotOS, then back to CachyOS for a short while (all of these were used for some months of time). It was only
until I started using Gentoo I started to take user freedom very seriously. It didn't start that way, but Gentoo already gave me an incentive 
to have a purely open source ecosystem. It started with the desire to compile as much as I can to promote control at the package level. 
However, as I have learned more about the Free Software Foundation, the GNU Project, and listening to Richard Stallman's arguments, had 
I started taking my software freedom more seriously, and even my freedoms as a US citizen more seriously.

When using Gentoo, it was difficult striping out every proprietary element there was from my machine. Mostly due to conveniences that
came with proprietary programs, especially extremes like LibreJS that demand a rework of your entire browsing experience. So I had to 
start small, starting with office programs, stripping out proprietary elements from my Gentoo installation (using the 100% Libre guide
from the official Gentoo wiki), quiting the majority of video games I had once played, etc. It's small steps to a better freedom. I 
even had to change my email from Gmail, to ProtonMail, and then finially to a FSF approved email, to respect my freedoms more (I'm still
migrating to the new email, so ProtonMail is still in my life). I unfortunately had to make "a deal with the devil" as describe by the 
FSF when it came to the Kernel and my BIOS, since Linux-Libre is incompatible with my laptop, and that the BIOS on my laptop is stuck
with the stock BIOS (no avialable free alternative).

The hardest step was with the browser. I first used Chrome on a Chromebook that was provided by my school, and then by my parents when
I had started homeschool. I then started using Edge from a Windows 11 system on a family desktop computer, which we all chipped in on.
This wasn't an improvement on freedom, but a functinoal improvement at the least. When I had bought my first laptop for $400 being on
sale (original price was $600), I had installed Linux first thing. I started making use of a mix of Librewolf and Brave. I used Librewolf
for personal use over the summer, but when school had started, I used Brave, since it was the only thing private and compatible with my
online school. After I had graduated, I made Librewolf my default and exclusive browser. I also refused to use DRM through Librewolf.
I then installed the Tor Browser to help with certian tasks, though I had barely used it. It was only recently (7/2/2026) that I had
started using GNU Icecat and the Tor Browser exclusively, giving Librewolf my finale wave goodbye, and experiencing the welcoming
embrace of freedom.

# How I do my Computing:

I use my Dell Inspiron 15 3535 for all my computing. I do plan to make a switch to a laptop that fully respects my freedoms in the
future.

I use GNU Icecat for general browsing and the Tor Browser for incompatible uses of GNU Icecat. I only run non-free JS through the Tor
Browser using default settings, so that I can still access non-free JS websites, while still dodging survielance and tracking. I also 
make use of Tor for every connection, with little execptions. When possible, I route all application level traffic through Tor, like SimpleX, GNU 
Icecat, Git, Freetube, etc. An execption is Jami, since performace is more important than ultimate privacy.

I work mostly through GNU Emacs using my own configuration. I find that Emacs is the best editor for me, being extremely customizible, 
telemetry-free, and freedom respecting. Outside of that, for official documents or files that need to be understood in a workplace, I 
have LibreOffice, I do refuse to use proprietary fonts, using FOSS fonts exclusively that still remain professional. Unfortunately, 
when dealing with proprietary tools for work, I won't use them unless they provide me a company-issued computer that stays at the
workplace. I find this appropiate since it enables me to work, while at the same time, repesting my freedom at home and public spaces.

# Introduction to Portage Config

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
