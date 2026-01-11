# 部署指南

## 第一步：在GitHub上创建仓库

1. 访问 https://github.com/new
2. 仓库名：`BlogbyAnson.github.io`
3. 设置为Public
4. 不要勾选"Initialize this repository with a README"
5. 点击"Create repository"

## 第二步：推送代码

如果仓库已存在，使用以下命令推送：

```bash
git push -u origin main
```

如果遇到权限错误，可能需要配置GitHub认证：
- 使用HTTPS：配置Personal Access Token作为密码
- 使用SSH：确保已添加SSH密钥到GitHub账户

## 第三步：启用GitHub Pages

1. 在仓库页面点击"Settings"
2. 向下滚动到"Pages"部分
3. Source选择"Deploy from a branch"
4. 分支选择"main"并"/ (root)"文件夹
5. 点击"Save"

## 第四步：配置Giscus

1. 确保您的仓库已启用Discussions功能
   - 在仓库"Settings"中找到"General"
   - 向下滚动到"Features"部分
   - 启用"Discussions"
2. 访问 https://giscus.app/
3. 输入仓库名：`YaoHeng-Hub/BlogbyAnson.github.io`
4. 配置偏好设置（语言选择"简体中文"）
5. 复制生成的代码片段
6. 更新hugo.toml中的giscus配置参数

## 故障排除

### 如果推送失败：
- 检查仓库名是否正确：`BlogbyAnson.github.io`
- 确保没有网络连接问题
- 验证GitHub认证凭据

### 如果网站未显示：
- 确认GitHub Pages已启用
- 检查GitHub Actions工作流是否成功运行
- 等待几分钟让部署生效

### 如果菜单链接失效：
- 检查hugo.toml中的baseURL和菜单URL配置
- 确保它们与GitHub Pages的URL结构匹配