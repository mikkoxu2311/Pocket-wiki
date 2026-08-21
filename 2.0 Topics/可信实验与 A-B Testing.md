---
type: topic
title: 可信实验与 A-B Testing
aliases: [可信在线实验, A/B Testing]
domains: [data-experimentation]
status: pilot
source_count: 2
---

# 可信实验与 A-B Testing

可信实验不只是把用户随机分成两组，而是确保分配、埋点、指标、统计判断与业务解释都没有破坏因果结论。

## 基本检查

- 实验前定义 primary metric 与 guardrail metrics。
- 检查 Sample Ratio Mismatch，确认实际分流符合设计比例。
- 监控重复记账、数据延迟与指标口径变化。
- 不因 revenue 上升就忽略用户体验受损。
- 给高风险高回报想法空间，但不要降低可信度标准。

## 与 discovery 的边界

实验适合回答“这个变化造成了什么”；[[客户访谈]] 和 [[Jobs to Be Done（JTBD）]] 更适合回答“为什么用户这样行动”。

## Sources

- [[Ronny Kohavi｜可信 A-B Testing]] — 00:00:00–00:00:22、00:06:37–00:07:22、00:55:47–00:57:06
- [[Teresa Torres｜持续产品发现]] — 00:23:58
