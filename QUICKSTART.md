# 快速开始指南

## 本地测试

1. **安装 Hugo Extended**
   ```bash
   # macOS
   brew install hugo
   
   # 或访问 https://gohugo.io/installation/
   ```

2. **运行本地服务器**
   ```bash
   hugo server -D
   ```
   访问 http://localhost:1313

## 部署到 GitHub Pages

### 第一步：创建 GitHub 仓库

1. 在 GitHub 上创建新仓库（例如：`family-recipes`）
2. 注意：如果仓库名不是 `family-recipes`，需要修改 `config.toml` 中的 `baseURL`

### 第二步：更新配置

编辑 `config.toml`，修改 `baseURL`：

```toml
baseURL = 'https://YOUR_USERNAME.github.io/family-recipes/'
```

将 `YOUR_USERNAME` 替换为你的 GitHub 用户名。

### 第三步：推送代码

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:lippea/family-recipes.git
git branch -M main
git push -u origin main
```

### 第四步：配置 GitHub Pages

1. 进入仓库 Settings
2. 点击左侧 **Pages**
3. 在 **Source** 选择 **GitHub Actions**
4. 保存设置

### 第五步：等待部署

GitHub Actions 会自动构建并部署。首次部署需要 2-5 分钟。

部署完成后访问：`https://YOUR_USERNAME.github.io/family-recipes/`

## 添加新菜单

在 `content/` 目录下创建新的 `.md` 文件：

```bash
hugo new 新菜单名称.md
```

然后编辑文件，添加内容。

或者直接创建文件，使用以下模板：

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

保存后 push 到 GitHub，网站会自动更新！

## 功能说明

- **分类**：点击导航栏的"分类"查看所有分类
- **标签**：点击导航栏的"标签"查看所有标签
- **搜索**：在首页搜索框输入关键词实时搜索
- **响应式**：支持手机和电脑访问

