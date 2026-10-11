# 靛蓝档案 · Indigo Archive

一个人的私人档案馆：写作（Blog）、项目（Projects）、著述（Publications）、投资笔记（Investing）与联系方式（Contact）。

纯 HTML / CSS / JS 单文件站点，无构建工具、无框架、无追踪。靛蓝夜空 + 星点网格为底，荧光青为唯一强调色；**月相**与**终端命令**是签名元素——主页展出亮面，日记藏在暗面。

## 目录结构

```
paper-museum/
├── index.html   # 站点本体（全部样式与逻辑内联，hash 路由切换六个视图）
├── 404.html     # 深色风格 404 页（GitHub Pages 自动生效）
├── rss.xml      # RSS 订阅源（示例条目，请替换为你的文章）
├── README.md
└── _backup/
    └── index-v1-paper-museum.html   # 上一版「纸上美术馆」完整备份
```

## 本地预览

```bash
cd paper-museum
python3 -m http.server 8000   # 访问 http://localhost:8000
```

## 部署与更新（GitHub Pages）

仓库：`jaysgj67-netizen/jaysgj67-netizen.github.io`，改完内容后：

```bash
git add -A && git commit -m "更新内容" && git push
```

约 1 分钟后 Pages 自动构建生效，访问 https://jaysgj67-netizen.github.io/

## 自定义指南

所有占位内容都在 `index.html` 中，搜索以下标记即可找到并替换：

| 位置 | 说明 |
|---|---|
| 名字「简」 | 顶部品牌、Hero 定位句、终端 `whoami` 输出、footer 版权行 |
| Hero 副标题与定位句 | 「主页展出亮面……」一段，改成你自己的话 |
| 终端脚本 | `<script>` 中 `termScript` 数组，三行命令可随意改写（`whoami` / `ls archive/` / `cat diary/latest`） |
| Blog 示例条目 | `view-blog` 区块，按 `tl-group`（diary/weekly/yearly）增删 |
| Projects 示例项目 | `view-projects` 区块的 `repo-card`，复制卡片即可新增 |
| Publications 示例书目 | `view-publications` 区块的 `pub-card` |
| Investing 原则与笔记 | `view-investing` 区块的 `ledger-row`；页内已附"非投资建议"声明 |
| 社交链接 | `view-contact` 的 `contact-card`，把 `github.com/yourname` 等换成你的真实地址 |
| 邮箱 | `mailto:hello@example.com` |
| CV 下载按钮 | 当前为占位 `href`，请换成你的简历文件（如 `cv.pdf` 放进同目录） |
| RSS 地址 | `rss.xml` 中的站点链接与示例条目 |
| 页脚年份与修订日期 | `f-bottom` 段落 |

**配色令牌**（`:root` CSS 变量）：

| 变量 | 值 | 用途 |
|---|---|---|
| `--night` | `#0d1226` | 夜空主底 |
| `--night-2` | `#141a36` | 卡片底 |
| `--moon` | `#eef1f9` | 月光白主文字 |
| `--moon-dim` | `#9aa3c7` | 次文字 |
| `--cyan` | `#4dd8d0` | 唯一强调色（荧光青） |
| `--amber` | `#ffb454` | 次强调（标签/警示） |
| `--indigo-bright` | `#4658d9` | 论文徽标等辅助 |

## 说明

- 页面内所有 Blog / Projects / Publications / Investing 条目均为**示例占位内容**，仅为展示设计效果，请替换为你的真实记录。
- 站内链接（导航、卡片、`#/xxx`）走 hash 路由，部署后无需任何服务器配置。
- 字体经自托管镜像加载（Space Grotesk / Noto Sans SC / JetBrains Mono），离线或镜像不可达时回退系统无衬线字体栈。
- 插图为本馆定制的深空科技风素材，靛蓝夜色系，与站点视觉统一。
- 上一版「纸上美术馆」完整保留在 `_backup/index-v1-paper-museum.html`，想换回旧皮肤可直接覆盖 `index.html`。
