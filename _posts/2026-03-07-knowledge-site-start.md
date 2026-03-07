---
layout: post
title: 从 0 到 1 搭建个人知识网站
subtitle: 用 Jekyll 模板快速上线并长期维护
author: GengerLi
image: /img/home.jpg
intro: 这篇文章记录我的知识网站最小可行流程，先跑起来，再持续优化。
intro_image: /img/home.jpg
intro_image_ratio: is-16by9
tags:
  - Jekyll
  - GitHub Pages
  - 知识管理
---

## 目标

我希望这个网站至少满足三件事：

1. 文章可长期沉淀，支持全文阅读和分类检索。
2. 发布路径简单，写完后可以一键推送上线。
3. 页面结构稳定，后续只需要专注内容。

## 最小发布流程

1. 在 `_posts` 里新建 `YYYY-MM-DD-title.md`。
2. 写好 front matter（标题、作者、标签、封面）。
3. 本地执行 `bundle exec jekyll serve --livereload` 预览。
4. `git add -A && git commit -m "new post" && git push`。
5. 等待 GitHub Actions 自动部署。

## 内容组织建议

- 每篇文章只回答一个核心问题。
- 每篇都写「适用场景」「步骤」「常见错误」三段。
- 标签尽量控制在 3 到 5 个，保持统一命名。

## 下一步

后续我会补充：

- 标签索引页（按主题聚合文章）
- 常用模板（教程、踩坑、复盘）
- 固定周更节奏
