---
title: "Hugo 搭建笔记：从零到上线只需 5 分钟"
date: 2026-05-01
description: "记录用 Hugo + Stack 主题搭建个人博客的完整过程。"
categories: ["技术"]
tags: ["Hugo", "博客搭建", "教程"]
author: "Me"
---

## 为什么选 Hugo？

在 Hugo、Hexo、Astro 之间纠结了一圈，最终选了 Hugo：

- **构建速度**：1000 篇文章 < 1 秒，Hexo 要 30 秒+
- **单二进制**：不需要 Node.js、不需要 npm，一个 hugo 命令搞定一切
- **模板语言**：Go templates 比 Hexo 的 EJS/Nunjucks 更简洁

<!--more-->

## 搭建步骤

### 1. 安装 Hugo

```bash
# macOS
brew install hugo

# Linux (snap)
snap install hugo

# 或者直接下载二进制
# https://github.com/gohugoio/hugo/releases
```

### 2. 创建站点

```bash
hugo new site my-blog
cd my-blog
git init
```

### 3. 安装 Stack 主题

```bash
git submodule add https://github.com/CaiJimmy/hugo-theme-stack.git themes/stack
```

### 4. 配置

编辑 `hugo.toml`，设置语言、菜单、参数。Stack 主题的文档非常详细。

### 5. 写文章

```bash
hugo new posts/my-first-post.md
```

然后用你喜欢的编辑器打开写就行。

### 6. 本地预览

```bash
hugo server -D
```

打开 `http://localhost:1313` 即可看到效果。

### 7. 部署到 GitHub Pages

```bash
hugo --minify
# 将 public/ 目录推送到 GitHub Pages 仓库
```

## 性能表现

构建速度测试：

```
hugo --minify
████████████████████████████████████████ 100%
Started in 47ms
```

47 毫秒。这就是选择 Hugo 的理由。

---

> 一个能让你专注于写作而不是折腾工具的博客系统，才是好系统。
