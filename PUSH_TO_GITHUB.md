# GitHub 推送命令

## 执行以下命令推送到 GitHub

打开 PowerShell，执行：

```powershell
cd C:\Users\JW3\Documents\Qieman-MCP
git push origin main
```

## 输入认证信息

系统会提示您输入：
- **用户名**：Chris1Wang3
- **密码**：使用 Personal Access Token（不是 GitHub 密码）

## 如果没有 Personal Access Token

1. 访问：https://github.com/settings/tokens
2. 点击 "Generate new token" → "Generate new token (classic)"
3. 勾选 `repo` 权限
4. 生成并复制 Token
5. 在 git push 时，密码处粘贴 Token

## 推送成功后

访问查看：https://github.com/Chris1Wang3/Qieman-MCP

---

**或者我帮您打开 GitHub 仓库页面，您可以直接在网页上传文件**
