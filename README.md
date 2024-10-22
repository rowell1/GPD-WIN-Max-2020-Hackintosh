[![EFI release](https://img.shields.io/badge/EFI-May_31,_2024-informational.svg)](https://github.com/rowell1/GPD-WIN-Max-2020-Hackintosh/tree/OpenCore)
[![OpenCore version](https://img.shields.io/badge/OpenCore-1.0.0-silver.svg)](https://github.com/acidanthera/OpenCorePkg)
[![MacOS version](https://img.shields.io/badge/BigSur-11.7.10-deeppink.svg)](https://www.apple.com/macos)
[![MacOS version](https://img.shields.io/badge/Monterey-12.7.5-violet.svg)](https://www.apple.com/macos)
[![MacOS version](https://img.shields.io/badge/Ventura-13.6.7-orange.svg)](https://www.apple.com/macos)
[![MacOS version](https://img.shields.io/badge/Sonoma-14.5-success.svg)](https://www.apple.com/macos)  


# GPD-WIN-Max-2020-Hackintosh [WIP]

OpenCore EFI folder for **GPD WIN Max 2020** (i5-1035G7 BIOS 1.16) now supports up to **macOS 14.5 Sonoma**  

With **OCAuxiliaryTools** I updated [_b00t0x/GPD-WIN-Max-Hackintosh (Aug 9, 2023)_](https://github.com/b00t0x/GPD-WIN-Max-Hackintosh) to **OpenCore 1.0.0**  
Added some Kexts and selected SMBIOS **MacBookAir9,1** (maximum OS = Current)  

### _Disclaimer: This repository under construction is for testing only ._  
_I hope to inspire other enthusiasts to extensively test my EFI folder ._  
_Since I don't own a WIN Max 2020, testing it on my multiboot P2 Max 2019 yielded the following results :_  
<img width="796" alt="WM20H" src="https://github.com/rowell1/GPD-WIN-Max-2020-Hackintosh/assets/156696883/16a0e591-e087-442a-a707-e0c10ffd5e48">  


## What’s included
............................................................. release ........ comment .......................... MinKernel .... MaxKernel  
• Lilu.kext ............................................ 1.6.7  
• VirtualSMC.kext ............................... 1.3.2  
• AppleALC.kext ................................. 1.9.0  
• ECEnabler.kext ................................. 1.0.4  
• IntelBTPatcher.kext<sup>_1_</sup> ......................... 2.4.0 _........... for macOS 12 and newer ........ 21.0.0_  
• IntelBluetoothFirmware.kext<sup>_1_</sup> ........... 2.4.0  
• IntelBluetoothInjector.kext<sup>_1_</sup> .............. 2.4.0 _........... for macOS 11 and earlier ........................ 20.9.9_  
• BlueToolFixup.kext<sup>_1_</sup> .......................... 2.6.8 _........... for macOS 12 and newer ........ 21.0.0_  
• NVMeFix.kext ................................... 1.1.1  
• RealtekRTL8111.kext ........................ 2.4.2  
• SMCBatteryManager.kext ................ 1.3.2  
• SMCProcessor.kext .......................... 1.3.2  
• SMCSuperIO.kext ............................. 1.3.2  
• USBMap.kext .................................... 1.0  
• VoodooPS2Controller.kext ............... 2.3.5  
• WhateverGreen.kext ........................ 1.6.6  
• AirportItlwm-Catalina.kext<sup>_2_</sup> ............. 2.2.0<sub>_stable_</sub> _.... for macOS 10.15 only .............. 19.0.0 .... 19.9.9_  
• AirportItlwm-BigSur.kext<sup>_2_</sup> ................ 2.2.0<sub>_stable_</sub> _.... for macOS 11 only ................... 20.0.0 .... 20.9.9_  
• AirportItlwm-Monterey.kext<sup>_2_</sup> ........... 2.2.0<sub>_stable_</sub> _.... for macOS 12 only ................... 21.0.0 .... 21.9.9_  
• AirportItlwm-Ventura.kext<sup>_2_</sup> .............. 2.2.0<sub>_stable_</sub> _.... for macOS 13 only .................. 22.0.0 .... 22.9.9_  
• AirportItlwm-Sonoma14.0.kext<sup>_2_</sup> ....... 2.3.0<sub>_alpha_</sub> _.... for macOS 14.3.1 and earlier ... 23.0.0 .... 23.3.9_  
• AirportItlwm-Sonoma14.4.kext<sup>_2_</sup> ....... 2.3.0<sub>_alpha_</sub> _.... for macOS 14.4 and newer ..... 23.4.0 .... 23.9.9_  
• VoodooI2C.kext ................................ 2.8  
• VoodooI2CGoodix.kext .................... 0.4.0  
• VoodooI2CHID.kext .......................... 1  
• 360Controller.kext ........................... 1.0  
• BrightnessKeys.kext ......................... 1.0.3  
• FeatureUnlock.kext .......................... 1.1.5  
• VoltageShift.kext .............................. 1.24  



## What works  
• iGPU acceleration  
• Built-in sound  
• Keyboard  
...... Hotkeys for brightness/volume adjustment  
• Trackpad  
• Touchpanel  
• Gamepad  
...... mouse mode  
...... Pad mode ( requires 360Controller )  
• Wired LAN  
• Wireless LAN  
• ThunderBolt 3 video output  
...... USB-C to DP 4K/60Hz  
...... USB-C to HDMI 4K/60Hz  
• Battery level display  
...... recommended to use _coconutBattery_ as there is approx. 5% difference in remaining battery capacity.  
• Sleep/Wake  

## What doesn't work  
• Audio output via ThunderBolt 4 port  
• HDMI video/audio output  


# Notes
### _Disclaimer: This repository under construction is for testing only._  
_The experience I learned building [_rowell1/GPD-P2-Max-2019-Hackintosh_](https://github.com/rowell1/GPD-P2-Max-2019-Hackintosh) became the reference for this project ._  


_________________________________________________________________________________________________
_<sup>1</sup> https://openintelwireless.github.io/IntelBluetoothFirmware/FAQ.html#what-additional-steps-should-i-do-to-make-bluetooth-work-on-macos-monterey-and-newer_  
_<sup>2</sup> https://github.com/OpenIntelWireless/itlwm/releases_  
_<sup>3</sup> https://github.com/acidanthera/Lilu/blob/master/KnownPlugins.md_   
_<sup>4</sup> https://osxlatitude.com/forums/topic/18095-how-do-i-grab-my-screens-edid-information/_



