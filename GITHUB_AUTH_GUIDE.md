# GitHub身份验证指南
# GitHub Authentication Guide

## 🔐 解决GitHub推送认证问题

由于GitHub不再支持密码认证，您需要使用个人访问令牌(Personal Access Token)来推送代码。

## 📋 步骤1: 创建GitHub个人访问令牌

### 1. 登录GitHub
- 访问 [https://github.com](https://github.com)
- 使用您的账号 `Jackiezyj` 登录

### 2. 进入设置页面
- 点击右上角头像
- 选择 "Settings"

### 3. 创建访问令牌
- 左侧菜单选择 "Developer settings"
- 点击 "Personal access tokens"
- 选择 "Tokens (classic)"
- 点击 "Generate new token (classic)"

### 4. 配置令牌
- **Note**: `megestrol-data-mining-token`
- **Expiration**: 选择 "90 days" 或 "No expiration"
- **Scopes**: 勾选以下权限：
  - ✅ `repo` (完整的仓库访问权限)
  - ✅ `workflow` (可选，如果需要GitHub Actions)

### 5. 生成令牌
- 点击 "Generate token"
- **重要**: 立即复制生成的令牌，它只会显示一次！

## 🔧 步骤2: 配置Git认证

### 方法1: 使用令牌作为密码
```bash
# 推送时使用令牌作为密码
git push -u origin megestrol-data-mining

# 当提示输入用户名和密码时：
# Username: Jackiezyj
# Password: [粘贴您的个人访问令牌]
```

### 方法2: 存储凭据 (推荐)
```bash
# 配置Git凭据存储
git config --global credential.helper store

# 然后推送，输入一次凭据后会自动保存
git push -u origin megestrol-data-mining
```

### 方法3: 在URL中直接使用令牌
```bash
# 重新设置远程仓库URL，包含令牌
git remote set-url origin https://Jackiezyj:YOUR_TOKEN@github.com/Jackiezyj/-.git

# 然后推送
git push -u origin megestrol-data-mining
```

## 🚀 步骤3: 推送代码

配置好认证后，执行以下命令：

```bash
# 推送新分支到GitHub
git push -u origin megestrol-data-mining

# 如果成功，您会看到类似输出：
# Branch 'megestrol-data-mining' set up to track remote branch 'megestrol-data-mining' from 'origin'.
# To https://github.com/Jackiezyj/-.git
#  * [new branch]      megestrol-data-mining -> megestrol-data-mining
```

## 🔄 步骤4: 设置默认分支

推送成功后，您需要在GitHub上设置默认分支：

1. 访问 [https://github.com/Jackiezyj/-](https://github.com/Jackiezyj/-)
2. 点击 "Settings" 标签
3. 左侧菜单选择 "Branches"
4. 在 "Default branch" 部分：
   - 点击切换按钮
   - 选择 `megestrol-data-mining`
   - 点击 "Update"
   - 确认更改

## 🛠️ 故障排除

### 问题1: 令牌无效
- 检查令牌是否过期
- 确认令牌有正确的权限
- 重新生成令牌

### 问题2: 权限不足
- 确认令牌包含 `repo` 权限
- 检查您是否有仓库的写入权限

### 问题3: 网络问题
- 检查网络连接
- 尝试使用VPN
- 检查防火墙设置

## 📱 移动端认证

如果您在移动设备上操作，也可以：

1. 使用GitHub移动应用
2. 通过GitHub CLI工具
3. 使用GitHub Desktop客户端

## 🔒 安全建议

1. **定期更新令牌**: 建议90天更新一次
2. **限制权限**: 只授予必要的权限
3. **不要分享**: 令牌等同于密码，请保密
4. **监控使用**: 定期检查令牌的使用情况

## 📞 获取帮助

如果仍然遇到问题：

1. 检查 [GitHub帮助文档](https://docs.github.com/en/authentication)
2. 查看 [GitHub状态页面](https://www.githubstatus.com/)
3. 在 [GitHub社区](https://github.com/orgs/community/discussions) 寻求帮助

---

## 🎯 快速操作清单

- [ ] 创建GitHub个人访问令牌
- [ ] 配置Git认证方式
- [ ] 推送代码到GitHub
- [ ] 设置默认分支
- [ ] 验证仓库内容

完成以上步骤后，您的甲地孕酮数据挖掘项目就成功上传到GitHub了！🎉

---

*最后更新: 2025年1月*
