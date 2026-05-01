# 我的博客

基于 [Hugo](https://gohugo.io) + [Stack](https://github.com/CaiJimmy/hugo-theme-stack) 主题搭建的个人博客。

## 技术栈

- **框架**: Hugo v0.161.1 (Extended)
- **主题**: hugo-theme-stack v3
- **部署**: GitHub Pages / Vercel / Cloudflare Pages

## 本地运行

```bash
# 安装 Hugo (macOS)
brew install hugo

# 克隆仓库
git clone --recursive https://github.com/yourname/blog.git
cd blog

# 启动开发服务器
hugo server -D

# 打开 http://localhost:1313
```

## 写文章

```bash
hugo new posts/my-new-post.md
```

用任意编辑器打开 `content/posts/my-new-post.md`，用 Markdown 写作。

## 构建部署

```bash
hugo --minify
# 输出在 public/ 目录
```

## 目录结构

```
blog/
├── config/_default/   # 配置文件
├── content/           # 内容
│   ├── posts/         # 文章
│   ├── about/         # 关于页面
│   ├── search.md      # 搜索页
│   └── archives.md    # 归档页
├── static/            # 静态资源
│   └── img/           # 图片
├── themes/stack/      # 主题
└── hugo.toml          # 主配置
```

## License

CC BY-NC-SA 4.0
