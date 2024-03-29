# MSI-Z97-Hackintosh-Opencore

This is a fully working EFI for MSI Z97 macOS Big Sur (Current: 12 Beta 5) installation booted using Opencore. Also supports Big Sur and Catalina.

![](https://i.imgur.com/9vQ2iJT.png)

## Specs

- MSI Z97 Gaming5 Motherboard
- Intel i5-4690K Processor (Overclocked to 4.4Ghz, 1.23v)
- 12GB 1333Mhz DDR3 RAM
- Samsung 256GB NVMe Storage
- Realtek ALC1150 Audio
- GTX760 2GB GPU
- Atheoros E2200 Gigabit Ethernet
- Fenvi T919 Wireless for WiFi and Bluetooth



## BIOS Settings

* Settings > Advanced > Integrated Graphics Configuration > IGD Multi-Monitor > **Enabled** (If running iGPU in Headless mode)
* OC Settings > CPU Features - **Intel VT-d** > **Disabled**
* OC Settings > CPU Features - **CFG Lock** > **Disabled**



## Working

Basically everything working including iMessage, Facetime, Airdrop, Handoff, Continuity, iTunes DRM (not TV+), Apple Watch Unlocking, Intel Quicksync. USB is mapped properly, USB3/USB2 all ports are working. [Link to USBMap](https://github.com/i3p9/USBMap-MSI-Z97-Gaming5) (Modification to the mentioned USBMap: removed HS10 port to accomodate Fenvi t919 usb header).


Sidecar doesn't work because the Processor/GPU doesn't support HEVC encode/decoding. It can be force enabled but the result is unuseable. If you really want to, use [FeatureUnlock](https://github.com/acidanthera/FeatureUnlock). Note: FeatureUnlock is now enabled in the EFI to enable Universal Control and other features.



## Notes

- Use a proper plist editor (Like Xcode, [PlistEdit Pro](https://www.fatcatsoftware.com/plisteditpro/) or [ProperTree](https://github.com/corpnewt/ProperTree)) to edit the config.plist file.

- You have to add the MLB/ROM/UUID/Serial yourself. (Generate them using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)). Use the SMBIOS `iMac15,1` if using a Dedicated GPU, or the SMBIOS `iMac14,4` if running off of iGPU only.

- Lastly, the DevicesPropertises section, in `PciRoot(0x0)/Pci(0x2,0x0) -> AAPL,ig-platform-id [Comment]`, put  `04001204` if using a Dedicated GPU, or  `0300220D` if running off of iGPU only.
- USB is mapped properly. Link to diagram: https://i.imgur.com/GcuevXE.png
- You have to use `iMac16,2` as the SMBIOS for Monterey to work. If you're on Big Sur or below, it's recommended to keep using iMac15,1. 


## Current versions of Kexts/Opencore in the EFI

* Opencore 0.7.2
* Everything else is updated (As of 4 August 2021)
