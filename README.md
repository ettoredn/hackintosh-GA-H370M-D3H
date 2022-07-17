# EFI folder for Gigabyte H370M D3H GSM

## System specifications 🖥
- Gigabyte H370M D3H GSM F14a
- Intel i5-9400F Coffee Lake
- Silicon Power P34A80M28 NVMe SSD
- Sapphire Pulse/Nitro+ RX 580
- Fenvi FV-HB1200
- macOS 10.15 Catalina

## UEFI Firmware Settings 🔧
- Disable CSM (requires GPU with [GOP](https://uefi.org/sites/default/files/resources/UPFS11_P4_UEFI_GOP_AMD.pdf)). Sapphire Nitro+ BIOS switch must be set to _quiet_, that is towards the back of the chassis
- Disable VT-d, FastBoot, SGX, PTT
- Enable Above 4G Decoding, USB XHCI

## OpenCore/NVRAM/other Settings 🔧
- Sytem Integrity Protection disabled (value obtained from recovery csrutil)

## USB Map
|     Physical Port     | macOS Port | Tested |
| --------------------- | -----------| ------ |
| Front 3.0 Gen1 Type A | 2.0 & 3.0  |   ✓    |
| Back 2.0 Type A       |     2.0    |   ✓    |
| Back 3.0 Gen1 Type A  |     3.0    |   ✓    |
| Back 3.0 Gen2 Type A  |     3.0    |   ✓    |
| Back 3.0 Gen2 Type C  |     3.0    |   -    |
| Internal F_USB2 (BT)  |     2.0    |   ✓    |



## Working 🏆
- USB ports
- NVRAM
- Audio: both mic and line out at both the front and back panel
- Sleep / Wake
- WiFi / Bluetooth: handoff not tested
- Dual monitor: no black screen issue at login, no sleep/wake issues
- Power Management settings
- SMBus
- CFG Lock [disabled via modGRUBshell.efi](https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html)

## Not Working ⛔
- Bluetooth audio devices, both mic and audio issues. Removing AppleALC makes them work though.

## Notes
- Plugging a mouse or keyboard into a USB 3.0 port could block boot (before USB map)
- Plugging the EFI USB drive into USB 3.0 port may result in boot issues (before USB map?)

## References
* [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
* [OpenCore configuration checker](https://opencore.slowgeek.com/)

