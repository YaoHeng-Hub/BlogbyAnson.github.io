# 个人博客

基于Hugo静态网站生成器构建的个人博客，使用GitHub Pages托管，支持Giscus评论系统。

## 项目特点

- 响应式设计，适配各种设备
- 快速加载，性能优秀
- 支持评论功能
- 自动化部署

## 技术栈

- [Hugo](https://gohugo.io/) - 静态网站生成器
- [Ananke主题](https://github.com/theNewDynamic/gohugo-theme-ananke) - 博客主题
- [GitHub Pages](https://pages.github.com/) - 免费托管服务
- [GitHub Actions](https://github.com/features/actions) - 自动化部署
- [Giscus](https://giscus.app/) - 基于GitHub Discussions的评论系统

## 本地开发

1. 安装[Hugo Extended](https://gohugo.io/getting-started/installing/)（必须是Extended版本）
2. 克隆项目
3. 运行 `hugo server -D` 启动本地服务器

## 部署到GitHub Pages

项目已配置GitHub Actions自动部署，当推送到main分支时会自动构建并发布到GitHub Pages。

注意：首次部署可能需要手动触发。

## 配置Giscus评论系统

1. 访问 [giscus.app](https://giscus.app/)
2. 按照向导配置您的仓库
3. 将生成的参数填入 `hugo.toml` 文件中的 `[params.giscus]` 部分

## 自定义配置

编辑 `hugo.toml` 文件可以配置：

- 网站标题、描述
- 社交媒体链接
- Giscus评论系统参数
- 菜单导航
- 其他主题选项

## 内容管理

- 文章保存在 `content/posts/` 目录
- 页面保存在 `content/` 根目录
- 使用Markdown格式编写内容

## 最佳实践

- 提交前确保本地构建无误
- 定期备份内容
- 使用有意义的commit消息
- 保持主题更新