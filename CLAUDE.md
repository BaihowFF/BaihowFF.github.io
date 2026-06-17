# BaihowFF 的博客 — 小G 工作手册

## 项目概述

MkDocs + Material 主题的个人博客，部署在 GitHub Pages，自定义域名 `baihowff.com`。

## 技术栈

- Python 3.11.9
- MkDocs 1.6.1 + mkdocs-material 9.7.6
- 托管: GitHub Pages (GitHub Actions 自动部署)
- 仓库: `BaihowFF/BaihowFF.github.io`

## 目录结构

```
E:\ZhangSanLaw\Process\Agent\GithubBlogAgent/
├── 待发布/                  ← 用户放草稿的地方（受 .gitignore 保护）
├── docs/
│   ├── about.md             ← 关于页面
│   ├── .authors.yml         ← 作者信息（baihowff）
│   ├── posts/               ← 博客文章目录
│   │   ├── 文章1.md
│   │   └── 文章2.md
│   └── stylesheets/
│       └── extra.css        ← 烟雨主题配色
├── mkdocs.yml               ← 博客配置文件
├── .github/workflows/
│   └── deploy.yml           ← GitHub Actions 自动部署
└── CLAUDE.md                ← 本文件
```

## 配色方案：烟雨 (Yan-yu)

| 用途 | 日间模式 | 夜间模式 |
|------|---------|---------|
| 背景 | `#E8F0F2` (晨雾蓝白) | `#283339` (远山深蓝) |
| 主色调 | `#6E99A4` (雾中水色) | `#6E99A4` (雾中水色) |
| 正文 | `#1A1A1A` (深色) | `#F5F5F5` (亮色) |

## 发布流程

### 当用户说"发布这篇文章"时

1. 检查 `待发布/` 目录下的 `.md` 文件
2. **检查并修正文章格式**（必须包含以下 YAML 头部）：

```yaml
---
title: 文章标题
date: YYYY-MM-DD
authors:
  - baihowff
tags:
  - 标签1
  - 标签2
---
```

3. 将文件移动到 `docs/posts/` 目录
4. 执行 git 操作：

```bash
git add docs/posts/文件名.md
git commit -m "feat: 发布新文章 - 文章标题"
git push
```

5. 通知用户 GitHub Actions 自动部署中，一两分钟后上线

### 当用户要求推送本地修改时

```bash
git add -A
git commit -m "feat: 描述修改内容"
git push
```

## 注意事项

- 不要修改用户文章的内容和风格（仅修正格式问题）
- 所有 git push 前必须经用户确认同意
- 不要在未确认的情况下执行破坏性 git 操作
- 用户时区：Asia/Shanghai (UTC+8)
