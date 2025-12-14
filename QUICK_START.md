# 🚀 快速开始指南

## 方案选择

你现在有两个选择来获取这个应用：

### ✅ 方案 1：使用 GitHub Actions 构建（推荐，无需本地环境）

**优点：**
- ✅ 不需要在本地安装任何开发环境
- ✅ 不占用本地磁盘空间
- ✅ GitHub 服务器自动构建
- ✅ 可以构建 Windows 和 macOS 版本

**步骤：**
1. Fork 这个仓库到你的 GitHub 账号
2. 按照 `BUILD_GUIDE.md` 中的说明操作
3. 等待 10-20 分钟构建完成
4. 下载构建好的安装包

**详细教程：** 查看 [BUILD_GUIDE.md](BUILD_GUIDE.md)

---

### 方案 2：本地构建（需要开发环境）

**需要安装：**
- Node.js 18+ (你已安装 ✅)
- Rust 工具链 (约 1-2GB)
- Git (你已安装 ✅)

**优点：**
- 可以修改代码
- 构建速度可能更快（取决于网络）
- 可以调试问题

**缺点：**
- 需要安装 Rust (1-2GB)
- 首次构建需要下载依赖

**步骤：**

#### 2.1 安装 Rust

访问 https://rustup.rs/ 下载安装器，或运行：

```bash
# Windows (PowerShell)
Invoke-WebRequest -Uri https://win.rustup.rs/x86_64 -OutFile rustup-init.exe
.\rustup-init.exe
```

#### 2.2 构建应用

```bash
# 进入项目目录
cd kiro-account-manager

# 安装依赖
npm install

# 开发模式运行（测试）
npm run tauri dev

# 构建生产版本
npm run tauri build
```

#### 2.3 查找构建产物

构建完成后，安装包位于：
- Windows: `src-tauri/target/release/bundle/msi/` 或 `src-tauri/target/release/bundle/nsis/`
- 文件类型: `.msi` 或 `.exe`

---

## 🎯 我的建议

**如果你：**
- ❌ 不想安装开发环境 → 选择方案 1（GitHub Actions）
- ❌ 磁盘空间有限 → 选择方案 1
- ✅ 想要修改代码 → 选择方案 2（本地构建）
- ✅ 经常需要构建项目 → 选择方案 2

**大多数用户推荐：方案 1（GitHub Actions）**

---

## 📞 需要帮助？

- 📖 GitHub Actions 构建：查看 [BUILD_GUIDE.md](BUILD_GUIDE.md)
- 💬 QQ 群：1020204332
- 🐛 问题反馈：https://github.com/hj01857655/kiro-account-manager/issues

---

## ⚡ 下一步

1. 选择你的方案
2. 按照对应的指南操作
3. 开始使用 Kiro Account Manager！