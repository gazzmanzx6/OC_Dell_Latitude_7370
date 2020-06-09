# OC_Dell_Latitude_7370
OpenCore EFI MacOS Catalina on Dell Latitude 7370

Use at your own risk! I can not be held responsible for any damage done.

- Dell Latitude 13 7370
- Intel m7-6Y75 Dual-Core
- Intel HD515
- 16 GB 1866 MHz LPDDR3 RAM
- PC300 NVMe SK hynix 256GB
- Broadcom BCM943602CS (using M.2 Key A+E adapter) with third antenna
- Sierra Wireless EM7345 4G LTE WWAN
- 1920x1080@60Hz HD Display
- Realtek ALC256 Audio (rebranded as ALC3246)
- BIOS version 1.18.5
- OpenCore v0.5.9
- MacBook9,1 as SMBIOS


Working:
- EC power management
- HD515 with full hardware acceleration
- USB-C charging
- Audio as AppleALC layout-id 11(0B000000)
- display brightness control
- touchpad with scrolling and two-finger-click (VoodooPS2)
- keyboard with backlight
- function keys (using Karabiner)
- microSD cardreader
- USB-C DisplayPort/Data/Thunderbolt3
- Handoff
- unlock with Apple Watch
- iMessage
- FaceTime
- headphone jack (using ComboJack https://github.com/hackintosh-stuff/ComboJack)

Not working:
- WWAN

Not tested:
- mini HDMI port (don't have that type of cable)

Recommended tools:
- MountEFI (mount EFI folder under MacOS)
- PlistEdit Pro (edit config.plist with GUI)


BIOS setting:
- System Configuration > Thunderbolt Adapter Configuration
  - Security level - No Security
- Virtualization Support > VT for Direct I/O
  - Disabled

BIOS tweaks:

  - disable CFG Lock: **setup_var 0x109 0x0**   Verify before use (extracted from BIOS 1.18.5)
  - increase DVMT:    **setup_var 0x432 0x3**    Verify before use (extracted from BIOS 1.18.5)

