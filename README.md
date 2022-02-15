# Dell Inspiron 15 7570 Hackintosh
* OpenCore 0.7.8
* macOS Monterey v12.2
* Windows 11 Pro (Dual Boot)
![This is an image](https://user-images.githubusercontent.com/85405303/153669634-a73875e8-4452-4cc2-abd2-fb0e3772f9b8.png)
![This is an image](https://user-images.githubusercontent.com/85405303/153669700-18ee9ac2-aba6-4428-88b7-0d51461e1f05.png)
![This is an image](https://user-images.githubusercontent.com/85405303/153669731-7e2a017e-8a81-4cc7-887a-fad4d8231693.png)

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
* USB-C* (Data/Power Delivery/Display)
* SD Card Reader
* Speakers
* Microphone
* Camera
* Touchscreen
* Trackpad
* Keyboard
* Keyboard Illumination (Native)
* <details><summary><strong>Keyboard Shortcuts</strong></summary>
  
  * FN + ESC = Toggle FN-Key Lock
  * FN + F1 = Mute Audio
  * FN + F2 = Decrease Volume
  * FN + F3 = Increase Volume
  * FN + F4 = Play Previous Track/Chapter
  * FN + F5 = Play/Pause
  * FN + F6 = Play Next Track/Chapter
  * FN + F10 = Toggle Keyboard Backlight
  * FN + F11 = Decrease Display Brightness
  * FN + F12 = Increase Display Brightness
  * FN + Insert = Sleep *Unstable
  * CTRL + Insert = Power Mode Options
  * FN + PgUp = Page Up
  * FN + PgDn = Page Down
  * FN + Home = Home
  * FN + End = End
  </details>
* Facetime
* iMessage
* AirPlay
* HandOff
* Siri
* Battery Indicator

## Not working
* AirDrop 
  * Shows its "On" but its not able to send or recieve with anyone.
* Keyboard Shortuts (FN Keys)
  * FN + F8 = Switch to External Display **[No Function]**
  * FN + F9 = Search **[No Function]**
  * FN + PrtScr = Wireless Off/On (Wifi?) **[No Function]**
  * FN + Insert = Sleep **[Works but unstable]**
    * Seems like laptop turns off rather than sleep. It goes through entire boot process instead of instantly wake up.
  * FN + S = Toggle Scroll Lock **[Wrong Function = Decrease Display Brightness]**
  * FN + B = Pause/Break **[Wrong Function = Increase Display Brightness]**
  * FN + H = Toggle between power & battery-status light/hard-drive activity light **[No Function/Not my device]**
  * FN + R = System Request **[No Function]**
  * FN + CTRL = Open Application Menu **[No Function]**
* Headphone Combo Jack
  * Unstable; Cuts off almost instantly (Needs ALC295PlugFix).
* USB-C (Data)
  * Low Speeds (40 MB/s Write & Read). 
* HDMI
  * Connecting/Disconecting causes screen to go black
    * Current fix is to close laptop, open it and both displays work (idk what's causing this).
