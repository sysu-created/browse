# browse

一个基于 [legacy.json](https://github.com/sysu/legacy.json/) 规范的历史项目浏览网站。

## 项目简介

本项目提供了一个中大人相关的[历史遗产项目](https://github.com/sysu/legacy.json/)的收集地。

## 如何添加项目

1. 在你的项目仓库中创建 `legacy.json` 文件（遵循 [legacy.json 规范](https://github.com/sysu/legacy.json/blob/main/spec.md)）
2. Fork 本仓库
3. 在 `input.txt` 文件中添加你的项目 GitHub 仓库地址（每行一个）
4. 提交 Pull Request

## 工作原理

项目使用 GitHub Actions 自动构建和部署：

1. 从 `input.txt` 读取项目列表
2. 使用 [legacy.json 工具](https://github.com/sysu/legacy.json/tree/main/tools/genpages) 下载项目的 `legacy.json` 文件
3. 使用自定义模板生成静态网页
4. 部署到 GitHub Pages

## 浏览网站

<https://sysu-created.github.io/browse/>

## 项目结构

```
.
├── .github/
│   └── workflows/
│       └── main.yml          # GitHub Actions 工作流配置
├── templates/
│   ├── common.css            # 通用样式
│   ├── index.tmpl            # 首页模板
│   └── detail.tmpl           # 详情页模板
└── input.txt                 # 项目列表
```

## 本地开发

如需本地预览，可以参考 [legacy.json 工具](https://github.com/sysu/legacy.json/tree/main/tools/genpages) 的使用说明。
