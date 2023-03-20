
<img src="https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png" width="200" height="48" />

# Hackintosh
# EFI Gigabyte-B360-Aorus-Gaming-3

### Currently Running On MacOS Ventura 13.2.1 

<img src="https://i.imgur.com/nRNr7SF.png" width="594" height="357" />

## Hardware - Hackintosh Config

|       Type       | Item                                             |
|:----------------:|--------------------------------------------------|
|     **CPU**      | [ Intel(R) Core(TM) i7-9700K CPU @ 3.60GHz ]     |
| **Motherboard**  | [ Gigabyte B360 Aorus Gaming 3 ]                 |
|     **RAM**      | [ 32GB DDR4 2666Mhz ]                            |
|     **GPU**      | [ AMD Radeon RX 580 4GB (Navi 10 XT) ]           |
|     **SSD**      | [ NVMe Corsair Force MP400 1TB ]                 |
| **Power Supply** | [ Asus ROG-THOR-1200P, 1200W, 80 Plus Platinum ] |
|                  |                                                  |
|    **SMBIOS**    | [ MacPro19,2 ]                                   |
|    **MacOS**     | [ Ventura ]                                     |
|   **Opencore**   | [ 0.9.0 ]                                        |


## BIOS Setting

### BIOS Version: F15b

### Disable

```
* Fast Boot
* Secure Boot
* Serial/COM Port
* VT-d
* CFG Lock (must be disable)
* Intel Platform Trust

```

### Enable

```
* Above 4G decoding
* Hyper-Threading
* EHCI/XHCI Hand-off
* DVMT Pre-Allocated(iGPU Memory): 64MB
* SATA Mode: AHCI
```

## Change Serial,MLB,SMUUID

At first download GenSMBIOS tool from [here.](https://github.com/corpnewt/GenSMBIOS)

Then extract it & Open-> GenSMBIOS.command

#### 1. Select option :3

![](https://github.com/sohagmahin/Gigabyte-B360-Aorus-Gaming-3-Hackintosh/blob/main/screenshots/1.png "1. Select option :3")

#### 2. type: iMac19,2

![](https://github.com/sohagmahin/Gigabyte-B360-Aorus-Gaming-3-Hackintosh/blob/main/screenshots/2.png)

#### 3. Copy the Serial, Board Serial & SmUUID

![](https://github.com/sohagmahin/Gigabyte-B360-Aorus-Gaming-3-Hackintosh/blob/main/screenshots/3.png)

#### 4. Open EFI->OC->config.plist then Replace it with your generated SMBIOS

```
Serial -> SystemSerialNumber
Board Serila -> MLB
SmUUID ->SystemUUID
```

![](https://github.com/sohagmahin/Gigabyte-B360-Aorus-Gaming-3-Hackintosh/blob/main/screenshots/4.png)

## Guide<br>

- [Open Core Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## Credit<br>

- Thanks to [Acidanthera](https://github.com/acidanthera) for providing [AppleALC](https://github.com/acidanthera/AppleALC), [HibernationFixup](https://github.com/acidanthera/HibernationFixup), [Lilu](https://github.com/acidanthera/Lilu), [NVMeFix](https://github.com/acidanthera/NVMeFix), [OcBinaryData](https://github.com/acidanthera/OcBinaryData), [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg), [RestrictEvents](https://github.com/acidanthera/RestrictEvents), [VirtualSMC](https://github.com/acidanthera/VirtualSMC), and [WhateverGreen](https://github.com/acidanthera/WhateverGreen).


[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)
