<p align="center"><img src="https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png" width="200" height="48" /></p>

<h1 align="center">EFI Ryzentosh • Asus ROG STRIX X570 Gaming-E • AMD Ryzen 7 3700X 8-Core • Nvidia ROG Strix GTX 1080 8GB</h1>

<p align="center">This project provides a guide for installing macOS on a PC with specific hardware configurations using OpenCore as a bootloader. It aims to assist users in transforming their PC into a functional Hackintosh. Here, you'll find all necessary steps, configurations, and files to achieve this installation.

Ventura install with Zen Series CPU and Asus ROG STRIX X570-E GAMING motherboard</p>

<p align="center"><img src="https://i.imgur.com/dAdnQ3X.png" /></p>


<h2 align="center">
---

Hardware - Hackintosh Config</h2>

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
    <td align="center"></td>
    <td align="center"></td>
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

<h2 align="center">
---

Bios Settings</h2>

<table align="center">
  <tr>
    <th align="center">Config</th>
    <th align="center">Status</th>
  </tr>
  <tr>
    <td align="center"><strong>Enter BIOS -&gt; Press Delete -&gt;</strong></td>
    <td align="center">[ Enter Setup ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Exit -&gt;</strong></td>
    <td align="center">[ Load Optimised Defaults ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Ai Tweaker -&gt; Ai Overclock Tuner -&gt;</strong></td>
    <td align="center">[ D.O.C.P.]</td>
  </tr>
  <tr>
    <td align="center"><strong>Advanced -&gt; APM Configuration -&gt; Power On By PCIe -&gt;</strong></td>
    <td align="center">[ Disable ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Advanced -&gt; PCI Subsystem Settings -&gt; Above 4G Decoding -&gt;</strong></td>
    <td align="center">[ Enabled ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Advanced -&gt; PCI Subsystem Settings -&gt; Re-Size BAR Support -&gt;</strong></td>
    <td align="center">[ Enabled ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Advanced -&gt; USB Configuration -&gt; Legacy USB Support -&gt;</strong></td>
    <td align="center">[ Auto or Disabled ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Boot -&gt; Boot Configuration -&gt; Fast boot -&gt;</strong></td>
    <td align="center">[ Disable ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Boot -&gt; CSM -&gt; Launch CSM -&gt;</strong></td>
    <td align="center">[ Disable ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Boot -&gt; Secure boot -&gt; OS Type -&gt;</strong></td>
    <td align="center">[ Windows UEFI mode ]</td>
  </tr>
  <tr>
    <td align="center"><strong>Boot -&gt; Secure boot -&gt; Key Management -&gt;</strong></td>
    <td align="center">[ Clear Secure Boot Keys ]</td>
  </tr>
</table>

<h2 align="center">OpenCore 0.9.3 EFI</h2>

<h3 align="center">Kexts included</h3>


<table align="center">
  <tr>
    <th align="center">Name</th>
    <th align="center">Version</th>
  </tr>
  <tr>
    <td align="center">Lilu</td>
    <td align="center">1.6.6</td>
  </tr>
  <tr>
    <td align="center">VirtualSMC</td>
    <td align="center">1.3.2</td>
  </tr>
  <tr>
    <td align="center">AMDRyzenCPUPowerManagement</td>
    <td align="center">0.7.1</td>
  </tr>
  <tr>
    <td align="center">WhateverGreen</td>
    <td align="center">1.6.5</td>
  </tr>
  <tr>
    <td align="center">AppleALC</td>
    <td align="center">1.8.3</td>
  </tr>
  <tr>
    <td align="center">RestrictEvents</td>
    <td align="center">1.1.2</td>
  </tr>
  <tr>
    <td align="center">NVMeFix</td>
    <td align="center">1.1.0</td>
  </tr>
  <tr>
    <td align="center">SmallTreeIntel812576Ethernet</td>
    <td align="center">1.3.0</td>
  </tr>
  <tr>
    <td align="center">AirportItlwm.kext</td>
    <td align="center">v2.3.0-alpha</td>
  </tr>
  <tr>
    <td align="center">AppleMCEReporterDisabler</td>
    <td align="center">1.2</td>
  </tr>
  <tr>
    <td align="center">LucyRTL8125Ethernet</td>
    <td align="center">1.1.0</td>
  </tr>
  <tr>
    <td align="center">SMCAMDProcessor</td>
    <td align="center">0.7.1</td>
  </tr>
</table>


<h3 align="center">Working Features</h3>

<table align="center">
  <tr>
    <th align="center">Features</th>
    <th align="center">Working?</th>
  </tr>
  <tr>
    <td align="center">2.5G Ethernet</td>
    <td align="center">✅</td>
  </tr>
  <tr>
    <td align="center">AX Wifi</td>
    <td align="center">✅</td>
  </tr>
  <tr>
    <td align="center">GPU Recognition</td>
    <td align="center">✅</td>
  </tr>
  <tr>
    <td align="center">USB Ports & Mappings</td>
    <td align="center">✅</td>
  </tr>
  <tr>
    <td align="center">CPU Power Management</td>
    <td align="center">✅</td>
  </tr>
  <tr>
    <td align="center">iMessage</td>
    <td align="center">✅</td>
  </tr>
  <tr>
    <td align="center">GPU Hardware acceleration</td>
    <td align="center">⛔️</td>
  </tr>
  <tr>
    <td align="center">Bluetooth</td>
    <td align="center">⛔️</td>
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

<H3 align="center">See the table below for the values matching your CPU Core Count.</H3>

<table align="center">
  <thead>
    <tr>
      <th style="text-align: center;">CoreCount</th>
      <th style="text-align: left;">Hexadecimal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center;"><strong>4 Core</strong></td>
      <td style="text-align: left;">[ 04 ]</td>
    </tr>
    <tr>
      <td style="text-align: center;"><strong>6 Core</strong></td>
      <td style="text-align: left;">[ 06 ]</td>
    </tr>
    <tr>
      <td style="text-align: center;"><strong>8 Core</strong></td>
      <td style="text-align: left;">[ 08 ]</td>
    </tr>
    <tr>
      <td style="text-align: center;"><strong>12 Core</strong></td>
      <td style="text-align: left;">[ 0C ]</td>
    </tr>
    <tr>
      <td style="text-align: center;"><strong>16 Core</strong></td>
      <td style="text-align: left;">[ 10 ]</td>
    </tr>
    <tr>
      <td style="text-align: center;"><strong>24 Core</strong></td>
      <td style="text-align: left;">[ 18 ]</td>
    </tr>
    <tr>
      <td style="text-align: center;"><strong>32 Core</strong></td>
      <td style="text-align: left;">[ 20 ]</td>
    </tr>
  </tbody>
</table>


<p align="center">So for example, a user with a 6-core processor should use these Replace values: B8 06 0000 0000 / BA 06 0000 0000 / BA 06 0000 0090 / BA 06 0000 00
EXAMPLE</p>



<p align="center"><img src="https://i.imgur.com/BbGgsap.png" width="736" height="625" /> </p>


<p align="center">Finally and as always, make sure you reset your NVRAM before booting into the new EFI</p>
---


