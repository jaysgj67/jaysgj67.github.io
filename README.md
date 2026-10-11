# 纸上美术馆 · The Paper Museum

一个人的私人档案馆：写作（Blog）、项目（Projects）、著述（Publications）、投资笔记（Investing）与联系方式（Contact）。

纯 HTML / CSS / JS 单文件站点，无构建工具、无框架、无追踪。衬线字体 + 陶土橙唯一强调色 + 纸张噪点纹理，展签与印章是签名元素。

## 目录结构

```
paper-museum/
├── index.html   # 站点本体（全部样式与逻辑内联，hash 路由切换六个视图）
├── 404.html     # 艺术化 404 页（GitHub Pages 自动生效）
├── rss.xml      # RSS 订阅源（示例条目，请替换为你的文章）
└── README.md
```

## 本地预览

任意静态服务器打开即可：

```bash
cd paper-museum
python3 -m http.server 8000   # 然后访问 http://localhost:8000
```

## 部署到 GitHub Pages

1. 在 GitHub 新建仓库（如 `yourname.github.io`，公开仓库）。
2. 推送本目录内容到 `main` 分支。
3. 仓库 Settings → Pages → Source 选择 `Deploy from a branch` / `main` / `/ (root)`。
4. 等待 1–2 分钟，访问 `https://yourname.github.io/`。

> 注意：GitHub Pages 免费版要求仓库为公开仓库（Pro 可私有）。

## 自定义指南

所有占位内容都在 `index.html` 中，搜索以下标记即可找到并替换：

| 位置 | 说明 |
|---|---|
| 名字「简」与英文名 | 顶部品牌印章、Hero、footer 版权行；`.brand .seal` 与相关文本 |
| `ARCHIVE · EST. 2008` | 档案馆起始年份 |
| Hero 副标题与定位句 | 一句话描述你自己 |
| Blog 示例条目（日记/周报/年报） | `view-blog` 区块，按 `tl-group` 增删 |
| Projects 示例项目 | `view-projects` 区块的 `project-card`，复制卡片即可新增 |
| Publications 示例书目 | `view-publications` 区块的 `pub-card` |
| Investing 原则与笔记 | `view-investing` 区块的 `ledger-row`；页内已附"非投资建议"声明 |
| 社交链接 | `view-contact` 的 `contact-card`，把 `github.com/yourname` 等换成你的真实地址 |
| 邮箱 | `mailto:hello@example.com` |
| CV 下载按钮 | 当前为占位 `href`，请换成你的简历文件（如 `cv.pdf` 放进同目录） |
| RSS 地址 | `rss.xml` 中的 `yourname.github.io` 与示例条目 |
| 页脚年份与修订日期 | `f-bottom` 段落 |

**配色令牌**（`:root` CSS 变量）：

| 变量 | 值 | 用途 |
|---|---|---|
| `--paper` | `#f4f1e8` | 页面纸白 |
| `--paper-deep` | `#eae4d4` | 次级面/页脚 |
| `--paper-lift` | `#faf8f1` | 卡片 |
| `--ink` | `#1c1917` | 主文字 |
| `--ink-soft` | `#57504a` | 次文字 |
| `--terracotta` | `#c96442` | 唯一强调色（印章/CTA/hover） |
| `--teal` | `#5b7f86` | 次强调（编号/眉标） |
| `--ochre` | `#8a5a2e` | 标签 |

## 说明

- 页面内所有 Blog / Projects / Publications / Investing 条目均为**示例占位内容**，仅为展示设计效果，请替换为你的真实记录。
- 站内链接（导航、卡片、`#/xxx`）走 hash 路由，部署后无需任何服务器配置。
- 字体经自托管镜像加载（Spectral / Noto Serif SC / JetBrains Mono / Caveat），离线或镜像不可达时回退系统衬线字体栈。
- 插图为本馆定制的木刻版画风格素材，暖米纸色系，与站点视觉统一。
