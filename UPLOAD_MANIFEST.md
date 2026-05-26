# GitHub 上传清单

上传 GitHub 仓库源码时，请上传这个项目的源码文件和配置文件，不要上传本地依赖、构建产物或安装包缓存。发布安装包请作为 GitHub Release assets 单独上传。

## 根目录文件

这些文件需要上传到仓库根目录：

- `.gitattributes`
- `.gitignore`
- `CHANGELOG.md`
- `how.md`
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
- `src/how.md`
- `src/main.tsx`
- `src/styles.css`

## Tauri / Rust 源码

上传整个 `src-tauri` 文件夹，但不要上传 `src-tauri/target` 和 `src-tauri/gen`。

需要包含：

- `src-tauri/Cargo.toml`
- `src-tauri/Cargo.lock`
- `src-tauri/build.rs`
- `src-tauri/how.md`
- `src-tauri/tauri.conf.json`
- `src-tauri/capabilities/default.json`
- `src-tauri/capabilities/how.md`
- `src-tauri/icons/how.md`
- `src-tauri/icons/icon.ico`
- `src-tauri/src/commands.rs`
- `src-tauri/src/how.md`
- `src-tauri/src/lib.rs`
- `src-tauri/src/main.rs`

## 脚本

上传整个 `scripts` 文件夹：

- `scripts/how.md`
- `scripts/setup-env.ps1`
- `scripts/release.ps1`
- `scripts/stop-dev.ps1`

## 文档

上传整个 `docs` 文件夹：

- `docs/DEVELOPMENT.md`
- `docs/how.md`
- `docs/PUBLISHING.md`

## GitHub 配置

上传整个 `.github` 文件夹：

- `.github/how.md`
- `.github/workflows/ci.yml`
- `.github/workflows/release.yml`
- `.github/ISSUE_TEMPLATE/bug_report.yml`
- `.github/ISSUE_TEMPLATE/feature_request.yml`
- `.github/ISSUE_TEMPLATE/how.md`
- `.github/workflows/how.md`
- `.github/pull_request_template.md`

## GitHub Release 资产

`github-release-v0.2.2` 是本地整理好的 Release 资产目录，不建议提交进源码仓库。发布到 GitHub Release 时，上传该目录内这些文件：

- `github-release-v0.2.2/图片自动命名器 Lite_0.2.2_x64-setup.exe`
- `github-release-v0.2.2/SHA256SUMS.txt`
- `github-release-v0.2.2/RELEASE_NOTES.md`

`github-release-v0.2.2/how.md` 只解释该目录用途，本身不需要作为 Release asset 上传。

## 不要上传

这些是本地生成内容，不要上传：

- `node_modules`
- `dist`
- `src-tauri/target`
- `src-tauri/gen`
- `github-release-*`
- `github-upload-ready`
- `.env`
- `.env.*`
- `*.p12`
- `*.pfx`
- `*.pem`
- `*.key`
- `updater.key`
- `updater.key.pub`
- `*.log`
- 生成出来的安装包 `.exe`

## 推荐上传方式

最稳妥的方式是用 Git 命令上传整个项目目录。`.gitignore` 会自动排除不该上传的内容。

如果用 GitHub 网页上传源码，请上传当前项目根目录中除“不要上传”列表以外的文件和文件夹；安装包请到 Release 页面单独上传。
