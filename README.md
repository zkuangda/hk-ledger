# 香港账单

香港旅行账单记录工具。纯静态网页，无框架、无 CDN、无后端。

线上地址：https://zkuangda.github.io/hk-ledger/

## 使用

用 iPhone 的 Edge / Safari 打开上面的网址 → 分享菜单 → **添加到主屏幕**，
之后就像 App 一样全屏打开，首次打开后可离线使用。

## 说明

- 数据只保存在浏览器 `localStorage`（`hkLedger_v1`），不上传任何服务器；
  换手机、清理浏览器数据都会丢失，请在账单页用**导出 CSV** 定期备份。
- 汇率默认 `1 HKD = 0.85372 CNY`，可在报告页点击修改（存于 `hkLedger_rate`）。
- 金额内部按「分」（整数）运算，不存在浮点误差。
- 导出的 CSV 为 UTF-8 带 BOM，Excel 可直接打开；导入支持覆盖或追加。

## 文件

| 文件 | 说明 |
| --- | --- |
| `index.html` | 全部页面、样式、逻辑（内联） |
| `manifest.json` | PWA 清单，相对路径以兼容 Pages 子目录 |
| `sw.js` | Service Worker，离线缓存；更新静态文件时改 `CACHE` 版本号 |
| `icon-192.png` `icon-512.png` `apple-touch-icon.png` | 图标 |
