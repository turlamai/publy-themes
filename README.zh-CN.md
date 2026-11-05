# Publy 主题预览

[English](README.md) · **中文**

本仓库展示 Publy 内置文章主题和图片卡片主题的预览及说明。索引用于展示，不是安装源；当前 Publy 开发版命令行列出本地主题时不会读取这里的索引。

## 独立文章主题

Publy 正在准备纯内容、带版本的 JSON 文章主题包，目前仍属于未发布的开发候选。请查看 [Publy 用户指南](https://github.com/turlamai/publy/blob/main/docs/USER-GUIDE.zh-CN.md)，确认你使用的版本支持什么功能。当前主题站不提供主题下载、自动更新、作者身份验证或签名目录；此格式暂不支持外部卡片主题包。

在支持主题包的构建版本中，作者可用以下命令校验和打包限定作用域的 CSS：

```sh
publy theme pack my.css --id my-style --theme-version 1.0.0 --name "我的主题" --license MIT --output my-style.json
```

分享时请一并提供许可证和预览图。用户可通过 `publy theme add ./my-style.json` 安装本地主题包，再用 `publy theme preview my-style` 预览。通过 HTTPS 获取时，必须从独立可信渠道获取并提供 `--sha256`；摘要只核对文件内容，不证明作者身份。主题包只接受限定在 `#publy` 内的一小部分 CSS，不执行软件包代码。

外部主题提交流程与主题站分发尚未开放，请不要将 npm 软件包作为主题包提交。
