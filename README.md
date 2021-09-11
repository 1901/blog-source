# README
---

## 新文章
```bash
hugo new post/new-page.md
```

## 测试
```bash
hugo server -D
```
运行上面的命令后，用浏览器访问 [http://localhost:1313/](http://localhost:1313/) 就可以即时看到效果，页面还能跟随文档的修改自动刷新。

## 部署
```bash
hugo --baseUrl="https://1901.github.io" 
```
运行上面的命令后，会在 `public` 目录生成所有的静态页面。将这个目录的所有文件 `push` 到 `github` 上的 `master` 分支就完成了。