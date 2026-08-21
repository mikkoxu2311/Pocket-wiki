# Repository instructions

本仓库是由 Agent 维护的 Markdown / Obsidian Wiki。任何 Agent 在仓库内工作，都必须遵守以下规则。

## 开始任何写入前

1. 完整读取 `README.md`、`使用说明.md` 和 `目录.md`。
2. 如果任务涉及导入、处理或更新 `0.0 Inbox/` 中的材料，必须使用 `.agents/skills/llm-wiki-ingest/SKILL.md`，并按其要求读取引用文件。
3. 先搜索相关的 `1.0 Material/`、`2.0 Topics/` 和 `3.0 Maps/` 页面，再决定更新还是新建。
4. 只改动完成当前任务所必需的文件；不得顺手重构整个 Wiki。

## 硬边界

- `0.0 Inbox/` 是原始证据区，只能读取；不得改写、移动、重命名或删除其中任何材料。
- 不猜作者、日期、说话人、页码、URL、DOI、ISBN 或原文。缺失就明确标注。
- 不把单一来源观点写成共识；来源冲突时并列保留观点、证据和成立条件。
- 优先更新已有 canonical Topic；不得为同义词重复建页。
- 不新建 Playbooks 层或其他顶层目录，除非用户明确要求改变架构。
- 不把私人、内部或受版权保护的完整原文复制到公开知识页。
- 根目录和编号文件夹中的 Markdown 面向人类读者；Agent 专用执行细节放在 `.agents/skills/`。

## 每次 ingest 必须完成

- 创建或更新 `1.0 Material/` 来源页；
- 只在证据支持且关系确实变化时更新 `2.0 Topics/` 与 `3.0 Maps/`；
- 更新 `目录.md` 中所有受影响页面的一句话说明；
- 在 `.agents/skills/llm-wiki-ingest/references/导入日志.md` 末尾追加记录，不覆盖历史；
- 检查来源定位、frontmatter、`source_file`、`source_id`、指纹、wikilink 和孤立页；
- 最后向用户报告读取材料、文件变更、查重结果、异常和仍需人工复核项。

导入日志是唯一的处理状态记录，不另建 manifest、ledger 或状态文件。文件修改时间只能用于扫描排序，不能单独证明材料已经处理或尚未处理。

## 非导入任务

- 回答问题时先读 `目录.md`，再读相关 Topic 与来源页，并列出实际使用的 Wiki 页面。
- 修复链接、格式或索引等机械问题可以直接完成。
- 删除、合并、大范围改写或改变作者原意前，必须先征求用户同意。
