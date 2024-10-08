# Gigabyte-X570-Hackintosh
 Run macOS with your AMD X570-based PC
![Screenshot 2024-07-18 at 9.30.46 PM](assets/Screenshot%202024-07-18%20at%209.30.46%E2%80%AFPM.png)

## My Hardware  
Components | Specifications  
------------ | -------------  
**Motherboard** | Gigabyte X570 Gaming X
**CPU** | AMD Ryzen 5 5600 Hexacore
**Ethernet** | Built-in RTL 8111
**Graphics** | AMD RX6800 XT 16GB
**RAM** | 8+32GB DDR4 3200Mhz  
**Storage** | 512GB WD SN580 NVME SSD for fun
**Storage** | 1.92TB Sandisk CloudSpeed SSD for hackintosh
**Storage** | 960GB Samsung PM983a NVME SSD for Windows
**Storage** | 3.0TB Hitachi HDD for Porn
**macOS** | 11.4-14.6

## Warning
 **This is made for 6 core processors like R5 5600, if you have 8/12/16 cores, please change config.plist.**

 **Please regenerate PlatformInfo before installation.**

 **Resize Bar & Above 4G Decoding have been enabled. If you don't want to enable them, please change ResizeAppleGPUBars to -1.**

 **If you have a RDNA2-based GPU with no native support, such as RX6700/XT/XL, RX6750GRE, RX6950XT, RX6400. Please replace WhateverGreen.kext with NootRX.kext.** 

 **If you're using an APU with built-in Vega iGPU enabled, please add NootRed.kext.**


## Installation Guide

1. **Prepare macOS Installer**
   - Download macOS from the App Store.
   - Use the createinstallmedia command to create a bootable USB installer.

2. **BIOS Settings**
   - Disable Secure Boot.
   - Disable Fast Boot.
   - Set Initial Display Output to PCIe Slot.
   - SATA AHCI

3. **Install macOS**
   - Boot from the USB installer.
   - Follow the on-screen instructions to install macOS.
   - Post-installation: Install OpenCore to the macOS drive.

## Post-Installation

1. **Drivers/Kexts**
   - **Ethernet:** RTL8111.kext for RTL 8111 Ethernet.
   - **Audio:** AppleALC.kext.
   - **GPU:** Supported natively, no additional kexts required.
   - **Miscellaneous:** Lilu.kext, VirtualSMC.kext, WhateverGreen.kext.

2. **Issues and Workarounds**
   - **Wi-Fi and Bluetooth:** Broadcom-based Wi-Fi and Bluetooth functionalities like AirDrop, Handoff, Sidecar, and AirPlay are not available.
   - **Apple Watch Unlock:** Not functional.
   - **Startup Disk:** Switching the startup disk in macOS is not effective. Use BIOS boot menu to switch disks.

3. **Additional Notes**
   - Keep your kexts and bootloader up to date.
   - Regularly backup your config.plist and EFI folder.

## macOS Versions Tested

- macOS Big Sur 11.4
- macOS Monterey 12.x
- macOS Ventura 13.x
- macOS Sonoma 14.0 - 14.5

## Resources

- [OpenCore Vanilla Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Hackintosh Forum](https://www.tonymacx86.com/)
- [RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X)
