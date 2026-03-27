# KernelSU for OnePlus Nord 2T (CPH2399)

This repository is a specialized fork of the KernelSU Action designed to build a custom kernel for the **OnePlus Nord 2T (mt6893)** running Android 14. It is configured to handle the non-GKI nature of the MediaTek 4.19 kernel using KernelSU version `v0.9.5`.

## ⚠️ Warning
* **Personal Use Only**: This project is intended for individual use. Sharing pre-built binaries is discouraged to respect the original kernel authors.
* **Risk of Brick**: Modifying the kernel is a high-risk operation. Always ensure you have a backup of your original `boot.img` and access to MTK Client or similar recovery tools.

## 📂 Project Structure
* **`boot/boot.img`**: Contains your original OxygenOS Android 14 boot image, used to provide the necessary ramdisk for the build.
* **`arm64/config/`**: Includes the specific configuration files, primarily `oplus6893_defconfig`, required for the Nord 2T.
* **`config.env`**: The central configuration file that defines the kernel source, toolchains, and KernelSU settings.

## 🛠 Build Configuration Summary
| Variable | Value | Description |
| :--- | :--- | :--- |
| **Kernel Source** | `OnePlusOSS/android_kernel_oneplus_mt6893` | Official OnePlus source for the mt6893 platform. |
| **Kernel Config** | `oplus6893_defconfig` | The specific defconfig identified for this device. |
| **Clang Version** | `r487747c` | Android 14 (U) compatible toolchain. |
| **KernelSU Tag** | `v0.9.5` | The final version supporting non-GKI kernels. |
| **Kprobes & Patch** | `Enabled` | Mandatory for KernelSU integration on 4.19 kernels. |

## 🚀 How to Build

1.  **Configure Environment**: Verify that your `config.env` points to the correct "Raw" URL of your uploaded `boot.img`.
2.  **Trigger Workflow**:
    * Navigate to the **Actions** tab in your GitHub repository.
    * Select the **Build Kernel** workflow.
    * Click **Run workflow**.
3.  **Retrieve Artifacts**: After the process finishes (roughly 3-10 minutes), download the `AnyKernel3` zip file from the workflow summary page.

## 📲 Installation
1.  Copy the `AnyKernel3` zip to your phone.
2.  Flash the zip via **TWRP** or a kernel manager (e.g., Franco Kernel Manager).
3.  Install the **KernelSU Manager APK** (version 0.9.5) to authorize root access.

---

## Thanks
- [KernelSU](https://github.com/tiann/KernelSU)
- [AnyKernel3](https://github.com/osm0sis/AnyKernel3)
- [xiaoleGun](https://github.com/xiaoleGun/KernelSU_Action) for the Action template