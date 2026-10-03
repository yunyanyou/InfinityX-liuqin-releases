[中文](README.md) · [English](README.en.md) · 日本語

# Project Infinity-X for Xiaomi Pad 6 Pro (liuqin)

Xiaomi Pad 6 Pro 向けの AOSP 系カスタムROMです。Project Infinity-X（LineageOS / AOSP）由来、非公式ビルド。

## 機能

- すべてのハードウェア・機能が動作（HDR 含む）
- キーボードカバー対応（裏返すと自動で無効化）
- スタイラス完全対応：接続ロジック、ペンモード認識（サードパーティ製ペン含む）、ボタンのカスタマイズ
- Dolby Audio / Dolby Vision / ac3 / ac4 デコード
- 画面の回転に合わせて左右チャンネルも回転
- SELinux enforcing
- タッチ操作可能な recovery

## ダウンロード

[SourceForge](https://sourceforge.net/projects/liuqin/files/Project_Infinity-X/) ページから入手できます。ファイル名には日付が含まれ、同名の `.sha256` が付属しています。書き込む前に検証してください：

```bash
sha256sum -c xxx.zip.sha256
```

## インストール

書き込む前に bootloader をアンロックし、PC に adb / fastboot ドライバをインストールしてください。

1. 付属の `recovery.img` を書き込み、recovery に入ります：

   ```
   adb reboot bootloader
   fastboot flash recovery recovery.img
   fastboot reboot recovery
   ```

2. recovery で「Apply update」を選び、`adb sideload xxx.zip` を実行します：

   ```
   adb sideload Project_Infinity-X-x.xx-liuqin-xx.xx.xxxx-GAPPS-UNOFFICIAL.zip
   ```

3. recovery を再起動するか聞かれたら no を選択
4. 「Factory reset」を選び、「Format data / factory reset」を選択
5. 再起動

## 更新履歴

[CHANGELOG.md](CHANGELOG.md) を参照してください。2026-10-03 より前のバージョンは QQ グループ / Coolapk で公開されており、一部の更新履歴は失われています。

## 免責事項

- すべてのデータをバックアップしてください。書き込みによって生じた問題について、私は一切責任を負いません。
- bootloader のアンロックにより保証は失効します。誤操作によって生じた結果について、私は一切責任を負いません。
- Project Infinity-X は LineageOS / AOSP 由来です。関連する上流プロジェクトおよびコンポーネントの著作権は、それぞれの所有者に帰属します。
- カーネルは Xiaomi 純正のプリビルドイメージ（未変更）です。ソースは [NOTICE.md](NOTICE.md) を参照してください。
- 書き込みによりすべてのデータが消去されます。事前にバックアップを！

メンテナー：Coolapk @測你貓貓、GitHub @yunyanyou 
バグや提案は QQ グループ（https://qm.qq.com/q/PUF57RhaOk）または [Issues](https://github.com/yunyanyou/liuqin-releases/issues) までお願いします。
