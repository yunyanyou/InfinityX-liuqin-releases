[中文](README.md) · [日本語](README.ja.md) · English

# Project Infinity-X for Xiaomi Pad 6 Pro (liuqin)

A stock-like custom ROM for the Xiaomi Pad 6 Pro, sourced from Project Infinity-X (LineageOS / AOSP), unofficial build.

## Features

- All hardware and features working (including HDR)
- Keyboard cover works, with a flip-to-disable algorithm
- Full stylus support: connection logic, pen-mode detection (including third-party pens), customizable buttons
- Dolby Audio / Dolby Vision / ac3 / ac4 decoding
- Left/right channels follow screen rotation
- SELinux enforcing
- Touch-enabled recovery

## Download

Builds are on the [SourceForge](https://sourceforge.net/projects/liuqin/files/Project_Infinity-X/) page. The filename includes the date, and a matching `.sha256` checksum file is provided. Verify before flashing:

```bash
sha256sum -c xxx.zip.sha256
```

## Installation

Unlock the bootloader and install the adb / fastboot drivers on your PC before flashing.

1. Flash the provided `recovery.img`, then enter recovery:

   ```
   adb reboot bootloader
   fastboot flash recovery recovery.img
   fastboot reboot recovery
   ```

2. In recovery, choose "Apply update", then run `adb sideload xxx.zip`:

   ```
   adb sideload Project_Infinity-X-x.xx-liuqin-xx.xx.xxxx-GAPPS-UNOFFICIAL.zip
   ```

3. When asked whether to reboot recovery, choose no
4. Choose "Factory reset", then "Format data / factory reset"
5. Reboot

## Changelog

See [CHANGELOG.md](CHANGELOG.md). Versions before 2026-10-03 were released in the QQ group / Coolapk, and some changelogs have been lost.

## Disclaimer

- Back up all your data; I am not responsible for any problems caused by flashing.
- Unlocking the bootloader voids your warranty; I am not responsible for any outcome caused by misuse.
- Project Infinity-X is sourced from LineageOS / AOSP; the copyright of the relevant upstream projects and components belongs to their respective owners.
- The kernel is a stock Xiaomi prebuilt image (unmodified); see [NOTICE.md](NOTICE.md) for its source.
- Flashing wipes all data, so back up first!

Maintainer: Coolapk @測你貓貓, GitHub @yunyanyou 
For bugs or suggestions, join the QQ group at https://qm.qq.com/q/PUF57RhaOk, or file an [Issue](https://github.com/yunyanyou/InfinityX-liuqin-releases/issues).
