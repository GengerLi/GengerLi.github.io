---
layout: post
title: "个人知识网站搭建记录"
subtitle: "从模板初始化到上线的最小流程"
author: GengerLi
categories: [站点建设]
tags: [Jekyll, GitHub Pages, 知识库]
banner: "/assets/images/banners/home.jpeg"
---

这篇文章记录我的知识网站第一版搭建过程，目标是先稳定上线，再持续优化内容。

## 环境与流程

1. 安装 Ruby 与 Bundler。
2. 在项目目录执行 `bundle install` 安装依赖。
3. 使用 `bundle exec jekyll serve --livereload` 本地预览。
4. 通过 `git push origin master` 触发 GitHub Actions 自动部署。

## 站点内容结构

- 首页：展示最新文章与站点定位。
- 归档页：按时间浏览历史文章。
- 分类与标签页：做主题聚合和快速检索。
- 关于页：说明站点目标与更新方向。

## 下一步计划

- 新增固定写作模板，减少每篇文章的准备时间。
- 补充工具类与排错类文章，优先写可复用内容。
