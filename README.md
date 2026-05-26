# 图片自动命名器 Lite

一个轻量的 Windows 桌面工具，用来把杂乱截图、微信图片、QQ 图片等批量重命名成更容易理解的文件名。

基于 Tauri + React + Vite 构建，发布后是普通 `.exe` 安装包，用户不需要安装 Node.js、Rust、Cargo 或开发工具。

## 功能

- 规律重命名：根据前两个文件名推断编号规律，批量生成后续文件名。
- AI 主题命名：识别图片内容，用四个字概括主题并生成新文件名。
- 两套功能独立：规律命名和 AI 命名互不干扰。
- 实时预览：识别或规则生成后，列表中立即显示新文件名。
- 选择性处理：支持全部图片、选中图片、失败图片重新识别。
- 停止识别：AI 识别过程中可以随时停止。
- 安全重命名：目标重名时自动避让，支持撤销最近一次重命名。
- 配置持久化：保存 Base URL、API Key、模型、主题等配置，不保存导入图片列表和预览结果。
- 日间 / 夜间主题：圆角玻璃风格界面。

## 下载使用

到 GitHub Releases 下载最新的 Windows 安装包：

```text
图片自动命名器 Lite_*_x64-setup.exe
```

双击安装后打开即可。当前安装包未做代码签名，Windows 可能会显示安全提醒，确认来源可信后选择继续运行。

## AI 配置

应用兼容 OpenAI 风格接口：

- Base URL 示例：`https://api.openai.com/v1`
- 本地 Ollama 示例：`http://localhost:11434/v1`
- 本地视觉模型示例：`llava`

填写 Base URL 和 API Key 后，可以点击模型列表获取可用模型。使用本地 Ollama 时通常不需要 API Key，但需要本机先运行对应视觉模型。

## 本地预览

Web 预览只适合看界面。本机文件选择、图片重命名等功能需要 Tauri 桌面窗口。

```ps1
npm.cmd install
npm.cmd run web
```

或双击：

```text
run-web.cmd
```

## 桌面开发

Windows 开发机可以先运行一键环境配置：

```text
setup-env.cmd
```

它会检查并尽量自动安装：

- Node.js / npm
- Rust / Cargo
- Visual Studio Build Tools / C++ linker
- Microsoft Edge WebView2 Runtime
- 项目 npm 依赖

启动桌面开发版：

```text
run-tauri.cmd
```

停止开发进程：

```text
stop-dev.cmd
```

更多开发说明见 [docs/DEVELOPMENT.md](docs/DEVELOPMENT.md)。

## 发布

本地生成 Windows 安装包：

```text
release.cmd
```

产物路径：

```text
src-tauri\target\release\bundle\nsis\
```

也可以推送 Git tag 触发 GitHub Actions 自动发布：

```ps1
git tag v0.2.0
git push origin v0.2.0
```

更多发布说明见 [docs/PUBLISHING.md](docs/PUBLISHING.md)。

## 配置存储

应用会把配置和撤销记录保存在系统用户配置目录下的：

```text
image-renamer-lite-tauri
```

保存内容包括命名输入、Base URL、API Key、模型、AI 命名格式、识别范围和主题。

不会保存导入图片列表，也不会保存上次生成的预览结果。

## License

[MIT](LICENSE)
