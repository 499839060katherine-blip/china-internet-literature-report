# china-internet-literature-report

一个 Claude Code skill：围绕任意主题，生成结构化的「中国互联网研究」文献搜索报告。

## 它做什么

输入一个主题，按 **A-C-D-E** 流程产出完整报告：

- **A — Literature search**：按期刊等级（SSCI/SCI/CSSCI）检索主题文献
- **C — Scholar mapping**：识别中外核心学者与核心概念
- **D — Research proposal**：基于文献缺口给出研究提案框架
- **E — Markdown output**：按固定模板输出完整报告

报告包含：全景速览、类型学、理论脉络、文献（A=SSCI / B=CSSCI / C=其他高影响力 / D=政府政策）、学者图谱、政策时间线、跨国比较、研究提案、检索式附录。

## 核心约束（已内置，无需额外叮嘱）

- **绝不编造** SSCI 分区（Q1–Q4）、影响因子、期刊排名等学术元数据，只标收录状态
- 文献须经网络检索验证，无法核实处一律标「⚠️待核实」
- 每条文献一句话简介 + 期刊名称超链接

## 安装

把本仓库 clone 或解压到你的 skills 目录：

```bash
# 方式一：git clone（推荐）
git clone <本仓库地址> ~/.claude/skills/china-internet-literature-report

# 方式二：手动解压
unzip china-internet-literature-report.zip -d ~/.claude/skills/
```

重启 Claude Code（或新开会话）后即可用。

## 使用

直接说以下任意一种（主题词可替换）：

1. `基于报告模板，以【主题】为主题生成中国互联网研究文献搜索报告`
2. `生成【主题】文献搜索报告`
3. `新主题：【主题】`

## 目录结构

```
china-internet-literature-report/
├── SKILL.md                      # 工作流 + 规则
└── references/report-template.md # 报告模板
```
