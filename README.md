# Dell Inspiron 15 7570 Hackintosh
* OpenCore 0.7.8
* macOS Monterey v12.2

## Laptop

| **Specifications** | **Details**                                                         |
| -------------- | --------------------------------------------------------------- |
| Laptop Model   | Dell Inspiron 15 7570 - 4K Touchscreen                          |
| CPU            | Intel® Core i7-8550U @ 1.8GHz (Kabylake R)                      |
| GPU            | Intel® UHD Graphics 620 & NVIDIA GeFroce 940MX (Maxwell)        |
| RAM            | 1 X 16GB DDR4 2400MHz                                           |
| Storage        | Samsung PM961 - NVMe M.2 SSD - 512GB                            |
| Display        | 4K Ultra HD - 60 Hz - Touchscreen - 15.6 inches                 |
| WIFI/Bluetooth | Intel® Dual Band Wireless - AC7265                              |
| Ethernet       | Realtek RTL8168/8111                                            |
| Audio          | Realtek ALC3254 or ALC295 (?)                                   |
| BIOS           | 1.20.0                                                         |

## BIOS Settings
<details><summary><strong>General</strong></summary>

* Boot List Option: UEFI
* Legacy Option ROMs: Disabled
* UEFI Boot Path Security: Always, Except Internal HDD
</details>

<details><summary><strong>System Configuration</strong></summary>
  
* Integrated NIC: Enabled w/PXE
* SATA Operation: AHCI
* Drives: Enabled* (If you have another drive installed, make sure its enabled)
* Enable SMART Reporting: Disabled
* USB Confguration: All Enabled
* USB PowerShare: Optional
* Audio: All Enabled
* Keyboard Illumination: Optional* (You can always use <FN + F10> hotkey)
* Keyboard Backlight with AC: Enabled
* Miscellaneous Devices: All Enabled
  </details>

<details><summary><strong>Video</strong></summary>
  
* Dynamic Backlight Control: Enabled
  </details>

<details><summary><strong>Security</strong></summary>
  
* Password Bypass: Disabled
* Password Change: Enabled
* Non-Admin Setup Changes: Disabled
* UEFI Capsule Firmware Updates: Enabled
* PTT Security: PTT On
* Computrace(R): Deactivate
* CPU XD Support: Enabled
* Admin Setup Lockout: Disabled
* Master Password Lockout: Disabled
  </details>

<details><summary><strong>Secure Boot</strong></summary>
  
* Secure Boot: Disabled
* Expert Key Management: Disabled
  </details>

<details><summary><strong>Intel Software Guard Extensions</strong></summary>
  
* Intel SGX: Software Controlled
  </details>

<details><summary><strong>Performance</strong></summary>
  
* Multi Core Support: All
* Intel SpeedStep: Enabled
* C-States Control: Enabled
* Intel TurboBoost: Enabled
* HyperThread Control: Enabled
  </details>

<details><summary><strong>Power Management</strong></summary>
  
* Intel Speed Shirt Technology: Enabled
* USB Wake Support: Disabled
* Wake on LAN: Disabled
  </details>

<details><summary><strong>POST Behavior</strong></summary>
  
* Adapter Warnings: Enabled
* FN Lock Options: Enabled;Secondary
* FastBoot: Thorough
  </details>

<details><summary><strong>Virtualization Support</strong></summary>
  
* Virtualization: Enabled
* VT for Direct I/O: Enabled
  </details>

<details><summary><strong>Wireless</strong></summary>
  
* Wireless Switch: All Enabled
* Wireless Device: All Enabled
  </details>

<details><summary><strong>Maintenance</strong></summary>
  
* BIOS Downgrade: Enabled
* Data Wipe: Disabled
* BIOS Recovery: Enabled;From Hard Drive
  </details>

<details><summary><strong>SupportAssist System Resolution</strong></summary>
  
* Support OS Recovery: Enabled
  </details>


## Working
* WIFI/Bluetooth
* Ethernet
* HDMI*
* x3 USB-A
* USB-C* (Power Delivery)
* SD Card Reader
* Speakers
* Microphone
* Camera
* Touchscreen
* Trackpad
* Keyboard
* Keyboard Illumination (Native)
* FN Keys (FN Lock, Mute, Volume Down/Up, Rewind, Play/Pause, Forward, Display Brightness Keys)
* FN + Insert = Instant Sleep*
* CTRL + Insert = Power Mode Dialog Box
* Facetime
* iMessage
* AirPlay
* Siri
* Battery Indicator

## Not working
* AirDrop 
  * Shows its "On" but its not able to send or recieve with anyone.
* HandOff
  * From Apple devices to laptop, yes. Laptop to Apple devices, no).
* FN Keys "Search", "Switch to External Display", "FN + Print = Wireless On/Off", "FN + B = Pause/Break", "FN + S = Scoll Lock", etc
* FN + Insert = Instant Sleep
  * Doesn't wake up after doing this, not even closing and opening laptop wakes it up)* Putting it to sleep by just closing laptop does work and wakes it back up.
* Headphone Combo Jack
  * Unstable; cuts off after .5 seconds.
* USB-C (Data)
  * Only powers devices, but no data at all for some reason.
* HDMI
  * Connecting/Disconecting causes screen to go black
    * Current fix is to close laptop, open it and both displays work (idk what's causing this).
# EFI
***You must add your own GenSMBIOS info (SystemProductName, SystemSerialNumber, MLB, SystemUUID, & ROM).***

<!-- Markdown link & img dfn's -->
[guideline]: https://dortania.github.io/OpenCore-Install-Guide/
[OpenIntelWireless's Repo]: https://github.com/OpenIntelWireless/HeliPort/releases
[itlwm]: https://github.com/OpenIntelWireless/itlwm/releases
[Proper Tree]: https://github.com/corpnewt/ProperTree
