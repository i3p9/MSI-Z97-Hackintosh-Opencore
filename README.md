# MSI-Z97-Hackintosh-Opencore

This is a fully working EFI for MSI Z97 macOS Big Sur (Current: 11.4) installation booted using Opencore.

![](https://i.imgur.com/i8ChKEV.png)

## Specs

- MSI Z97 Gaming5 Motherboard
- Intel i5-4690K Processor
- Team 3200Mhz 8GB DDR3 RAM
- Samsung 256GB NVMe Storage
- Realtek ALC1150 Audio
- GTX760 2GB GPU
- Atheoros E2200 Gigabit Ethernet
- Fenvi T919 Wireless for WiFi and Bluetooth 



# BIOS Settings

* Settings > Advanced > Integrated Graphics Configuration > IGD Multi-Monitor > **Enabled** (If running iGPU in Headless mode)
* OC Settings > CPU Features - **Intel VT-d** > **Disabled**
* OC Settings > CPU Features - **CFG Lock** > **Disabled**



 ## Working

Basically everything working including iMessage, Facetime, Airdrop, Handoff, Continuity, iTunes DRM (not TV+), Apple Watch Unlocking, Intel Quicksync. USB is mapped properly, USB3/USB2 all ports are working. [Link to USBMap](https://github.com/i3p9/USBMap-MSI-Z97-Gaming5) (Modification to the USBMap: removed HS10 port to accomodate Fenvi t919 usb header)



Sidecar doesn't work because the Processor/GPU doesn't support HEVC encode/decoding. It can be force enabled but the result is unuseable.



## Notes

Use a proper plist editor (Like [PlistEdit Pro](https://www.fatcatsoftware.com/plisteditpro/) or Xcode or [ProperTree](https://github.com/corpnewt/ProperTree)) to edit the config.plist file. You have to add the MLB/ROM/UUID/Serial yourself. (Generate them using [macserial](https://github.com/acidanthera/MacInfoPkg))



## Current versions of Kexts/Opencore in the EFI

* Opencore 0.6.9
* Everything else is updated (As of 27 May 2021)
