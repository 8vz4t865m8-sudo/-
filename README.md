# 深渊幸存者 Abyss Survivor

## 自动构建 iOS IPA（零配置）

### 1. 上传项目到 GitHub
```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/你的用户名/abyss-survivor.git
git push -u origin main
```

### 2. 自动编译
Push 后自动触发 `Build iOS IPA` 工作流，**不需要任何证书配置**。

在 GitHub 页面点击 **Actions** → 选择 **Build iOS IPA** → 等待约 5-8 分钟 → 下载 `AbyssSurvivor-unsigned` 里的 IPA。

### 3. 安装
下载的 IPA 是**未签名**的，用你自己的签名工具安装即可：
- 牛蛙助手 / 爱思助手
- TrollStore
- 企业证书重签
- 或其他签名工具

---

## 如果需要签名版 IPA

去 GitHub 仓库 **Actions** → **Build Signed iOS IPA** → **Run workflow**

这需要在 Settings → Secrets 添加你的 Apple 开发者证书：

| Secret | 说明 |
|--------|------|
| `APP_STORE_CONNECT_TEAM_ID` | Apple Team ID |
| `BUNDLE_IDENTIFIER` | App ID |
| `BUILD_CERTIFICATE_BASE64` | .p12 证书 Base64 |
| `P12_PASSWORD` | 证书密码 |
| `BUILD_PROVISION_PROFILE_BASE64` | .mobileprovision Base64 |
| `APPLE_PROFILE_NAME` | Profile 名称 |

---

## 游戏操作
- **拖动屏幕**：移动角色
- **自动攻击**：角色自动索敌射击
- **收集碎片**：靠近紫色光球吸取经验
- **升级选择**：每升一级选择强化
- **~ 键**：开发者面板
