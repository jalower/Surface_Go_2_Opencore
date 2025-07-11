![OpenCore logo](https://github.com/acidanthera/OpenCorePkg/raw/master/Docs/Logos/OpenCore_with_text_Small.png)

# Surface-Go-2-OpenCore
After a long long period of trial and error, I finally able to boot into macOS on this Surface Go 2. 
The **Pentium Gold Y4425 Microsoft Surface Go 2 (8gb / 64gb eMMC model)**  thanks to [Acidanthera's OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg) and [atisDu's OpenCore files](https://github.com/atisDu/Surface_go_opencore) The OpenCore version of this repository is 1.0.5! So consider updating it and the kexts from Acidanthera's  repos.
The latest macOS Version running is Monterey 12.7.4 

For Core m3-8100Y Microsoft Surface Go 2 please visit [jlempen's OpenCore files](https://github.com/jlempen/Surface-Go-2-OpenCore).

# Issues pending to fix
Camera not working

It is able to turn on Bluetooth now, able to conncet to Airpods Pro 2, but the connection is unstable.

Able to pair with my iPhone, but unable to connet due to the error of " (Device) is unsupported"

Screen mirroring

Brightness control

Trackpad scrolling

# What is confirmed to be working from me
Sleep is working

Battery is fixed and is able to show in menu bar

The icons and graphics for booting screen is enabled and working.

Audio is working

iServices are working for me (e.g. iCloud, iMessages....)

DRM is fixed

The wifi card (Intel AX200) works in macOS

# Issues from atisDU that are unsure
macOS only works with eMMC storage if you use the [EmeraldSDHC kext](https://github.com/acidanthera/EmeraldSDHC) which as of writing this (11.07.2024 and the EmeraldSDHC kext version 0.1.2) does not seem to work with the SD host controller found in
the Surface Go (4gb / eMMC). Even legacy ATA controller kexts dont work. Which means that internal storage won't work.

# What is confirmed to be working from atisDU
The realtek SD card reader works

The touch (keyboard) cover and trackpad works with the [BigSurface kext](https://github.com/Xiashangning/BigSurface), comprising of modified Voodoo input kexts.

# How to make it boot
Install the image through macrecovery according to the [Dortania OpenCore install guide](https://dortania.github.io/OpenCore-Install-Guide/) 
The laptop is in the platform of kaby lake cpu's or simply use the provided config.plist, but change the PlatformInfo SMBIOS accordingly, for which a guide can be found in 
the opencore install guide.

Put the EFI folder in the root of the usb drive and download the mac os Monterey recovery folder by following the OpenCore install guide.


## Disclaimer
This repository is neither a howto nor an installation manual. Using these files requires at least basic knowledge of [Acidanthera's OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg), ACPI, UEFI and the art of hackintoshing in general. I recommend reading the excellent [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide), as well as all its linked resources.
