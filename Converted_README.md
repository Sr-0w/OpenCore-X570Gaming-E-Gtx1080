![Image](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png)

# EFI Ryzentosh • Asus ROG STRIX X570 Gaming-E • AMD Ryzen 7 3700X 8-Core • Nvidia ROG Strix GTX 1080 8GB

Ventura install with Zen Series CPU and Asus ROG STRIX X570-E GAMING motherboard

![Image](https://i.imgur.com/dAdnQ3X.png)


## Hardware - Hackintosh Config

Type
|---|
Item
|---|
**CPU**
AMD Ryzen 7 3700X 8-Core
**Motherboard**
Asus ROG STRIX X570-E GAMING
**RAM**
16GB G.Skill,(2x8GB),3600MHz,DDR4,F4-3600C18-8GVK
**GPU**
Nvidia ROG Strix GTX 1080 8GB
**SSD**
NVMe Samsung SSD 970 EVO Plus 1TB
**Power Supply**
Corsair 750w Full Modular


**SMBIOS**
MacPro7,1
**MacOS**
Ventura 13.5.1
**Opencore**
0.9.3

## Bios Settings

Config
|---|
Status
|---|
**Enter BIOS -&gt; Press Delete -&gt;**
[ Enter Setup ]
**Exit -&gt;**
[ Load Optimised Defaults ]
**Ai Tweaker -&gt; Ai Overclock Tuner -&gt;**
[ D.O.C.P.]
**Advanced -&gt; APM Configuration -&gt; Power On By PCIe -&gt;**
[ Disable ]
**Advanced -&gt; PCI Subsystem Settings -&gt; Above 4G Decoding -&gt;**
[ Enabled ]
**Advanced -&gt; PCI Subsystem Settings -&gt; Re-Size BAR Support -&gt;**
[ Enabled ]
**Advanced -&gt; USB Configuration -&gt; Legacy USB Support -&gt;**
[ Auto or Disabled ]
**Boot -&gt; Boot Configuration -&gt; Fast boot -&gt;**
[ Disable ]
**Boot -&gt; CSM -&gt; Launch CSM -&gt;**
[ Disable ]
**Boot -&gt; Secure boot -&gt; OS Type -&gt;**
[ Windows UEFI mode ]
**Boot -&gt; Secure boot -&gt; Key Management -&gt;**
[ Clear Secure Boot Keys ]

## OpenCore 0.9.3 EFI

### Kexts included


Name
|---|
Version
|---|
Lilu
1.6.6
VirtualSMC
1.3.2
AMDRyzenCPUPowerManagement
0.7.1
WhateverGreen
1.6.5
AppleALC
1.8.3
RestrictEvents
1.1.2
NVMeFix
1.1.0
SmallTreeIntel812576Ethernet
1.3.0
AirportItlwm.kext
v2.3.0-alpha
AppleMCEReporterDisabler
1.2
LucyRTL8125Ethernet
1.1.0
SMCAMDProcessor
0.7.1


### Working Features

Features
|---|
Working?
|---|
2.5G Ethernet
✅
AX Wifi
✅
GPU Recognition
✅
USB Ports & Mappings
✅
CPU Power Management
✅
iMessage
✅
GPU Hardware acceleration
⛔️
Bluetooth
⛔️

## Important informations

Note 1 - If you are using a 6 or Less Core Ryzen then go into the Config,plist and under PlatformInfo->Generic Change the ProcessorType from 0 to 1537, This will list your CPU info correctly inside About This Mac.

Note 2 - The SmallTreeIntel82576.kext is now fully working as of Monterey 12.0 Beta 8

Note 3 - BIOS SETTING CHANGE - Since Bios Revision 4010 Power On By PCIe can break shut down on some peoples builds so ensure the following setting is now set as disabled.

Advanced -> APM Configuration -> Power On By PCIe -> Disabled
For OpenCore Using OpenCore Configurator add your details by modifying the following


<img  src="https://i.imgur.com/sSquwww.png"/>

### Important patch info to set the correct core count for your CPU


Patches are now universal across 15h, 16h, 17h, and 19h by utilizing the OpenCore kernel Quirk ProvideCurrentCpuInfo. OpenCore 0.7.1 or newer is required.

Make sure to enable this quirk or the system won't boot.

Note for Zen 4: Zen 4 (Ryzen 7000) requires patching for IOPCIFamily.kext.
This patch is enabled by default. Please ensure that you've added it to your current config for Zen 4 stability. This patch also allows MSI A520, B550, and X570 boards to boot macOS Monterey and newer.

Core Count patch needs to be modified to boot your system. Find the four algrey - Force cpuid_cores_per_package patches and alter the Replace value only.

<H3 >See the table below for the values matching your CPU Core Count.</H3>

ead
|---|
style="text-align: center;"CoreCount
|---|
style="text-align: left;"Hexadecimal
|---|
style="text-align: center;"**4 Core**
style="text-align: left;"[ 04 ]
style="text-align: center;"**6 Core**
style="text-align: left;"[ 06 ]
style="text-align: center;"**8 Core**
style="text-align: left;"[ 08 ]
style="text-align: center;"**12 Core**
style="text-align: left;"[ 0C ]
style="text-align: center;"**16 Core**
style="text-align: left;"[ 10 ]
style="text-align: center;"**24 Core**
style="text-align: left;"[ 18 ]
style="text-align: center;"**32 Core**
style="text-align: left;"[ 20 ]


So for example, a user with a 6-core processor should use these Replace values: B8 06 0000 0000 / BA 06 0000 0000 / BA 06 0000 0090 / BA 06 0000 00
EXAMPLE



![Image](https://i.imgur.com/BbGgsap.png)


Finally and as always, make sure you reset your NVRAM before booting into the new EFI