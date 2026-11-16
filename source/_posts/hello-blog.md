---
title: 👋 博客开张
date: 2026-11-16 20:00:00
tags:
  - 随笔
categories:
  - 折腾
---

这里是我的新博客，用的是 **Hexo + Cactus 主题**，整体排版参考了一个我很喜欢的个人站点。

写下这篇，主要是给自己留一份「开工备忘」：站点是怎么组织的、以后写文章要动哪几个文件。

## 这套站点由什么组成

| 部分 | 位置 | 作用 |
| --- | --- | --- |
| 站点配置 | `_config.yml` | 站点名、作者、域名、文章链接格式 |
| 主题配置 | `themes/cactus/_config.yml` | 导航菜单、配色、页脚、评论 |
| 自定义样式 | `source/css/custom.css` | 字体、颜色、间距等细节 |
| 文章 | `source/_posts/` | 每篇文章一个 `.md` 文件 |
| 独立页面 | `source/about/`、`source/diary/`、`source/projects/` | 关于、生活、项目 |
| 图片等静态资源 | `source/images/` | Logo、导航小图标、文章配图 |

## 一句话流程

写完 Markdown，跑一条命令，`public/` 目录里就是完整的静态站点，丢到任何静态托管上都能访问。

```bash
hexo new "文章标题"   # 新建文章
hexo server           # 本地预览 http://localhost:4000
hexo generate         # 生成静态文件到 public/
```

> 后面两篇分别是 Hexo 命令速查和 Markdown 语法速查，忘了随时翻。
