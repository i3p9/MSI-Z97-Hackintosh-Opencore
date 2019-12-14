# MSI-Z97-Hackintosh-Opencore

This is a fully working EFI for MSI Z97 macOS Catalina installation booted using Opencore.

![](https://i.imgur.com/tt3wSGP.png)

## Specs

- MSI Z97 Gaming5 Motherboard
- Intel i5-4690K Processor
- Team 3200Mhz 8GB DDR3 RAM
- Samsung 256GB NVMe Storage
- Realtek ALC1150 Audio
- GTX760 2GB GPU
- Atheoros E2200 Gigabit Ethernet
- Fenvi T919 Wireless for WiFi and Bluetooth 



 ## Working

Basically everything working including iMessage, Facetime, Airdrop, Handoff, Continuity, iTunes DRM, Apple Watch Unlocking, Intel Quicksync. 



Sidecar doesn't work because the Processor/GPU doesn't support HEVC encode/decoding. It can be force enabled but the result is unuseable.



## Notes

Use a proper plist editor (Like [PlistEdit Pro](https://www.fatcatsoftware.com/plisteditpro/) or Xcode or [ProperTree](https://github.com/corpnewt/ProperTree)) to edit the config.plist file. You have to add the MLB/ROM/UUID/Serial yourself. (Generate them using [macserial](https://github.com/acidanthera/MacInfoPkg))



## Current versions of Kexts/Opencore in the EFI

* Opencore 0.5.2 (0.5.3 caused very early kernel panic so skipping it for now)
* Everything else is updated (As of 15 December 2019)