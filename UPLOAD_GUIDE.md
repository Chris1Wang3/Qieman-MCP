# GitHub 仓库上传指南

## 前提条件

1. 确保您已在 GitHub 上创建了仓库 `Qieman-MCP`
   - 访问：https://github.com/new
   - 仓库名：Qieman-MCP
   - 设置为 Public
   - **不要**勾选 "Add a README file"

## 上传步骤

### 方式一：使用 HTTPS（推荐）

在 PowerShell 或命令提示符中执行以下命令：

```powershell
# 1. 进入项目目录
cd C:\Users\JW3\Documents\Qieman-MCP

# 2. 初始化 Git 仓库
git init

# 3. 添加所有文件
git add .

# 4. 提交更改
git commit -m "Initial commit: Add Qieman MCP Server with comprehensive README"

# 5. 添加远程仓库
git remote add origin https://github.com/Chris1Wang3/Qieman-MCP.git

# 6. 推送到 GitHub（首次推送）
git push -u origin main
```

**注意**：执行 `git push` 时，系统会提示您输入 GitHub 用户名和密码（或 Personal Access Token）

### 方式二：使用 SSH

如果您已配置 SSH 密钥：

```powershell
# 1-4 步骤同上

# 5. 添加远程仓库（SSH）
git remote add origin git@github.com:Chris1Wang3/Qieman-MCP.git

# 6. 推送到 GitHub
git push -u origin main
```

## 如果仓库已存在

如果您之前已创建过仓库，需要先删除旧的远程关联：

```powershell
git remote remove origin
git remote add origin https://github.com/Chris1Wang3/Qieman-MCP.git
git push -u origin main
```

## 验证上传

上传成功后，访问以下链接查看：
https://github.com/Chris1Wang3/Qieman-MCP

## 后续更新

以后更新文件时，使用以下命令：

```powershell
git add .
git commit -m "Update: 描述您的更改"
git push
```

## 常见问题

### 1. 如果提示需要 Personal Access Token

GitHub 已不再支持密码认证，需要使用 Personal Access Token：

1. 访问：https://github.com/settings/tokens
2. 点击 "Generate new token" → "Generate new token (classic)"
3. 勾选 `repo` 权限
4. 生成并复制 Token
5. 在 `git push` 时，用户名填 `Chris1Wang3`，密码填入 Token

### 2. 如果提示分支名称问题

如果默认分支是 `master` 而不是 `main`：

```powershell
git branch -M main
git push -u origin main
```

### 3. 如果需要强制推送（谨慎使用）

```powershell
git push -f origin main
```

---

**准备就绪！** 现在您可以按照上述步骤将代码推送到 GitHub 了。
