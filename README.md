# FlClash-Publish

打包发布工作流仓库，自动从 [go2world-icu/FlClash](https://github.com/go2world-icu/FlClash) 拉取代码构建并发布。

## 使用方式

### 手动触发

1. 打开 Actions → **build** → **Run workflow**
2. 输入 `ref`（分支或标签，如 `main`、`v1.0.0`）
3. 点击运行

### 自动触发

推送 tag `v*` 到本仓库时自动构建并发布 Release 到 FlClash 仓库。

## 所需 Secrets

| Secret | 说明 |
|--------|------|
| `BOARD_SDK_PAT` | 访问私有子模块 board_sdk 的 Token |
| `KEYSTORE` | Android 签名文件 (base64) |
| `SERVICE_JSON` | Google Services 配置 (base64) |
| `KEY_ALIAS` | 签名别名 |
| `STORE_PASSWORD` | 签名库密码 |
| `KEY_PASSWORD` | 签名密钥密码 |
