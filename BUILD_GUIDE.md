# 使用 GitHub Actions 构建指南

## 📋 前提条件

1. 拥有 GitHub 账号
2. Fork 这个仓库到你自己的账号

## 🚀 步骤

### 1. Fork 仓库

1. 访问 https://github.com/hj01857655/kiro-account-manager
2. 点击右上角的 "Fork" 按钮
3. 等待 Fork 完成

### 2. 启用 GitHub Actions

1. 进入你 Fork 的仓库
2. 点击 "Actions" 标签
3. 如果看到提示，点击 "I understand my workflows, go ahead and enable them"

### 3. 触发构建

有两种方式触发构建：

#### 方式 A：手动触发（推荐）

1. 在你的仓库中，点击 "Actions" 标签
2. 在左侧选择 "Build Application" 工作流
3. 点击右侧的 "Run workflow" 按钮
4. 选择分支（通常是 main 或 master）
5. 点击绿色的 "Run workflow" 按钮

#### 方式 B：推送代码触发

1. 克隆你 Fork 的仓库到本地
2. 进行任何修改（或创建空提交）
3. 推送到 GitHub

```bash
git clone https://github.com/你的用户名/kiro-account-manager.git
cd kiro-account-manager
git commit --allow-empty -m "触发构建"
git push
```

### 4. 等待构建完成

1. 在 "Actions" 标签中查看构建进度
2. 构建时间约 10-20 分钟（取决于 GitHub 服务器负载）
3. 会同时构建 Windows 和 macOS 版本

### 5. 下载构建产物

构建完成后：

1. 点击完成的工作流运行
2. 滚动到页面底部的 "Artifacts" 部分
3. 下载对应平台的文件：
   - `app-windows-latest-default` - Windows 版本
   - `app-macos-latest-x86_64-apple-darwin` - macOS Intel 版本
   - `app-macos-latest-aarch64-apple-darwin` - macOS Apple Silicon 版本

### 6. 安装应用

#### Windows
1. 解压下载的 zip 文件
2. 在 `bundle/msi/` 或 `bundle/nsis/` 目录中找到安装程序
3. 双击 `.msi` 或 `.exe` 文件安装

#### macOS
1. 解压下载的 zip 文件
2. 在 `bundle/dmg/` 目录中找到 `.dmg` 文件
3. 双击打开并拖动到 Applications 文件夹

## 📝 注意事项

- 构建产物会保留 90 天
- 每次推送代码都会触发新的构建
- 如果构建失败，检查 Actions 日志查看错误信息
- GitHub 免费账户每月有 2000 分钟的 Actions 使用时间

## 🔧 故障排除

### 构建失败
- 检查 Actions 日志中的错误信息
- 确保仓库中的代码完整且没有语法错误
- 可能需要等待几分钟后重试

### 找不到构建产物
- 确保工作流运行完成（绿色勾号）
- 检查是否有错误导致构建中断
- 某些步骤失败可能不会生成产物

## 💡 提示

- 可以修改 `.github/workflows/build.yml` 来自定义构建流程
- 如果只需要 Windows 版本，可以删除 macOS 相关的配置以节省时间
- 建议在本地测试代码后再推送，避免浪费 Actions 时间

## 📞 获取帮助

如果遇到问题：
1. 查看 GitHub Actions 日志
2. 在原仓库提交 Issue
3. 加入 QQ 群：1020204332