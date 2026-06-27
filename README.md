# 写作蒸馏器.skill

英文名：`writing-dna-skill`

一个用于蒸馏任意账号/作者写作风格的 skill，通过把一批文章拆解成可复用的 Writing DNA：语言、结构、选题、素材、认知框架与视觉风格，它可以复刻这种写作风格。

## 适合什么

- 分析某个账号/作者的稳定写作风格
- 沉淀自己的写作风格资产
- 对比不同作者在同一议题上的表达差异
- 给 agent/AI 提供更稳定的风格复刻上下文

## 语料要求

真实蒸馏建议准备：

- 最好是 20 篇以上该作者的完整文章（素材越多，风格覆盖越完整，效果越好）
- 单篇最好大于 1000 字
- 文件格式建议为 `.md` 或 `.txt`

`examples/format-only/` 只用于演示目录格式，不代表真实蒸馏效果。不要用少量短文评估这个 skill 的上限。

## 快速上手

1. 让 agent 抓取或手动准备20 篇以上的完整文章，放入命名为 `raw/` 或 `raw-corpus/`的文件夹。
2. 让 agent 使用 `writing-dna-skill`，或阅读 `SKILL.md` / `写作蒸馏器.skill.md`，并按流程蒸馏所有文章。
3. 等待 agent 输出：
   - `语言DNA.md`
   - `文章结构模板.md`
   - `写作视角与认知框架.md`
   - `视觉风格指南.md`
   - `Writing-DNA.md`
4. 后续写作前，让 agent 先重新阅读所有蒸馏产物，再按该风格写作。

## 重要边界

这个项目用于学习、分析、风格研究和个人写作资产沉淀。请不要用于冒充作者本人、误导读者，或侵犯他人版权。

开源仓库不应包含未经授权的原文语料。你可以放目录模板、字段模板、说明文档和自己拥有版权的示例文本。

## 文件结构

```text
writing-dna-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── 写作蒸馏器.skill.md
├── docs/
│   ├── release-checklist.md
│   └── usage-boundaries.md
├── templates/
│   └── author-corpus/
│       ├── raw/
│       ├── _meta/
│       ├── 语言DNA.md
│       ├── 文章结构模板.md
│       ├── 写作视角与认知框架.md
│       ├── 视觉风格指南.md
│       └── Writing-DNA.md
└── examples/
    └── format-only/
```

## License

MIT
