# Nieve 更新通道

Nieve（网盘解析下载 · 开屏广告自动跳过 · 三合一应用）的检查更新数据源。

## update.json 字段

- `versionCode`：最新版本号（整数，与 APK 的 versionCode 对比）
- `versionName`：展示用版本名
- `minVersionCode`：最低兼容版本（低于此版本的客户端强制提示升级）
- `downloadUrl`：下载地址（一般指向本仓库的 Releases 页面）
- `changelog`：本次更新说明
- `updateDate`：发布日期

## 发布新版本

1. 在 Releases 页面上传新 APK 作为附件；
2. 更新 `update.json` 的 `versionCode` / `versionName` / `changelog`；
3. 客户端「设置 → 关于 Nieve → 检查更新」会拉取
   `https://raw.githubusercontent.com/yingxingw/nieve-update/main/update.json` 进行比较。
