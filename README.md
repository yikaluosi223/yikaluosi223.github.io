# 数字花园 - 个人博客与知识库

基于 Hugo + Obsidian 的个人博客，用于知识学习资料及成果管理。

## 技术栈

- **Hugo** — 静态网站生成器
- **PaperMod** — Hugo 主题
- **Obsidian** — Markdown 编辑器，content 目录即 Obsidian Vault
- **GitHub Pages** — 自动部署

## 快速开始

### 前置要求

- [Hugo Extended](https://gohugo.io/installation/) (>= 0.140.0)
- [Obsidian](https://obsidian.md/) (可选，用于编辑内容)

### 本地运行

```bash
# 克隆仓库
git clone --recursive https://github.com/<username>/<username>.github.io.git
cd <username>.github.io

# 启动开发服务器
hugo server -D

# 访问 http://localhost:1313/
```

### 用 Obsidian 编辑内容

1. 打开 Obsidian
2. 选择 "打开文件夹作为 Vault"
3. 选择 `content/` 目录
4. 开始写作！

### 部署

推送到 `main` 分支，GitHub Actions 会自动构建并部署到 GitHub Pages。

## 目录结构

```
.
├── content/          # Hugo 内容 + Obsidian Vault
│   ├── posts/        # 博客文章
│   ├── notes/        # Zettelkasten 笔记
│   │   ├── permanent/  # 常青笔记
│   │   └── literature/ # 文献笔记
│   └── projects/     # 项目文档
├── layouts/          # 自定义模板
│   ├── _default/_markup/  # 渲染钩子 (wikilink, callout)
│   └── partials/     # 部分模板 (backlinks, wikilink processor)
├── assets/css/extended/  # 自定义 CSS
├── themes/PaperMod/  # 主题 (git submodule)
└── .github/workflows/    # GitHub Actions 部署
```

## 特性

- ✅ Obsidian wikilink 双向链接
- ✅ Obsidian 风格 Callout 渲染
- ✅ 反向链接显示
- ✅ 中文排版优化
- ✅ 暗色模式
- ✅ 标签系统
- ✅ 全文搜索 (Fuse.js)
- ✅ 自动部署
