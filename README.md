[English](README.en.md) · [日本語](README.ja.md) · 中文

# Project Infinity-X for Xiaomi Pad 6 Pro (liuqin)

为小米平板 6 Pro 构建的类原生，来源 [Project Infinity-X](https://github.com/ProjectInfinity-X)（LineageOS / AOSP），非官方构建。

## 功能

- 所有硬件与功能均正常（含 HDR）
- 键盘保护套正常，翻转禁用算法
- 触控笔完整支持，连接逻辑正常，笔模式识别（含第三方笔）、按键自定义
- 杜比音效 / 杜比视界 / ac3 / ac4 解码
- 屏幕旋转时左右声道跟随
- SELinux 强制执行
- 可触摸的recovery


## 下载

[SourceForge](https://sourceforge.net/projects/liuqin/files/Project_Infinity-X/) 页面，文件名带日期，附带同名 `.sha256`，刷入前可先校验：

```bash
sha256sum -c xxx.zip.sha256
```

## 安装

刷入前需解锁 bootloader，并在电脑装好 adb / fastboot 驱动。

1. 刷入提供的 `recovery.img`，然后进入 recovery

   ```
   adb reboot bootloader
   fastboot flash recovery recovery.img
   fastboot reboot recovery
   ```

2. 在recovery中选择Apply update后执行 `adb sideload xxx.zip`

   ```
   adb sideload Project_Infinity-X-x.xx-liuqin-xx.xx.xxxx-GAPPS-UNOFFICIAL.zip
   ```

3. 弹出是否重启 recovery 时选 no
4. 选择Factory reset，再选择Format data / factory reset
5. 重启

## 更新日志

见 [CHANGELOG.md](CHANGELOG.md)。2026-10-03 之前的版本均在 QQ 群 / 酷安发布，部分日志已丢失。

## 免责声明
- 请备份所有数据，因刷机而产生的任何问题与本人无关。
- 解锁 bootloader 会失去保修，因误操作产生的任何结果与本人无关。
- [Project Infinity-X](https://github.com/ProjectInfinity-X) 来源于 LineageOS / AOSP，相关上游与组件版权归各自所有者
- 内核为小米原厂预编译，未修改，源码见 [NOTICE.md](NOTICE.md)
- 刷机会清空所有数据，请先备份！

维护者：酷安@測你貓貓 github@yunyanyou 
有 bug 或者任何 建议 可进QQ群https://qm.qq.com/q/PUF57RhaOk 反馈，或提交 [Issues](https://github.com/yunyanyou/InfinityX-liuqin-releases/issues)。
