# 自动出餐 iOS 壳（Capacitor）

已配置：
- appId: net.zunlan.hm
- appName: 自动出餐
- 远程地址: https://hm.zunlan.net
- 相机/相册权限已写入 Info.plist

## 方案 A：有 Mac

```bash
npm install
npx cap sync ios
npx cap open ios
```

Xcode 里：
1. 选 App target → Signing & Capabilities
2. Team 选你的 Apple ID（免费账号即可）
3. Bundle Identifier 改成唯一值，例如 net.zunlan.hm
4. 连上 iPhone，Run

免费账号：7 天有效期，最多 3 台设备。

## 方案 B：没有 Mac（Windows）

1. 把整个目录上传到 GitHub 仓库
2. Actions → build-ios-unsigned → Run workflow
3. 下载 hm-unsigned.ipa
4. Windows 安装 Sideloadly
5. Sideloadly 里登录 Apple ID，选择 IPA，连 iPhone 安装

Sideloadly 会用你的 Apple ID 重新签名，7 天有效。
