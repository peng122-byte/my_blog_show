# 博客项目说明

## 项目信息

- **博客地址**: https://kun123.xyz/
- **博客名称**: 鲲的琴盒
- **框架**: Hugo + hugo-theme-stack 主题
- **语言**: 简体中文 (默认) + English

## 仓库结构

| 仓库 | 用途 |
|------|------|
| `peng122-byte/my_blog_source` | 源码仓库（本地开发） |
| `peng122-byte/my_blog_show` | 静态文件仓库（GitHub Pages） |

## 部署流程

```
git push → GitHub Actions 自动构建 → 部署到 GitHub Pages → 自动 SSH 更新阿里云服务器
```

**完全自动化，只需 `git push` 即可完成部署。**

## 常用命令

```bash
# 创建新文章
hugo new post/文章名称/index.md

# 本地预览
hugo server

# 发布文章
git add .
git commit -m "新文章：xxx"
git push origin main
```

## 目录结构

- `content/post/` - 博客文章目录
- `content/page/` - 独立页面（关于、归档等）
- `assets/img/avatar.png` - 头像图片
- `hugo.yaml` - 网站配置文件
- `.github/workflows/deploy.yml` - 自动部署配置

## 服务器信息

- **阿里云博客目录**: `/var/www/blog`
- **部署方式**: GitHub Actions SSH 自动 pull
