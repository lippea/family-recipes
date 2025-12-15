# Family Recipes - 家庭菜单网站

使用 Hugo + GitHub Pages + GitHub Actions 构建的低维护成本家庭菜单网站。

## 功能特性

- ✅ 分类浏览
- ✅ 标签筛选
- ✅ 实时搜索
- ✅ 响应式设计
- ✅ 自动部署

## 本地开发

### 前置要求

- [Hugo Extended](https://gohugo.io/installation/) (推荐最新版本)
- Node.js (用于搜索功能)

### 安装依赖

```bash
npm install
```

### 运行本地服务器

```bash
npm run dev
```

访问 http://localhost:1313 查看网站

### 构建静态文件

```bash
npm run build
```

生成的文件在 `public/` 目录

## 添加新菜单

在 `content/` 目录下创建新的 Markdown 文件，例如：

```markdown
---
title: "菜单名称"
date: 2024-01-01
categories: ["主菜"]
tags: ["标签1", "标签2"]
difficulty: "简单"
servings: 4
description: "菜单描述"
---

## 食材
- 食材1
- 食材2

## 步骤
1. 步骤1
2. 步骤2
```

## 部署到 GitHub Pages

### 1. 创建 GitHub 仓库

在 GitHub 上创建一个新仓库（例如：`family-recipes`）

### 2. 更新配置

编辑 `config.toml`，将 `baseURL` 改为你的仓库地址：

```toml
baseURL = 'https://YOUR_USERNAME.github.io/family-recipes/'
```

### 3. 推送代码

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/family-recipes.git
git push -u origin main
```

### 4. 配置 GitHub Pages

1. 进入仓库 Settings
2. 点击左侧 Pages
3. 在 Source 选择 "GitHub Actions"
4. 保存设置

### 5. 自动部署

GitHub Actions 会自动构建并部署网站。首次部署可能需要几分钟。

部署完成后，访问 `https://YOUR_USERNAME.github.io/family-recipes/` 即可看到网站。

## 项目结构

```
family-recipes/
├── config.toml              # Hugo 配置文件
├── content/                # 菜单内容（Markdown 文件）
├── layouts/
│   └── _default/            # 模板文件
├── .github/
│   └── workflows/
│       └── deploy.yml       # GitHub Actions 工作流
└── package.json             # Node.js 依赖
```

## 维护

- **添加菜单**：在 `content/` 目录下添加 Markdown 文件，push 到 GitHub 即可自动部署
- **修改样式**：编辑 `layouts/_default/baseof.html` 中的 CSS
- **修改配置**：编辑 `config.toml`

## 许可证

MIT

