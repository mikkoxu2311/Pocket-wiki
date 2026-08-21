---
type: episode
guest: Ronny Kohavi
date: 2023-07-27
source_file: "[[ronny-kohavi]]"
external_url: https://www.youtube.com/watch?v=hEzpiDuYFoE
status: expanded-pilot
insight_count: 16
---

# Ronny Kohavi — A/B Testing

## 这一期在回答什么

为什么实验结果经常反直觉甚至错误？Ronny 讨论失败率、长期指标、大改版、SRM、Twyman's Law、统计显著性和平台治理，核心是让组织能够信任证据。

## 核心洞见

### 1. 很小的界面变化也可能产生巨大结果
**例子：** 搜索结果中交换两行信息显著改变收入；直觉很难预测注意力和行为链。微小排序变化会改变注意力、点击和后续收入链，规模放大后形成巨大结果；正因这种非线性难靠直觉预测，才需要受控实验。

> **原话（08:34）：** “But to me, this was an example of a tiny change that was the best revenue generating idea in Bing's history, and we didn't rate it properly.”

**时间戳：** 04:56–10:35

### 2. “一小时创造巨大提升”是罕见异常
**结论：** 应建立可重复实验系统，而不是用传奇案例设定项目预期。传奇案例证明上行空间存在，却不代表每小时工作都应产生同等收益；把尾部结果当基线，会诱导团队挑指标和隐藏失败。更健康的预期是用大量可信实验积累小幅收益，并把极端赢家当作无法预先指定的尾部回报。

> **原话（10:57）：** “Everybody wants these amazing results, and I show them in chapter one in my book, multiple of these small efforts, huge gain.”

**时间戳：** 10:35–13:17

### 3. 大多数 idea 不会产生正向结果
**证据：** 在成熟实验组织里约 80%–90% 实验未达到预期；这不是团队无能，而是人类预测复杂系统的能力有限。复杂产品中因果关系难以直觉推断，成熟团队的大多数想法也不显著；失败率高说明便宜否证比高层自信更重要。

> **原话（14:09）：** “Not every experiment maps to an idea.”

**时间戳：** 13:17–19:23

### 4. 组织必须保存反直觉学习
**方法：** 建 experiment repository，记录假设、结果、guardrail 和解释；否则人员流动后同一失败会被重新发现。仓库要保存假设、变体、指标、guardrail 和解释，让后来者知道什么已被否证及其条件；只记录赢家会制造幸存者偏差。

> **原话（19:34）：** “The other thing that's very beneficial is just to have your whole history of experiments and do some ability to search by keywords.”

**时间戳：** 19:23–20:45

### 5. Experimentation 不等于只做小赌注
**结论：** 大胆创新仍可实验；区别是 rollout 可控、成功标准预先定义，而不是因投入大就免于验证。大创新仍可先测试关键假设、分阶段 rollout 并保留回滚；实验反对的是不可学习的一次性发布，不反对高风险高回报方向。

> **原话（27:25）：** “Then you have the ability to test everything and make sure that you're not degrading and getting value out of experimentation.”

**时间戳：** 20:45–28:00

### 6. 小团队先看实验所需样本，而非公司年龄
**判断：** 根据 baseline、最小有意义变化和流量估算 duration；若要数月才有 power，应用定性研究或更大的 outcome。所需样本由基线率、最小有意义变化和噪声决定，和公司成立年限没有直接关系；样本不足时应换问题或证据方法。

> **原话（25:14）：** “But what I find is that in software, it is so easy to run A/B testing and it is so easy to build a platform.”

**时间戳：** 24:48–28:00

### 7. Overall Evaluation Criterion 防止单指标获胜
**方法：** 把目标 metric 与用户体验、可靠性等 guardrails 组合；收入上涨若靠伤害用户，不应判赢。OEC 把业务目标与体验、可靠性等 guardrail 放在同一判定里，防止团队通过伤害用户或未来价值赢得短期指标。

> **原话（30:16）：** “These are key metrics that were part of the overall evaluation criteria, that we've used.”

**时间戳：** 28:00–32:43

### 8. 长期效应需要 holdout 或经过验证的模型
**边界：** 短期 proxy 只有在历史上能预测长期结果时才可信；重要变化可保留长期 control。长期 holdout 能直接观察持续效应，proxy 则必须先用历史关系验证；未经验证的短期点击不能被想当然地当成长期价值。

> **原话（32:57）：** “One is you can run long-term experiments for the goal of learning something.”

**时间戳：** 32:43–36:31

### 9. Big-bang redesign 几乎总是难以学习
**推理：** 数十项变化混在一起，即使失败也不知道原因；应尽量分解，确需重构时保留阶段 rollout 和旧体验基线。一次改变太多元素，即使整体变差也无法定位责任；分步测试保留学习归因，确需重构时至少要有阶段基线和回退路径。

