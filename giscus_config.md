# Giscus评论系统配置指南

## 什么是Giscus？
Giscus是一个基于GitHub Discussions的评论系统，允许访客在您的博客文章下留下评论。

## 配置步骤

### 1. 准备GitHub仓库
- 创建一个公共GitHub仓库（例如：`yourusername/comments`）
- 或者使用您现有的公共仓库

### 2. 启用Discussions
- 访问仓库设置页面
- 在"Features"部分启用"Discussions"

### 3. 获取Giscus配置参数
访问 https://giscus.app 并按以下方式配置：
- Repository: `yourusername/comments` （您的仓库地址）
- Select the Discussion Category: `Announcements` （或其他类别）
- Mapping: `Specific mapping` -> `pathname`
- Theme: `light` 或其他主题
- Language: `zh-CN` （中文）

## Giscus配置参数示例
以下是配置完成后获得的HTML代码片段，您需要在后续步骤中使用这些参数：

```html
<script src="https://giscus.app/client.js"
        data-repo="yourusername/comments"
        data-repo-id="your-repo-id"
        data-category="Announcements"
        data-category-id="your-category-id"
        data-mapping="pathname"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="bottom"
        data-theme="light"
        data-lang="zh-CN"
        crossorigin="anonymous"
        async>
</script>
```

## 注意事项
- 请将示例中的参数替换为您自己的实际参数
- 首次部署后，Giscus会在对应的文章路径下自动创建Discussion