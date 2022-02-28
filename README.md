# Hp 250 G6 (Skylake) OpenCore EFI [Monterey]
![Hp Latpop Snapshot](https://raw.githubusercontent.com/IsraPerez98/OpenCore-HP250G6-Skylake/main/Docs/HP-Image.png)

### Built using [OpenCore 0.7.8](https://github.com/acidanthera/OpenCorePkg/releases)

### **If you're going to use this EFI remember to generate your own SMBIOS Serials using [Install Guide - PlatformInfo](https://dortania.github.io/OpenCore-Install-Guide/config.plist/skylake.html#platforminfo) with MacBookPro14,1**

This repo contains information for getting macOS 12 Monterey working on a HP 250 G6 Skylake (i3-6006u) Laptop

In case you haven't made any modifications to the laptop or have done any upgrades, I suggest buying a SATA SSD as it will really help performance.

Also I would recommend you to check your current WLAN + BT card, only models with Intel will work with this configuration, check the wiki [Supported/Unsupported Chipsets](https://dortania.github.io/Wireless-Buyers-Guide/unsupported.html)

As of now I think the EFI is almost complete except for a few things.

**Enhancements and improvements are always welcome**

### Currently Running:


| Component     | Version      |
| ------------- | ------------ |
| macOS version | 12.2.1 |
| OpenCore      | 0.7.8        |

## Hardware Info

| Component | Model                                   |
| --------- | --------------------------------------- |
| CPU                           | Intel® Core™ i3-6006U (2 GHz, 3 MB cache, 2 cores)                    |
| Memory                        | 8 GB DDR4-2133 SDRAM (1 x 8 GB)                                       |
| Video Graphics [`DGPU`]       | AMD Radeon™ 520 Graphics (2 GB DDR3 dedicated)                        |
| Storage                       | Toshiba 1 TB 5400 rpm SATA                                            |
| Display                       | 39,62 cm (15,6 in) diagonal FHD SVA anti-glare WLED-backlit (1366 x 768) |
| GPU [`iGPU`]                  | Intel HD 520                                                          |
| Camera                        | HP TrueVision HD Camera with integrated digital microphone            |
| WLAN                          | Intel Dual Band Wireless-AC 3168 802.11ac (1x1) Wi-Fi and Bluetooth 4.2          |
| Touchpad                      | Synaptics SMBus Touchpad with multi-touch gesture support             |
| Battery Type                  | 4-cell, 41 Wh Li-ion                                                  |

## Kexts

| Kext                   | Version     | Remark                                   |
| ---------------------- | ----------- | ---------------------------------------- |
| AirportItlwm           | 2.1.0       | Fixes Intel Wifi                         |
| AppleALC               | 1.6.9       | Fixes onboard audio                      |
| BlueToolFixup          | 2.6.1       | Fixes Bluetooth on Monterey              |
| BrightnessKeys         | 1.0.2       | Fixes brightness keys                    |
| IntelBluetoothFirmware | 2.1.0       | Fixes Intel Bluetooth                    |
| Lilu                   | 1.6.0       | Kext patcher                             |
| RealtekRTL8111         | 2.4.2       | Ethernet                                 |
| SMCBatteryManager      | 1.2.8       | Battery indicator                        |
| SMCProcessor           | 1.2.8       | CPU temp monitoring                      |
| SMCSuperIO             | 1.2.8       | Monitor fan speed, not working           |
| VirtualSMC             | 1.2.8       | SMC chip emulation                       |
| VoodooPS2Controller    | 2.2.7       | Enable keyboard/Trackpad                 |
| WhateverGreen          | 1.5.7       | Graphics                                 |

## ACPI patches


| Patch                 | Remark                         |
| --------------------- | ------------------------------ |
| SSDT-PLUG-DRTNIA      | x86 plugin injection fix       |
| SSDT-PNLF             | Backlight fix                  |
| SSDT-EC-USBX-LAPTOP   | USBX patch                     |
| SSDT-XOSI             | Trackpad fix                   |
## Status

### Working

- [x] Wifi
- [x] Bluetooth
- [x] Keyboard
- [x] Trackpad with gestures and physical buttons
- [x] Audio
- [x] Ethernet
- [x] iCloud services - iMessage, FaceTime, AppStore
- [x] GPU acceleration
- [x] Camera
- [x] Microphone
- [x] Sleep/wake
- [x] HDMI video (Audio through HDMI does not work)
- [x] DRM content playback (Netflix)
- [x] Linux dualboot using OpenCore
- [x] Brightness config + brightness keys

### Not Working at the moment

- [ ] GPU acceleration with dedicated Radeon card (obviously)

### Not Tested
- [ ] Handoff, continuity
- [ ] AirPlay
- [ ] AirDrop
- [ ] Sidecar
- [ ] FileVault


# Mainly based on-
- [sortedcord/hp15bs661tx-hackintosh](https://github.com/sortedcord/hp15bs661tx-hackintosh)

## CREDITS

- [Acidanthera](https://github.com/acidanthera)
- [Dortania OC guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCore](https://github.com/acidanthera/OpenCorePkg/)