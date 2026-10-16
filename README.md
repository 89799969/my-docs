# my-docs

使用 MkDocs 编写技术文档，通过 GitHub Actions 自动构建并部署到 GitHub Pages。

## 项目结构

```
my-docs/
├── docs/                  # 存放 Markdown 文档
│   ├── index.md           # 主页
│   ├── about.md           # 关于页面
│   ├── guide.md           # 使用指南
│   └── api.md             # API 参考
├── .github/workflows/
│   └── deploy.yml         # 自动化部署工作流
└── mkdocs.yml             # MkDocs 配置文件
```

## 部署流程

1. 推送 `docs/**` 或 `mkdocs.yml` 的变更到 `main` 分支
2. GitHub Actions 自动安装 MkDocs Material 并构建
3. 构建产物（`site/` 目录）自动推送到 `gh-pages` 分支
4. GitHub Pages 托管，访问 `https://<用户名>.github.io/my-docs/`

## 本地预览

```bash
pip install mkdocs-material
mkdocs serve
```
