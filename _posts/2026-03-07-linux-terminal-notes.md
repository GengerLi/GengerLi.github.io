---
layout: post
title: Linux 命令行高频排错清单
subtitle: 先定位问题，再动手修复
author: GengerLi
image: /img/home.jpg
intro: 这是一份我日常用的命令行排错速查，重点是少走弯路。
intro_image: /img/home.jpg
intro_image_ratio: is-16by9
tags:
  - Linux
  - Terminal
  - Debug
---

## 1. 先看当前状态

```bash
pwd
ls -la
git status --short
```

先确认你在正确目录，避免“修了半天修错地方”。

## 2. 查文件和文本

```bash
rg --files
rg "关键词" -n
```

优先用 `rg`，速度快且输出清晰。

## 3. 服务起不来时

```bash
lsof -i :4000
pgrep -af jekyll
```

如果端口被占用，先停掉旧进程再重启。

## 4. 权限问题

遇到 `Permission denied` 时，优先检查：

1. 目录归属是否为当前用户。
2. 是否误用了系统路径安装依赖。
3. 是否可以改为用户目录安装。

## 5. 我常用的处理原则

- 先复现，再修复。
- 一次只改一处，便于回滚。
- 每次修复后立即验证。
