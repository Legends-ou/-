# Security

请不要把 API Key、签名证书、私钥或真实用户图片提交到仓库。

## API Key

应用会把用户填写的 AI 配置保存在本机用户配置目录中，不会写入项目源码目录。

公开 issue 或截图时，请遮挡：

- API Key
- 私有 Base URL
- 本地文件路径中的敏感信息

## Code Signing

Windows 代码签名证书应通过 GitHub Secrets 或本机安全存储管理，不要提交到 GitHub。
