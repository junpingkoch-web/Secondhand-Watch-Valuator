# Project: watch-valuator（二手表估值器 / Secondhand Watch Valuator）

零构建静态站，**故意保持单文件结构**：全部 HTML/CSS/JS 都内联在一个 44KB 的 `index.html` 里，
没有拆成 `index.html`/`style.css`/`script.js`。这是用户明确做过的选择（2026-07-24），
**不要主动拆分成多文件，除非再次被明确要求**。

## 文件结构
- `index.html` — 唯一的核心文件，全部逻辑内联
- `ads.txt` / `robots.txt` / `sitemap.xml` / `README.md` — 已补齐，跟其他仓库对齐

## 双份同步（改动前必读）
这个工具**同时存在两份内容完全一致的副本**：
1. 独立仓库：`watch-valuator/index.html`（本仓库，`junpingkoch-web/Secondhand-Watch-Valuator`）
2. 博客内嵌副本：`watch-guide-blog/static/tools/watch-valuator/index.html`

这是刻意保留的"两份都要"场景（不像 duty-free-calculator 那样已经去重合并成一份）。
**改这个工具的任何内容，必须同时改两个仓库里的这两个文件，保持字节级一致**——
只改一边会导致独立站和博客内嵌版本显示不一致。

## Commands
- 无构建/测试命令
- 本地预览：共享配置在 `C:\Users\junpi\.claude\.claude\launch.json`

## 部署流程
- 改完直接 commit + push 到 `main`（两个仓库都要推）
- Commit 作者身份：`Junping Koch <junping.koch@gmail.com>`，每个仓库单独设置

## 明确禁止的事
- 不要把这个文件拆成 `index.html`/`style.css`/`script.js` 三件套——用户明确选择保持单文件
- 不要只改这一份就完事——记得去 `watch-guide-blog/static/tools/watch-valuator/index.html` 同步改动

## 持续维护
每次你需要重复纠正 Claude 同一件事三次以上，就把结论补进这个文件对应章节。
