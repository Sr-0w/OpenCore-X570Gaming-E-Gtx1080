<p align="center"><img src="https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png" width="200" height="48" /></p>

<h1 align="center">EFI Ryzentosh • Asus ROG STRIX X570 Gaming-E • AMD Ryzen 7 3700X 8-Core • Nvidia ROG Strix GTX 1080 8GB</h1>

<p align="center">Ventura install with Zen Series CPU and Asus ROG STRIX X570-E GAMING motherboard</p>

<p align="center"><img src="https://i.imgur.com/dAdnQ3X.png" /></p>


<h2 align="center">Hardware - Hackintosh Config</h2>

<table align="center">
  <tr>
    <th align="center">Type</th>
    <th align="center">Item</th>
  </tr>
  <tr>
    <td align="center"><strong>CPU</strong></td>
    <td align="center">AMD Ryzen 7 3700X 8-Core</td>
  </tr>
  <tr>
    <td align="center"><strong>Motherboard</strong></td>
    <td align="center">Asus ROG STRIX X570-E GAMING</td>
  </tr>
  <tr>
    <td align="center"><strong>RAM</strong></td>
    <td align="center">16GB G.Skill,(2x8GB),3600MHz,DDR4,F4-3600C18-8GVK</td>
  </tr>
  <tr>
    <td align="center"><strong>GPU</strong></td>
    <td align="center">Nvidia ROG Strix GTX 1080 8GB</td>
  </tr>
  <tr>
    <td align="center"><strong>SSD</strong></td>
    <td align="center">NVMe Samsung SSD 970 EVO Plus 1TB</td>
  </tr>
  <tr>
    <td align="center"><strong>Power Supply</strong></td>
    <td align="center">Corsair 750w Full Modular</td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td align="center"><strong>SMBIOS</strong></td>
    <td align="center">MacPro7,1</td>
  </tr>
  <tr>
    <td align="center"><strong>MacOS</strong></td>
    <td align="center">Ventura 13.5.1</td>
  </tr>
  <tr>
    <td align="center"><strong>Opencore</strong></td>
    <td align="center">0.9.3</td>
  </tr>
</table>

<h2 align="center">Bios Settings</h2>

<table align="center">
  <tr>
    <th>Config</th>
    <th>Status</th>
  </tr>
  <tr>
    <td><strong>Enter BIOS -&gt; Press Delete -&gt;</strong></td>
    <td>[ Enter Setup ]</td>
  </tr>
  <tr>
    <td><strong>Exit -&gt;</strong></td>
    <td>[ Load Optimised Defaults ]</td>
  </tr>
  <tr>
    <td><strong>Ai Tweaker -&gt; Ai Overclock Tuner -&gt;</strong></td>
    <td>[ D.O.C.P.]</td>
  </tr>
  <tr>
    <td><strong>Advanced -&gt; APM Configuration -&gt; Power On By PCIe -&gt;</strong></td>
    <td>[ Disable ]</td>
  </tr>
  <tr>
    <td><strong>Advanced -&gt; PCI Subsystem Settings -&gt; Above 4G Decoding -&gt;</strong></td>
    <td>[ Enabled ]</td>
  </tr>
  <tr>
    <td><strong>Advanced -&gt; PCI Subsystem Settings -&gt; Re-Size BAR Support -&gt;</strong></td>
    <td>[ Enabled ]</td>
  </tr>
  <tr>
    <td><strong>Advanced -&gt; USB Configuration -&gt; Legacy USB Support -&gt;</strong></td>
    <td>[ Auto or Disabled ]</td>
  </tr>
  <tr>
    <td><strong>Boot -&gt; Boot Configuration -&gt; Fast boot -&gt;</strong></td>
    <td>[ Disable ]</td>
  </tr>
  <tr>
    <td><strong>Boot -&gt; CSM -&gt; Launch CSM -&gt;</strong></td>
    <td>[ Disable ]</td>
  </tr>
  <tr>
    <td><strong>Boot -&gt; Secure boot -&gt; OS Type -&gt;</strong></td>
    <td>[ Windows UEFI mode ]</td>
  </tr>
  <tr>
    <td><strong>Boot -&gt; Secure boot -&gt; Key Management -&gt;</strong></td>
    <td>[ Clear Secure Boot Keys ]</td>
  </tr>
</table>

<h2 align="center">OpenCore 0.9.3 EFI</h2>

<h3 align="center">Kexts included</h3>