> **原话（36:47）：** “So the right way to do this is to say, "Yes, we want to do a redesign, but let's do it in steps and test on the way and adjust," so you don't need to take 17 new changes, that many of them are going to fail.”

**时间戳：** 36:31–43:35

### 10. 可以给 big bets 固定资源比例
**结论：** 例如约 20% 探索高风险方向、80% 持续改进；比例不是定律，作用是避免两类工作互相吞噬。固定比例保证 big bets 不被短期胜率排挤，同时限制单次失败对整体资源的吞噬；比例仍应随公司风险承受能力调整。

> **原话（43:03）：** “I do want to allocate some percentage of resources to big bets. [...] What I'm telling you is 80% of the time, you will fail. So be ready for that.”

**时间戳：** 43:03–45:41

### 11. Covid 展示了实验无法覆盖所有冲击
**边界：** Airbnb 面临需求结构突变时需要战略判断和快速行动；实验是决策工具，不是假装世界稳定。疫情等全局冲击同时影响 control 和 treatment 之外的环境，历史实验无法覆盖所有未来状态；模型外变化需要业务判断与额外监测。

> **原话（48:34）：** “These are things that you can really answer with the controlled experiments, and sometimes it means that you might have to replicate them six months down when Covid say is not as impactful as it is.”

**时间戳：** 45:41–50:01

### 12. Trust 是实验平台最重要的产品
**结论：** 分流容易，确保 exposure、指标、统计和日志正确很难；团队若遇到几次错误结果，就会退回职位权力。平台首先要让人相信随机化、指标和分析没有系统错误；一个不可信系统产出越快，组织就越快把噪声变成决策。

> **原话（52:43）：** “And so to me, it is very important that when you present this and say, "This is science, this is a controlled experiment, this is the resolve," you better believe that this is trustworthy.”

**时间戳：** 50:01–55:26

### 13. Sample Ratio Mismatch 是基础健康检查
**证据：** 微软自动检查后仍发现约 8% 实验存在 SRM；预期 50/50 却显著偏离，说明分配或数据管道有问题。SRM 检查实际分流是否偏离设计比例，能及早发现埋点、分配或过滤错误；基础健康未通过时，后续显著性没有解释价值。

> **原话（57:06）：** “And there's a paper that was published, 2018, where we share that at Microsoft, even though we'd be running experiments for a while, is around 8% of experiments that suffered from the sample ratio mismatch.”

**时间戳：** 55:26–01:00:45

### 14. Twyman's Law：过于惊人的数字通常有问题
**做法：** 先查 instrumentation、单位、机器人、重复用户和分流，再庆祝异常大提升。过于惊人的结果更可能来自数据管道、单位或实验污染，因此先排错再庆祝；Twyman's Law 是调查优先级，不是否认所有突破。

> **原话（01:00:51）：** “So Twyman's law, the general statement is if any figure that looks interesting or different is usually wrong.”

**时间戳：** 01:00:45–01:02:14

### 15. P-value 不是“结果为真的概率”
**结论：** 它是在零假设成立时观察到当前或更极端数据的概率；需结合 power、效应大小和多重检验。P-value 描述在零假设成立时看到当前或更极端数据的概率，不是“方案正确概率”；误读会把统计阈值变成错误确定性。

> **原话（01:03:08）：** “And we're computing the probability that the data we're seeing matches the hypothesis, this null hypothesis.”

**时间戳：** 01:02:14–01:07:44

### 16. 从少数可信实验和平台化开始改变文化
**方法：** 找争议大、可快速验证的案例，让怀疑者参与指标设计；随后统一分流、检查和报告，避免每队自造统计系统。文化改变从少量高信任实验开始，让团队亲眼看到直觉被推翻，再把随机化、指标和知识库平台化；先追数量会复制不可信流程。

> **原话（01:07:17）：** “I think today, there's enough vendors that provide good experimentation platforms that are trustworthy, that I would say not a good way to consider using one of those.”

**时间戳：** 01:07:44–01:14:11


## 这一期的完整逻辑链

可信实验系统的起点不是追求更多测试，而是承认多数想法不会奏效，并确保随机化、样本比例、统计解释和 OEC 都可靠。小变化也可能产生大结果，大赌注则应被分解并渐进 rollout；长期影响需要 holdout 或经历史验证的 proxy。实验仓库保存反直觉学习，使失败真正降低下一次决策成本。

## 连接
- [[可信实验与 A-B Testing]]
- [[激活指标]]
- [[留存]]
- [[产品发现（Product Discovery）]]
