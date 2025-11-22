# Plexi Kernel GKI 2.0 - KMI - android14-6.1-11

  This is a modified kernel rebased off the google ACK branch `common-android14-6.1`
  This kernel has been tested and developed for use with Google Pixel Tensor SoC models based on
    the Exynos fab. Personal testing was performed on a Google Pixel 6 Pro. Please open an issue
    if you experience any.

# Features

  - GKI 2.0 kernel KMI compatible with the Pixel 6, 7, 8, and 9 series (include 'a' models)

  - SukiSU v4.0.0 latest; integrated kernel-level root. Download the manager app or read more:
      (https://github.com/SukiSU-Ultra/SukiSU-Ultra)

  - SUSFS v2.0.0; advanced root-hiding capabilities. Management is support via KernelSU module
    or directly through the SukiSU manager app

  - built entirely with Android Clang/LLVM r547379 (v20.0.0) with LTO-thin and Clang CFI optimizations

  - SPL (security patch level) `202509`

  - (TODO: add to in-tree; testing successful) bcm4389 WiFi driver rebuilt + monitor-mode firmware!!!

  - battery life improvements (while still performing better than stock kernel)

  - 

# Flashing Notes:

  1. Use the latest `platform-tools` from Google (v36+) [HIGHLY RECOMMENDED]

  2. Do a test boot before flashing. While in bootloader: `fastboot boot <boot_img>`

  3. Google Implements anti-rollback in the bootloader, which means you can only flash boot images

     that have the same or newer SPL as your device is currently on. For maximum compatibility, I

     will always match the SPL of the current official stock release. If you are on an older SPL or

     aren't sure, you can use `magiskboot unpack <plexi_boot_image>` or download the `Image` file, rename the

     `Image` to `kernel` and then run `magiskboot repack <current_boot_image>`.

  * [TO-DO] Make a script containing the plexi image that you can easily repack with a single command.

  * [TO-DO-TOO] Add a feature to `SukiSU Ultra` manager to automagically repack a boot image.
 


# UNFINISHED


# END
