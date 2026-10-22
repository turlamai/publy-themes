# Publy Theme Registry

[English](README.md) · **中文**

精选的 Publy 主题索引（文章主题用于 Markdown → 微信 HTML，卡片主题用于图片帖 3:4 PNG 套图）。`publy theme ls` 会读取本仓库的 `index.json`。

## 格式

```json
{
  "version": 1,
  "themes": [
    { "id": "my-theme", "kind": "article | card", "source": "builtin | npm", "npm": "@scope/publy-theme-my-theme", "description": "..." }
  ]
}
```

## 提交主题

1. 将主题发布为名为 `publy-theme-*` 的 npm 包（文章主题：作用域限定在 `#publy` 下的 CSS；卡片主题：一个 `CardTheme` 风格配置模块）。
2. 在包的 README 中附上渲染后的预览图。
3. 提交 PR，在 `index.json` 中添加一个条目。

外部主题提交将在 M4 开放；在此之前，注册表仅列出内置主题。
