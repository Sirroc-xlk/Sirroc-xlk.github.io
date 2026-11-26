# 我的小站

网址：https://sirroc-xlk.github.io

用 [Astro](https://astro.build) 搭建，文章用 Markdown 写，推送到 GitHub 后会自动发布（一般 1～2 分钟生效）。

## 怎么发一篇新文章（直接在 GitHub 网页上操作，不用装任何软件）

1. 打开仓库里的 `src/content/posts` 文件夹
2. 点右上角 **Add file → Create new file**
3. 文件名写成英文或拼音加 `.md`，比如 `2026-12-01-first-snow.md`（文件名就是文章网址的一部分）
4. 内容最上面先写这一段"文章信息"，然后空一行开始写正文：

```markdown
---
title: 文章标题
date: 2026-12-01
description: 一句话简介（可以不写）
tags: [随笔, 生活]
---

正文从这里开始写……
```

5. 点右上角 **Commit changes**，再点一次 **Commit changes** 确认
6. 等 1～2 分钟，刷新网站就能看到新文章了

## 常见操作

| 想做的事 | 怎么做 |
| --- | --- |
| 修改文章 | 打开那篇 `.md` 文件，点铅笔图标 ✏️ 编辑，然后 Commit |
| 删除文章 | 打开文件，点右上角 `…` → **Delete file** |
| 先存草稿不发布 | 在文章信息里加一行 `draft: true`，想发布时删掉这行 |
| 放图片 | 把图片上传到 `public/images/` 文件夹，文章里写 `![说明](/images/图片名.jpg)` |
| 改网站名字和简介 | 编辑 `src/site.config.ts` |
| 改"关于"页 | 编辑 `src/pages/about.md` |

Markdown 写法忘了，可以看网站上的《写文章的格式小抄》。

## 发布失败怎么办

打开仓库的 **Actions** 页面，红叉就是失败了，点进去能看到原因。最常见的是文章开头的"文章信息"格式写错了（比如少了 `---`、日期格式不对、冒号用了中文冒号 `：`）。

## 在自己电脑上预览（可选，进阶）

```bash
npm install
npm run dev
```

然后浏览器打开 http://localhost:4321
