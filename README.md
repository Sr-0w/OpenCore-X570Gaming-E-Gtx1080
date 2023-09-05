This README provides a detailed guide on setting up a Hackintosh system with specific hardware configurations using OpenCore. Before proceeding, especially if you are new to Hackintosh or the OpenCore bootloader, it's crucial to familiarize yourself with the official [OpenCore Documentation](https://dortania.github.io/OpenCore-Install-Guide/). This guide will give you an overview of the setup process, but the OpenCore docs will provide a deep dive into each step.

<p align="center"><img src="https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png" width="200" height="48" /></p> 

# EFI Ryzentosh • Asus ROG STRIX X570 Gaming-E • AMD Ryzen 7 3700X 8-Core • Nvidia ROG Strix GTX 1080 8GB

This guide focuses on setting up the Ventura macOS version on a system powered by the Zen Series CPU and Asus ROG STRIX X570-E GAMING motherboard

<p align="center"><img src="https://i.imgur.com/dAdnQ3X.png" />

---

### Hardware Configuration for Hackintosh Setup

|       Type       | Item                                   |
|:----------------:|----------------------------------------|
|     **CPU**      | AMD Ryzen 7 3700X 8-Core                      |
| **Motherboard**  | Asus ROG STRIX X570-E GAMING     |
|     **RAM**      | 16GB G.Skill,(2x8GB),3600MHz,DDR4,F4-3600C18-8GVK   |
|     **GPU**      | Nvidia ROG Strix GTX 1080 8GB  |
|     **SSD**      | NVMe Samsung SSD 970 EVO Plus 1TB   |
| **Power Supply** | Corsair 750w Full Modular  |

|    **SMBIOS**    | MacPro7,1                           |
|    **MacOS**     | Ventura 13.5.1                       |
|   **Opencore**   | 0.9.3                             |

---

### BIOS Settings

|        Config                                                    | Status                     |
|:----------------------------------------------------------------:|----------------------------|
| **Enter BIOS -> Press Delete ->**                                | Enter Setup            |
| **Exit ->**                                                      | Load Optimised Defaults|
| **Ai Tweaker -> Ai Overclock Tuner ->**                          | D.O.C.P.                |
| **Advanced -> APM Configuration -> Power On By PCIe ->**         | [ Disable ]                |
| **Advanced -> PCI Subsystem Settings -> Above 4G Decoding ->**   | [ Enabled ]                |
| **Advanced -> PCI Subsystem Settings -> Re-Size BAR Support ->** | [ Enabled ]                |
| **Advanced -> USB Configuration -> Legacy USB Support ->**       | [ Auto or Disabled ]       |
| **Boot -> Boot Configuration -> Fast boot ->**                   | [ Disable ]                |
| **Boot -> CSM -> Launch CSM ->**                                 | [ Disable ]                |
| **Boot -> Secure boot -> OS Type ->**                            | [ Windows UEFI mode ]      |
| **Boot -> Secure boot -> Key Management ->**                     | [ Clear Secure Boot Keys ] |

## OpenCore 0.9.3 EFI

### Kexts included

* Lilu 1.6.6,
* VirtualSMC 1.3.2,
* AMDRyzenCPUPowerManagement 0.7.1
* WhateverGreen 1.6.5,
* AppleALC 1.8.3,
* RestrictEvents 1.1.2,
* NVMeFix 1.1.0
* SmallTreeIntel812576Ethernet 1.3.0
* AirportItlwm.kext v2.3.0-alpha
* AppleMCEReporterDisabler 1.2
* LucyRTL8125Ethernet 1.1.0
* SMCAMDProcessor 0.7.1

#---

### Working Features

|        Features         |   Working?  |
|:-----------------------:|------------ |
|      2.5G Ethernet      |    ✔️     |
|         AX Wifi         |    ✔️     |
|     GPU Recognition     |    ✔️     |
|   USB Ports & Mappings  |    ✔️     |
|   CPU Power Management  |    ✔️     |
|         iMessage        |    ✔️     |
|GPU Hardware acceleration|    ❌     |
|        Bluetooth        |    ❌     |

---

### Important Notes

> **Note 1:** If you are using a 6 or Less Core Ryzen then go into the Config,plist and under PlatformInfo->Generic Change the ProcessorType from 0 to 1537, This will display your CPU information correctly inside About This Mac.

> **Note 2:** The SmallTreeIntel82576.kext is now fully working as of Monterey 12.0 Beta 8

> **Note 3:** BIOS SETTING CHANGE - Since Bios Revision 4010 Power On By PCIe can break shut down on some peoples builds so ensure the following setting is now set as disabled.

Advanced -> APM Configuration -> Power On By PCIe -> Disabled
For OpenCore, use the OpenCore Configurator to add your details by modifying the following

<p align="center"><img src="https://i.imgur.com/sSquwww.png"/>

#---

### Important Patch Information: Setting the Correct Core Count

It's important to note that patches are now universal across 15h, 16h, 17h, and 19h by utilizing the OpenCore kernel Quirk ProvideCurrentCpuInfo. OpenCore 0.7.1 or newer is required.

Make sure to enable this quirk or the system won't boot.

Note for Zen 4: Zen 4 (Ryzen 7000) requires patching for IOPCIFamily.kext.
This patch is enabled by default. Please ensure that you've added it to your current config for Zen 4 stability. This patch also allows MSI A520, B550, and X570 boards to boot macOS Monterey and newer.

Core Count patch needs to be modified to boot your system. Find the four algrey - Force cpuid_cores_per_package patches and alter the Replace value only.
