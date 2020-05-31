# EFI folder for Gigabyte H370M D3H GSM

## System specifications
- Gigabyte H370M D3H GSM F14a
- Intel i5-9400F Coffee Lake
- Silicon Power P34A80M28 NVMe SSD
- Sapphire Pulse/Nitro+ RX 580
- Fenvi FV-HB1200
- macOS 10.15 Catalina

## UEFI Firmware Settings
* Disable CSM (requires GPU with [GOP](https://uefi.org/sites/default/files/resources/UPFS11_P4_UEFI_GOP_AMD.pdf)). Sapphire Nitro+ BIOS switch must be set to _quiet_, that is towards the back of the chassis
* Disable VT-d, FastBoot, SGX, PTT
* Enable Above 4G Decoding, USB XHCI

## USB Map
* Front panel 3.0 Gen 1 mapped to both 2.0 Type A and 3.0 Type A
* Back panel 2.0 mapped to 2.0 Type A
* Back panel 3.0 Gen 1 mapped to 3.0 Type A
* Back panel 3.0 Gen 2 Type A mapped to 3.0 Type A
* Back panel 3.0 Gen 2 Type C *not tested*

## Working
* All USB ports
* NVRAM
* Audio: both mic and line out on both the front and back panel
* sleep/wake
* WiFi / Bluetooth: handoff not tested
* Dual monitor: no black screen issue at login, no sleep/wake issues
* Power Management settings
* SMBus
* CFG Lock [disabled via modGRUBshell.efi](https://dortania.github.io/OpenCore-Desktop-Guide/extras/msr-lock.html)

## References

* [OpenCore Desktop Guide](https://dortania.github.io/OpenCore-Desktop-Guide/)
* [OpenCore configuration checker](https://opencore.slowgeek.com/)

