
# Ryzentosh EFI Configuration

![OpenCore Logo](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png)

This repository provides a guide and necessary configurations for installing macOS on a PC with specific hardware using OpenCore as a bootloader. The primary configuration is based on the following hardware:

- **Motherboard**: Asus ROG STRIX X570 Gaming-E
- **CPU**: AMD Ryzen 7 3700X 8-Core
- **GPU**: Nvidia ROG Strix GTX 1080 8GB

---

## Hardware Configuration

| Type          | Item                                                      |
|---------------|-----------------------------------------------------------|
| **CPU**       | AMD Ryzen 7 3700X 8-Core                                  |
| **Motherboard** | Asus ROG STRIX X570-E GAMING                             |
| **RAM**       | 16GB G.Skill,(2x8GB),3600MHz,DDR4,F4-3600C18-8GVK         |
| **GPU**       | Nvidia ROG Strix GTX 1080 8GB                             |
| **SSD**       | NVMe Samsung SSD 970 EVO Plus 1TB                        |
| **Power Supply** | Corsair 750w Full Modular                               |
| **SMBIOS**    | MacPro7,1                                                 |
| **MacOS**     | Ventura 13.5.1                                            |
| **Opencore**  | 0.9.3                                                     |

---

## BIOS Settings

Ensure the following BIOS settings are applied:

- **Config** | **Status**
- **Enter BIOS -> Press Delete** | [ Enter Setup ]
...

---

## Kernel Patching

Kernel patching details are essential for the system's stability. Ensure the provided patches are correctly applied. Specifically, the Zen 3 patch is mandatory for Zen 4 stability, enabling MSI A520, B550, and X570 boards to boot macOS Monterey and newer.

---

## Core Count Patching

Modify the Core Count patch according to your system. Find the "Force cpuid_cores_per_package" patches and alter the Replace value:

| CoreCount | Hexadecimal |
|-----------|-------------|
| 4 Core    | [ 04 ]      |
| 6 Core    | [ 06 ]      |
...

For instance, a user with a 6-core processor should use these Replace values: 
```
B8 06 0000 0000 / BA 06 0000 0000 / BA 06 0000 0090 / BA 06 0000 00
```

---

## Final Notes

Ensure you reset your NVRAM before booting into the new EFI.

![Example Image](https://i.imgur.com/BbGgsap.png)

