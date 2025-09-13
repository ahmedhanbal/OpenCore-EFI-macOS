# Hackintosh EFI for HP 15s-EF2127WM laptop 

This repository contains the EFI setup I used to successfully boot macOS on my HP laptop with AMD CPU.

I have tested this configuration on:

- **macOS 15 (Sequoia)**
- **macOS Tahoe Beta**

Previous versions may also work (as low as Catalina).

---

## Hardware Specs

### ✅ Supported
- **CPU:** AMD Ryzen 5 5500U  
- **GPU:** AMD Radeon Graphics (internal display works)  
- **Audio:** Realtek(R) ALC236 (working with layout-id 3, speakers OK) 
- **Audio:** AMD High Definition Audio Device (output works)  

### ❌ Unsupported / Not Working
- **Audio (Microphone Array):** AMD Audio Device  
- **Wi-Fi:** Realtek RTL8822CE 802.11ac PCIe Adapter  
- **Storage Controller:** Gold P31/BC711/PC711 NVMe SSD  
- **Bluetooth:** Realtek Bluetooth 5 Adapter  

---

## Storage Note

Since the onboard **NVMe SSD is unsupported**, I used my **rooted Android phone** as a storage device.  

Instead of exposing the entire phone storage, I created a **raw `.img` file** on the Android device, which macOS treated as a native disk.  
This allowed me to install and boot macOS directly, bypassing the unsupported NVMe controller.  

---

## Installation Reference

I followed [Dortania’s OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) to set up this Hackintosh.  
