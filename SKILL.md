---
name: china-internet-literature-report
description: Use when the user asks to generate a themed Chinese internet research literature search report — triggers include "基于报告模板…生成文献搜索报告", "生成【主题】文献搜索报告", "新主题：【主题】", or any request for a topic literature + policy search report graded by SSCI/CSSCI with a research proposal.
---

# 中国互联网研究文献搜索报告

围绕一个主题，生成结构化的「中国互联网研究」文献搜索报告：按期刊等级检索文献、识别核心学者、给出研究提案，输出到固定模板。

## 触发口令（主题词可替换）

1. **完整版**：`基于报告模板，以【主题】为主题生成中国互联网研究文献搜索报告`
2. **简洁版**：`生成【主题】文献搜索报告`
3. **极简版**：`新主题：【主题】`

## 执行流程（A-C-D-E）

1. **A — Literature search**：按期刊等级检索主题文献（SSCI/SCI/CSSCI/EI/AHCI）
2. **C — Scholar mapping**：识别该主题的中外重要学者及其核心概念
3. **D — Research proposal**：基于文献缺口提出研究提案框架
4. **E — Markdown output**：按模板输出完整报告

## 硬性规则（违反即作废）

### 1. 绝不编造学术元数据（最高优先级）
- 只标「（SSCI）收录」/「（CSSCI）」等**收录状态**，绝不编造 SSCI 分区（Q1–Q4）、影响因子、中科院分区、JCR 排名
- 无法核实的卷期页、DOI、作者机构一律标「⚠️待核实」
- 宁可说"不知道"，不可编造

### 2. 文献必须真实，经网络检索验证
- 用网络检索核实关键文献的**作者、标题、期刊、年份**
- 优先报告能通过公开网页确认的信息，不凭记忆虚构条目

### 3. 格式规则
- 文献按期刊等级分类：**A = SSCI/SCI，B = CSSCI（分顶级/一般），C = 其他高影响力来源，D = 政府政策/官方文件**
- 每条文献附**一句话简介**（概括核心发现与贡献，不写"该文献对论文的意义"）
- 所有期刊名称加**超链接**（SSCI 链期刊官网，CSSCI 链知网采编平台或期刊官网）
- 政策文件单独列为 D 类，按时间排序，附发布部门、核心内容、研究意义

## 报告结构

> 摘要 → 第一部分全景速览（八大主题）→ 第二部分专题深化（类型学 + 理论 + 文献 A/B/C/D + 学者 + 政策 + 比较 + 提案）→ 第三部分发现与建议 → 附录（获取资源 + 检索式）

完整模板见 `references/report-template.md`（以「平台劳动」为例填充，更换主题时保留全部 Markdown 格式与表格结构，仅替换主题相关内容）。

## 输出位置

默认保存到用户的研究目录下（原工作流为 `personal/china_internet/literature report/`，文件命名 `YYMMDD_{主题}_literature_report_{日期}.md`）。若用户未指定目录，先询问；不要写死到某个人的绝对路径。

## 注意事项

- 生成日期自动标注为当日
- 报告末尾附「报告局限性说明」，注明非系统性文献综述、待核实条目需二次确认
- 如需针对子主题或理论视角深化，主动询问
