# Pocket Wiki｜可继续生长的 LLM Wiki

这是一个可以直接下载、阅读并继续扩展的 Markdown / Obsidian 知识库。当前 Sample 以 12 期 Lenny's Podcast 为起点，但同一套结构也能吸收文章、论文、报告、书摘、网页正文、访谈和会议记录。

它不把材料堆成一批孤立摘要，而是分成三层：

- `1.0 Material/`：保留每一份来源的判断、推理、例子、边界和定位；
- `2.0 Topics/`：把多个来源围绕同一问题连接起来；
- `3.0 Maps/`：提供领域导航和阅读路径。

## 快速开始

1. 下载或 clone 整个仓库。
2. 用 Obsidian 将仓库根目录作为 Vault 打开，从 [首页](首页.md) 开始阅读。
3. 把你的新材料放进 `0.0 Inbox/`。
4. 用 Codex 打开仓库根目录，然后说：`帮我处理 Inbox 里最新加入的材料。`

仓库自带 `llm-wiki-ingest` Skill。Codex 会根据请求自动调用；需要显式指定时，可以说：`使用 $llm-wiki-ingest 处理 Inbox 里的新增材料。`

完整用法见 [使用说明](使用说明.md)。

## 仓库结构

```text
0.0 Inbox/       原始材料投递区；Agent 只读
1.0 Material/    单一来源的编译页
2.0 Topics/      跨来源的 canonical 知识页
3.0 Maps/        领域地图与阅读路径
目录.md          面向读者和 Agent 的全库索引
.agents/skills/  仓库级 Agent Skill、质量规范与导入日志
AGENTS.md        所有 Agent 必须遵守的仓库规则
```

## 公开边界

`.gitignore` 默认不追踪 `0.0 Inbox/` 中的个人材料，只保留该目录的说明文件。不要把私人、内部或受版权保护的完整原文提交到公开仓库。

这个仓库提供 12 期 Lenny's Podcast 的派生知识页，不提供完整付费文字稿。后续 300 多期全量索引会作为独立项目发布，不直接堆回这个 Sample。
