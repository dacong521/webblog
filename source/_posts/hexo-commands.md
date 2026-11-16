---
title: 🧰 Hexo 常用命令与写作流程
date: 2026-11-15 21:30:00
tags:
  - Hexo
  - 工具
categories:
  - 折腾
---

## 日常三条命令

```bash
hexo new "文章标题"     # 新建文章，生成 source/_posts/文章标题.md
hexo server            # 本地起服务，浏览器打开 http://localhost:4000
hexo generate          # 生成静态站点到 public/
```

改完文章刷新浏览器即可，本地服务会自动重新生成（默认开启了实时预览）。

## 新建独立页面

```bash
hexo new page about    # 生成 source/about/index.md
hexo new page diary    # 生成 source/diary/index.md
```

页面和文章的区别：页面不会出现在文章列表里，适合「关于」「生活」「项目」这类常驻内容。建完还要在主题配置的 `nav` 里加一项，导航栏才会显示。

## 清理与重新生成

```bash
hexo clean && hexo generate
```

样式改了但页面没变化时，先 `hexo clean` 再生成，多半就好了。

## 文章的头部信息（Front-matter）

每篇文章开头的两行 `---` 之间是元信息：

```yaml
---
title: 文章标题
date: 2026-11-16 20:00:00
tags:
  - 标签一
  - 标签二
categories:
  - 分类
---
```

- `date` 决定文章在首页和归档里的排序（新的在前）
- `tags` 和 `categories` 可以只写一个，也可以都不写
- 想固定某篇文章的链接，可以在 `_config.yml` 里调整 `permalink`

## 图片怎么放

在文章同目录放一个同名文件夹，把图片丢进去，正文里这样引用：

```markdown
![说明文字](图片文件名.png)
```

这样导出、迁移时图片跟着文章走，不会丢。
