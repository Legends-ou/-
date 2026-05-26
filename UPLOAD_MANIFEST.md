# GitHub 上传清单

上传 GitHub 时，请上传这个项目的源码文件和配置文件，不要上传本地依赖、构建产物或安装包缓存。

## 根目录文件

这些文件需要上传到仓库根目录：

- `.gitattributes`
- `.gitignore`
- `CHANGELOG.md`
- `LICENSE`
- `README.md`
- `SECURITY.md`
- `index.html`
- `package.json`
- `package-lock.json`
- `release.cmd`
- `run-tauri.cmd`
- `run-web.cmd`
- `setup-env.cmd`
- `stop-dev.cmd`
- `tsconfig.json`
- `tsconfig.node.json`
- `vite.config.ts`

## 前端源码

上传整个 `src` 文件夹：

- `src/App.tsx`
- `src/main.tsx`
- `src/styles.css`

## Tauri / Rust 源码

上传整个 `src-tauri` 文件夹，但不要上传 `src-tauri/target` 和 `src-tauri/gen`。

需要包含：

- `src-tauri/Cargo.toml`
- `src-tauri/Cargo.lock`
- `src-tauri/build.rs`
- `src-tauri/tauri.conf.json`
- `src-tauri/capabilities/default.json`
- `src-tauri/icons/icon.ico`
- `src-tauri/src/commands.rs`
- `src-tauri/src/lib.rs`
- `src-tauri/src/main.rs`

## 脚本

上传整个 `scripts` 文件夹：

- `scripts/setup-env.ps1`
- `scripts/release.ps1`
- `scripts/stop-dev.ps1`

## 文档

上传整个 `docs` 文件夹：

- `docs/DEVELOPMENT.md`
- `docs/PUBLISHING.md`

## GitHub 配置

上传整个 `.github` 文件夹：

- `.github/workflows/ci.yml`
- `.github/workflows/release.yml`
- `.github/ISSUE_TEMPLATE/bug_report.yml`
- `.github/ISSUE_TEMPLATE/feature_request.yml`
- `.github/pull_request_template.md`

## 不要上传

这些是本地生成内容，不要上传：

- `node_modules`
- `dist`
- `src-tauri/target`
- `src-tauri/gen`
- `.env`
- `.env.*`
- `*.p12`
- `*.pfx`
- `*.pem`
- `*.key`
- `*.log`
- 生成出来的安装包 `.exe`

## 推荐上传方式

最稳妥的方式是用 Git 命令上传整个项目目录。`.gitignore` 会自动排除不该上传的内容。

如果用 GitHub 网页上传，请上传 `image-renamer-tauri-github-upload` 文件夹里面的所有内容，而不是上传 zip 文件本身。
