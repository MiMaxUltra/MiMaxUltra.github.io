# Curry Stark 的个人博客（Minimal Mistakes + GitHub Pages）

这是 Curry Stark（MiMaxUltra）的个人博客源码，基于 Minimal Mistakes 主题，部署在 GitHub Pages。

- 主题皮肤：air
- 语言：简体中文（zh-CN）
- 评论：Utterances（基于 GitHub Issues）
- 检索：站内全文搜索（Lunr）

## 在线地址
- 主页：`https://MiMaxUltra.github.io`

## 快速开始
1. 克隆本仓库
2. 修改站点配置：`_config.yml`
3. 本地预览（可选）
   - 安装 Ruby（含 Bundler、Jekyll），或直接依赖 GitHub Actions/Pages 构建
   - 本地预览命令（如已安装 Jekyll）：
     ```bash
     bundle install
     bundle exec jekyll serve
     ```
     打开 `http://127.0.0.1:4000` 预览

## 你可能想改的配置
- 站点信息：`_config.yml`
  - `title`、`name`、`description`、`locale`、`url`、`baseurl`
  - 评论：`comments.provider`（当前 `utterances`），`comments.utterances.repo`
  - 作者信息：`author.name`、`author.email`、`author.bio`、`author.location`、`author.avatar`
  - 社交链接：`social.links` 与 `author.links`
  - 页脚：`footer.links`、`footer.since`
- 导航：`_data/navigation.yml`
- 关于页：`_pages/about.md`
- 归档/分类/标签页：`_pages/year-archive.md`、`_pages/categories.md`、`_pages/tags.md`
- 首页布局：`index.html`（Front matter）

## 写一篇新文章
- 在 `_posts/` 目录下新建 Markdown 文件，文件名格式：`YYYY-MM-DD-title.md`
- 推荐 Front matter 模板：
  ```yaml
  ---
  layout: single
  title: 你的文章标题
  date: 2025-09-10 20:00:00 +0800
  categories: [分类A, 分类B]
  tags: [标签1, 标签2]
  author: Curry Stark
  excerpt: 一句简短摘要，便于社交分享与列表页展示。
  ---
  ```
- 图片资源放在 `assets/images/`，以相对路径引用：`/assets/images/xxx.png`

## 评论（Utterances）
- 需在 GitHub 安装并授权 Utterances 应用到本仓库：`https://github.com/apps/utterances`
- 确保仓库 Issues 已开启（Settings → General → Features → 勾选 Issues）
- 配置位置：`_config.yml` → `comments.utterances.repo`

## 站内检索（Lunr）
- 已开启全文检索：`search: true`、`search_full_content: true`
- 若使用 Algolia，可将 `search_provider` 改为 `algolia` 并填写 `algolia.*` 配置

## 目录结构（节选）
```
.
├─ _config.yml               # 站点与主题全局配置
├─ _data/
│  ├─ navigation.yml         # 顶部导航
│  └─ ui-text.yml            # 主题内置多语言文本（已含 zh-CN）
├─ _pages/
│  ├─ about.md               # 关于页面
│  ├─ year-archive.md        # 归档
│  ├─ categories.md          # 分类
│  └─ tags.md                # 标签
├─ _posts/                   # 文章目录（按日期命名）
├─ _layouts/ _includes/ _sass/  # 主题模板与样式
├─ assets/                   # 静态资源（图像/JS/CSS）
└─ index.html                # 首页（layout: home, author_profile: true）
```

## 部署
- push 到 `master` 分支，GitHub Pages 将自动构建并发布
- 仓库设置建议：Settings → Pages → Branch 选择 `master`（或默认设置）

## 常见问题
- 首页不显示文章？确认 `_posts/` 文件命名与 Front matter `date` 正确
- 评论不显示？确认已安装 Utterances 并开启 Issues，且 `_config.yml` 的 `comments.utterances.repo` 正确
- 中文界面未生效？确认 `_config.yml` 的 `locale: zh-CN`

## 授权与感谢
- 主题：Minimal Mistakes（MIT）
- 本仓库内容版权归作者所有，欢迎在标注来源的前提下合理引用

欢迎通过 Issues 提交建议或勘误。
