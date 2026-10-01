# QBS Science Writing

把科研写作书中的方法，转成可以调用的写作 Skill。

An independent, book-based AI skill for scientific manuscript structure and revision, drawing on Hilary Glasman-Deal's *Science Research Writing*, second edition.

## 方法来源

本项目依据《Science Research Writing: for native and non-native speakers of English》第二版，选择性提炼读者导向、功能拆解、章节结构、句子衔接、贡献归属与语言确定性。它不是原书、逐页翻译或官方配套产品。

QBS 是本项目的技能组织方式，不是原书中的术语。书中方法被转写为可执行指令，技能的调用流程不代表作者规定了唯一写作顺序。

## 能做什么

- 先判断句子和段落的任务，再调整结构和语言。
- 梳理 Introduction、Methods、Results、Discussion、Conclusion、Abstract 和 Title 的关系。
- 逆向拆解目标论文的信息组织方式，而不复制其表述。
- 检查术语、时态、指代、贡献归属和确定程度是否符合原意。

## 文件结构

```text
qbs-science-writing/
  SKILL.md
  agents/openai.yaml
  references/book-framework.md
  references/language-and-meaning.md
  references/source-map.md
```

## 使用

在支持该技能格式的 Agent 中加载本目录；`SKILL.md` 是入口，`references/` 按任务需要读取。目录名使用 `qbs-science-writing`。仅下载仓库不等于平台已自动启用技能，具体加载方式取决于所用工具。

示例请求：

```text
请使用 $qbs-science-writing 修改下面的段落。
先判断它的写作功能，再调整结构与语言。
保留事实、数值和引用，不补造信息。
原文：……
```

```text
请使用 $qbs-science-writing 拆解这段目标论文：
标注每句的作用，提炼信息顺序，并解释哪些结构可以迁移。
文本：……
```

## 原则与边界

先结构，后语言；先准确，后精练。模型是可选择和调整的功能组合，不是固定模板。近期目标论文可以帮助校准写作惯例，但单篇例文不能代表普遍规则。

技能改善表达，不验证研究真实性，也不保证录用。缺失的事实需要作者补充，当前期刊要求应另行核实。

本仓库仅收录方法转述和技能配置，不附带原书 PDF、扫描页、习题答案或大型词汇表。完整教学内容请阅读合法获取的原书。出处与页码见[来源索引](references/source-map.md)。
