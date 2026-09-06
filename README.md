# zerotier-ish-build

在 GitHub Actions 上为 iSH（iOS Linux shell）静态编译 ZeroTier One aarch64 musl 二进制。

## 产物

每次构建输出三个静态链接的 aarch64 musl 二进制文件：

- `zerotier-one` — ZeroTier 守护进程
- `zerotier-cli` — 命令行工具
- `zerotier-idtool` — 密钥生成工具

## 构建方式

使用 `ubuntu-latest` amd64 runner，通过 `gcc-aarch64-linux-musl` 交叉编译工具链直接编译 aarch64 musl 静态二进制，无需 Docker 或 QEMU 模拟。

触发方式：手动点击 Actions tab 的 **Run workflow**，或 push 到 `main` 分支自动触发。
