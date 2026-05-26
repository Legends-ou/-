# 项目根目录说明

本目录是 `图片自动命名器 Lite` 的 GitHub 仓库根目录，保留源码、配置、脚本、文档和当前 Windows 发布包。

## 关键文件

- `package.json`：前端依赖、NPM 脚本和项目版本。
- `package-lock.json`：锁定 Node 依赖版本，GitHub/本机安装依赖时使用。
- `index.html`：Vite 前端入口 HTML。
- `vite.config.ts`：Vite 开发服务器和构建配置，默认端口 `5173`。
- `tsconfig.json`、`tsconfig.node.json`：TypeScript 编译配置。
- `README.md`：项目介绍和使用说明。
- `CHANGELOG.md`：版本变更记录。
- `LICENSE`：MIT 许可证。
- `SECURITY.md`：安全反馈说明。
- `UPLOAD_MANIFEST.md`：GitHub 上传/发布清单。

## 常用命令

- `npm install`：安装前端依赖。
- `npm run dev`：启动网页开发预览。
- `npm run build`：生成前端生产文件到 `dist/`。
- `npm run tauri -- build`：生成 Tauri 桌面发布包。
- `npm run release -- -SkipInstall`：使用脚本检查环境并构建发布包。

## 本地生成物

`node_modules/`、`dist/`、`src-tauri/target/`、`src-tauri/gen/` 都是可重新生成目录，不应该作为源码长期保留。