<table align="center">
  <tr>
    <th>Name</th>
    <th>Version</th>
  </tr>
  <tr>
    <td>Lilu</td>
    <td>1.6.6</td>
  </tr>
  <tr>
    <td>VirtualSMC</td>
    <td>1.3.2</td>
  </tr>
  <tr>
    <td>AMDRyzenCPUPowerManagement</td>
    <td>0.7.1</td>
  </tr>
  <tr>
    <td>WhateverGreen</td>
    <td>1.6.5</td>
  </tr>
  <tr>
    <td>AppleALC</td>
    <td>1.8.3</td>
  </tr>
  <tr>
    <td>RestrictEvents</td>
    <td>1.1.2</td>
  </tr>
  <tr>
    <td>NVMeFix</td>
    <td>1.1.0</td>
  </tr>
  <tr>
    <td>SmallTreeIntel812576Ethernet</td>
    <td>1.3.0</td>
  </tr>
  <tr>
    <td>AirportItlwm.kext</td>
    <td>v2.3.0-alpha</td>
  </tr>
  <tr>
    <td>AppleMCEReporterDisabler</td>
    <td>1.2</td>
  </tr>
  <tr>
    <td>LucyRTL8125Ethernet</td>
    <td>1.1.0</td>
  </tr>
  <tr>
    <td>SMCAMDProcessor</td>
    <td>0.7.1</td>
  </tr>
</table>


<h3 align="center">Working Features</h3>

<table align="center">
  <tr>
    <th>Features</th>
    <th>Working?</th>
  </tr>
  <tr>
    <td>2.5G Ethernet</td>
    <td>✅</td>
  </tr>
  <tr>
    <td>AX Wifi</td>
    <td>✅</td>
  </tr>
  <tr>
    <td>GPU Recognition</td>
    <td>✅</td>
  </tr>
  <tr>
    <td>USB Ports & Mappings</td>
    <td>✅</td>
  </tr>
  <tr>
    <td>CPU Power Management</td>
    <td>✅</td>
  </tr>
  <tr>
    <td>iMessage</td>
    <td>✅</td>
  </tr>
  <tr>
    <td>GPU Hardware acceleration</td>
    <td>⛔️</td>
  </tr>
  <tr>
    <td>Bluetooth</td>
    <td>⛔️</td>
  </tr>
</table>

<h2 align="center">Important informations</h2>

<p align="center">Note 1 - If you are using a 6 or Less Core Ryzen then go into the Config,plist and under PlatformInfo->Generic Change the ProcessorType from 0 to 1537, This will list your CPU info correctly inside About This Mac.</p>

<p align="center">Note 2 - The SmallTreeIntel82576.kext is now fully working as of Monterey 12.0 Beta 8</p>

<p align="center">Note 3 - BIOS SETTING CHANGE - Since Bios Revision 4010 Power On By PCIe can break shut down on some peoples builds so ensure the following setting is now set as disabled.</p>

<p align="center">Advanced -> APM Configuration -> Power On By PCIe -> Disabled</p>
<p align="center">For OpenCore Using OpenCore Configurator add your details by modifying the following</p>


<img align="center" src="https://i.imgur.com/sSquwww.png"/>

<h3 align="center">Important patch info to set the correct core count for your CPU</h3>


<p align="center">Patches are now universal across 15h, 16h, 17h, and 19h by utilizing the OpenCore kernel Quirk ProvideCurrentCpuInfo. OpenCore 0.7.1 or newer is required.</p>

<p align="center">Make sure to enable this quirk or the system won't boot.</p>

<p align="center">Note for Zen 4: Zen 4 (Ryzen 7000) requires patching for IOPCIFamily.kext.</p>
<p align="center">This patch is enabled by default. Please ensure that you've added it to your current config for Zen 4 stability. This patch also allows MSI A520, B550, and X570 boards to boot macOS Monterey and newer.</p>

<p align="center">Core Count patch needs to be modified to boot your system. Find the four algrey - Force cpuid_cores_per_package patches and alter the Replace value only.</p>

### See the table below for the values matching your CPU Core Count.

|        CoreCount      | Hexadecimal |
|:---------------------:|------------ |
|     **4 Core**        | [   04    ] |
|     **6 Core**        | [   06    ] |
|     **8 Core**        | [   08    ] |
|     **12 Core**       | [   0C    ] |
|     **16 Core**       | [   10    ] |
|     **24 Core**       | [   18    ] |
|     **32 Core**       | [   20    ] |

So for example, a user with a 6-core processor should use these Replace values: B8 06 0000 0000 / BA 06 0000 0000 / BA 06 0000 0090 / BA 06 0000 00
EXAMPLE



<img src="https://i.imgur.com/BbGgsap.png" width="736" height="625" /> 


Finally and as always, make sure you reset your NVRAM before booting into the new EFI
