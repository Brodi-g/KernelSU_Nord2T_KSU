# KernelSU for OnePlus Nord 2T (CPH2399)

This repository builds a KernelSU-enabled kernel for the **OnePlus Nord 2T** running Android 14.

## ⚠️ Warning
* **Personal Use Only**: Do not share built kernels to respect original authors.
* **Risk**: Modifying kernels can cause bootloops. Have a backup of your original `boot.img`.

## 📂 Project Structure
* **`boot/boot.img`**: Stock OxygenOS Android 14 boot image for ramdisk.
* [cite_start]**`config.env`**: Build configuration (Kernel v4.19, KernelSU v0.9.5). 

## 🛠 Build Setup
| Variable | Value |
| :--- | :--- |
| **Kernel Source** | `OnePlusOSS/android_kernel_oneplus_mt6893` |
| **Kernel Config** | `oplus_mt6893_defconfig` |
| **Clang** | `r487747c` (Android 14 compatibility) |
| **KernelSU** | `v0.9.5` (Last non-GKI version) |

## 🚀 How to Build
1. [cite_start]Update `SOURCE_BOOT_IMAGE` in `config.env` with your Raw link. 
2. Go to **Actions** -> **Build Kernel**.
3. Click **Run workflow**.
4. Download the `AnyKernel3` zip from the completed action.

## 📲 Installation
1. Flash the `AnyKernel3` zip via TWRP.
2. Install the **KernelSU Manager APK v0.9.5**.

---

## Thanks
- [KernelSU](https://github.com/tiann/KernelSU)
- [AnyKernel3](https://github.com/osm0sis/AnyKernel3)
- [xiaoleGun](https://github.com/xiaoleGun/KernelSU_Action) for the Action template