---
layout: post
title: "Linux 常用排错清单"
subtitle: "问题定位优先，修复动作最小化"
author: GengerLi
categories: [开发实践]
tags: [Linux, Terminal, Debug]
banner: "/assets/images/banners/home.jpeg"
---

当服务起不来、命令报错或者部署失败时，我会先按固定顺序检查，避免无效操作。

## 第一步：确认上下文

```bash
pwd
ls -la
git status --short
```

先确认目录、文件和分支是否正确。

## 第二步：定位进程和端口

```bash
pgrep -af jekyll
lsof -i :4000
```

如果端口占用，先结束旧进程再重启服务。

## 第三步：看日志关键词

重点关注这三类报错：

- 权限问题（Permission / safe.directory）
- 依赖问题（could not find gem / version conflict）
- 构建问题（scss syntax / plugin missing）

## 第四步：小步验证

每次只改一个变量，执行一次验证命令，避免多处修改导致问题叠加。
