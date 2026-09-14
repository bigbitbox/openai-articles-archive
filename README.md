# OpenAI Articles Archive

个人维护的 OpenAI 技术文章快照库，收藏 GPT、Codex、提示工程及 Agent 相关内容。

在线文章可能被更新、迁移或删除。本项目保存文章在特定时间点的正文与网页快照，供离线阅读、历史追溯和版本对比。快照代表保存时的内容，不保证与当前官网一致。

## 文章索引

| 文章 | 快照日期 | 阅读版本 | 来源 |
| --- | --- | --- | --- |
| Rethinking skills and prompts for GPT-6 Astra | 2026-09-14 | [Markdown](articles/rethinking-skills-and-prompts-for-gpt-6-astra/2026-09-14/article.md) · [离线 HTML](articles/rethinking-skills-and-prompts-for-gpt-6-astra/2026-09-14/index.html) · [元数据](articles/rethinking-skills-and-prompts-for-gpt-6-astra/2026-09-14/metadata.json) | [OpenAI 原文](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra) |
| Prompting guidance for GPT-5.6 Sol | 2026-07-17（首次入库日期） | [Markdown](articles/prompting-guidance-for-gpt-5p6-sol/2026-07-17/article.md) · [元数据](articles/prompting-guidance-for-gpt-5p6-sol/2026-07-17/metadata.json) | 历史导入，原始页面 URL 未记录 |

GPT-5.6 文章从本仓库已有文件原样迁入，包括原有的重复标题。其目录日期来自首次 Git 提交，实际网页抓取时间未知，也没有当时的 HTML；不以新抓取的网页冒充历史快照。

## 离线阅读

下载或克隆仓库后，用浏览器打开对应快照目录中的 `index.html`，并保留同目录下的 `assets/`。GitHub 文件页面主要用于查看源码，阅读排版后的 HTML 请在本地打开。

```sh
git clone https://github.com/bigbitbox/openai-articles-archive.git
cd openai-articles-archive
```

如果浏览器限制本地文件资源，可在仓库根目录运行：

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

然后访问 <http://127.0.0.1:8000/>，进入文章目录并打开 `index.html`。

离线 HTML 保留原页面的静态排版、正文、图片和字体。站点脚本与动态加载已移除，搜索、主题切换和 Ask AI 等在线交互不在快照范围内；普通外部链接仍指向原网站。

## 目录与文件

```text
articles/
  <article-slug>/
    YYYY-MM-DD/
      article.md
      original.html
      index.html
      assets/
      metadata.json
```

| 文件 | 用途 |
| --- | --- |
| `article.md` | 便于阅读、检索和 Git 差异对比的正文；优先保存官方 Markdown 原件 |
| `original.html` | 抓取时返回的 HTML 原件，保留原始资源引用 |
| `index.html` | 将资源引用本地化后的静态离线阅读版 |
| `assets/` | 页面样式、图片、字体及 CSS 引用的资源 |
| `metadata.json` | 来源、作者、发布日期、抓取时间、处理说明和文件 SHA-256 校验值 |

历史导入记录可以只有 Markdown 和元数据。`metadata.json` 中的 `source_sha256` 对应下载原件，`sha256` 对应仓库内文件；CSS 经资源路径改写后，两者可能不同。

## 快照规则

- 日期目录按 `Asia/Shanghai` 时区的抓取日期命名；元数据保存带时区的实际抓取时间。文章发布日期单独记录。
- 再次抓取时新增目录，保留旧快照；同一天需要保存多个版本时，使用 `YYYY-MM-DDTHH-mm-ss+0800` 区分。
- 原始 HTML 与官方 Markdown 按下载内容保存。离线适配只修改阅读版及其资源，并在元数据中说明。
- 不补写无法确认的来源或日期；历史导入记录明确说明日期依据与缺失信息。
- 个人笔记、翻译和评论与原文分开存放，避免混入文章快照。

## 原文归属

文章及相关图片、字体等资源的权利归原作者及相应权利人所有。收录不改变原内容的许可条件。本项目为个人收藏与研究用途，与 OpenAI 无隶属关系。
