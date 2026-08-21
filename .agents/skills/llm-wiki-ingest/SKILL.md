---
name: llm-wiki-ingest
description: Ingest new, latest, or explicitly named source materials from this repository's `0.0 Inbox/` into the Markdown/Obsidian LLM Wiki. Use when the user asks to process, import, add, or update Inbox materials, continue growing the knowledge base, 处理最新材料, 导入新材料, 把材料加入知识库, or update the Wiki from new sources. Creates or updates Material, Topics, Maps, 目录, and the append-only import log.
---

# LLM Wiki Ingest

把 `0.0 Inbox/` 中的新材料编译进现有知识网络。直接完成文件写入与 QA，不只返回摘要或方案。

## 开始前

从本 `SKILL.md` 所在目录向上三级定位仓库根目录，不依赖用户提供绝对路径。完整读取：

1. `<repo>/AGENTS.md`
2. `<repo>/README.md`
3. `<repo>/使用说明.md`
4. `<repo>/目录.md`
5. `references/页面规范.md`
6. `references/导入日志.md`

随后读取与待处理材料最接近的现有 Material、Topic 和 Map。长访谈或播客可参考 `1.0 Material/Marty Cagan｜产品团队的本质.md` 的内容密度，但不得机械复制章节结构。

## 确定待处理材料

- 用户明确指定文件时，只处理指定文件。
- 用户说“最新”“新增”“未处理”或笼统要求处理 Inbox 时，扫描 `0.0 Inbox/` 的可读材料，忽略 `README.md`、隐藏文件和系统文件。
- 对每个候选文件计算 SHA-256，并用相对路径、文件名、标题、作者、URL、DOI/ISBN、`source_id` 与日志和现有页面查重。
- 日志中没有相同路径与指纹，或同一路径的指纹发生变化，才视为待处理。修改时间只用于决定处理顺序。
- 已导入同一版本时停止重复写入并报告证据。新版、译文、节选或不同载体必须保留版本关系，不能静默覆盖。
- 若没有待处理材料，报告扫描范围和查重结果，不写空日志。

`references/导入日志.md` 是唯一状态来源。不得另建 manifest、ledger 或状态文件。

## 执行流程

### 1. 阅读与审计

完整阅读材料，不只依赖 frontmatter、摘要、目录或搜索片段。识别材料类型、标题、作者或说话人、日期、版本、语言、外部链接和可用 locator；记录 metadata 冲突、缺页、OCR 错误、说话人不明与弱定位。

`0.0 Inbox/` 只读：不得改写、移动、重命名或删除。

### 2. 创建或更新来源页

- 所有单一来源页放进 `1.0 Material/`，用 frontmatter 区分材料类型。
- 正文结构由材料本身决定，不套固定模板。遵守 `references/页面规范.md` 的证据、归因、密度和定位底线。
- 保留独立判断、reasoning、例子或数据、反例、适用边界和 locator；质量优先于 Token 节省。
- `source_file` 必须链接到真实 Inbox 原文的文件名，例如 `source_file: "[[example]]"`；未知字段不猜测。
- 短引文必须可核验、归属正确并直接支持判断。跨段综合标注“综合判断，无单句原话”。

### 3. 连接知识网络

- 搜索标题、aliases、`concept_id` 和近义词，优先更新已有 canonical Topic。
- 把新来源带来的推理、例子、反例、边界、分歧和 locator 写进相关 Topic。
- 只有概念边界稳定、有独立解释价值且无法自然并入现有 Topic 时才新建 Topic。
- 不创建 Playbooks。只有 Topic 关系或阅读路径实质变化时才更新 Map；Map 不复制正文。

### 4. 同步目录与日志

- 更新 `<repo>/目录.md`：收录所有新页面，并更新受影响页面的一句话说明与 `updated` 日期。
- 在 `references/导入日志.md` 末尾追加一个批次记录，逐一列出本次材料的相对路径、SHA-256、`source_id`、动作、输出页面与异常。
- 不修改历史日志；发现旧记录错误时追加更正记录。
- 每次有实际导入写入时，目录和日志都必须更新，即使没有新建 Topic 或 Map。

### 5. QA

检查：

- 关键判断能否回到 locator；作者、说话人、短引文与 locator 是否匹配；
- 是否过度压缩 reasoning、例子或边界；是否把单一来源误写成共识；
- 是否重复创建 Topic，或抹平来源冲突；
- frontmatter、`source_id`、`source_file`、`source_fingerprint`、`insight_count` 与正文是否一致；
- 新增 wikilink 是否可解析，新页面是否至少连接一个现有页面；
- `目录.md` 和导入日志是否同步，Inbox 原文是否保持未修改。

完成后报告：扫描范围、处理与跳过的材料、创建或修改文件、洞见数量、Topic/Map 变化、查重证据、来源异常、QA 结果和人工复核项。
