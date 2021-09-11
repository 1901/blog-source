---
title: "使用 Hugo 搭建博客"
date: 2021-09-10T20:07:01+08:00
---

尝试使用 `Hugo` 来搭建静态博客。

## 安装
我是用的 `macOS`，如果是其他系统请直接参考 [官方文档](https://gohugo.io/getting-started/installing/)。
```bash
brew install hugo
```

## 创建博客
```bash
hugo new site myblog
```

## 安装主题
可以在这里找到你喜欢的主题。(本站采用的就是 hugo-book 主题) 
- [https://themes.gohugo.io](https://themes.gohugo.io)
```bash
cd themes
git clone --depth 1 https://github.com/alex-shpak/hugo-book book
```
