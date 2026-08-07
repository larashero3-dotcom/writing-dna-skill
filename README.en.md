# Writing DNA Distiller

[中文](README.md) | English

[![Writing DNA Distiller: distill any author's writing style into reusable Writing DNA for AI agents](assets/writing-dna-hero-en.png)](https://moxt.ai/hub?view=skill&id=writing-dna-skill)

Skill name: `writing-dna-skill`

An agent skill for distilling the writing style of any author or publication into reusable rules.

This is not a simple "write like this person" prompt. It gives an agent a complete distillation workflow for turning a corpus of full articles into reusable Writing DNA: language, structure, topic selection, source strategy, cognitive frames, and visual style. Before writing, the agent can reread these documents to reproduce the target style with greater consistency.

This skill was created at [moxt.ai](https://moxt.ai).

> [**Open Writing DNA Distiller on MoxtHub →**](https://moxt.ai/hub?view=skill&id=writing-dna-skill)

## The Problem It Solves

When people ask AI to imitate an author, they often provide a few examples and say, "Write in this style." The result is unreliable because the agent is guessing from surface-level tone.

`writing-dna-skill` takes a different approach. Instead of asking the agent to imitate immediately, it first analyzes a substantial corpus of complete articles, turns recurring style choices into explicit rules, and then uses those rules to guide future writing.

The skill examines:

- recurring words, sentence structures, punctuation, and rhythm
- how articles open, develop, transition, and close
- which topics the author selects or avoids
- which sources, examples, data, and screenshots appear repeatedly
- the worldview, value judgments, and assumptions behind the writing
- image strategy, layout, typography hierarchy, and color when the source is visual

## Best For

- analyzing the stable writing style of an author, account, or publication
- turning your own writing history into a reusable style asset
- comparing how different authors approach the same topic
- giving an AI agent more reliable context for style-consistent writing

## Chinese And English Artifacts

The skill keeps the conversation language separate from the artifact language. A user may speak Chinese while analyzing an English newsletter, or speak English while building a Chinese writing system.

- Chinese artifacts use `templates/author-corpus/zh/` and Chinese filenames.
- English artifacts use `templates/author-corpus/en/` and English filenames.
- An explicit user choice takes priority. Otherwise, the source corpus determines the artifact language.

## What It Can Analyze

The skill turns "style" from a vague impression into rules that can be recorded, reused, and checked. It looks beyond tone to understand why an article is written in a particular way, how evidence is organized, and how conclusions are formed.

Suitable source material includes:

- long-form articles, newsletters, columns, blogs, and public-account posts
- image-led posts on Xiaohongshu, Weibo, and other social platforms
- your own archive of past writing
- articles by multiple authors writing about the same subject

If the source includes screenshots, illustrations, charts, or distinctive formatting, preserve them. For visual publications, image placement, evidentiary screenshots, heading hierarchy, and whitespace can be as important as the prose itself.

## Six Layers of Distillation

| Layer | What It Analyzes | Output |
| - | - | - |
| **L1 Surface Language** | Word frequency, sentence length, punctuation, rhetoric, recurring expressions | `language-dna.md` |
| **L2 Article Structure** | Opening hook, body architecture, transitions, closing pattern | `structure-patterns.md` |
| **L3 Topic Logic** | Timing, angle selection, topic priorities | `cognitive-framework.md` |
| **L4 Source Strategy** | References, authorities, examples, and use of data | `cognitive-framework.md` |
| **L5 Cognitive Frame** | Worldview, values, assumptions, and recurring propositions | `cognitive-framework.md` |
| **L6 Visual Style** | Image strategy, formatting, typography hierarchy, and color | `visual-style-guide.md` |

In short:

- L1-L2 explain how the author writes.
- L3-L5 explain how the author thinks.
- L6 explains how the work is presented.

Reliable style reproduction needs all three. Language alone may sound similar while expressing different ideas. Structure alone may resemble the original outline but miss the voice. Ignoring visual style can make image-led content feel wrong even when the prose is close.

## Corpus Requirements

For a real distillation, prepare:

- at least 20 complete articles
- `.md` or `.txt` source files
- material from different periods, topics, and article types when possible

`examples/format-only/` demonstrates the expected directory structure. It is not a reliable style corpus, and a few short samples should not be used to judge the skill's full capability.

## Distillation Workflow

A complete distillation normally follows six steps:

1. **Collect the source corpus:** Gather at least 20 complete articles and place them in `raw/` or `raw-corpus/`.
2. **Build metadata:** Record the title, date, article type, topic, hook, structure, and source strategy for each article in `_meta/`.
3. **Analyze language DNA:** Measure word frequency, sentence length, punctuation, paragraph rhythm, recurring expressions, and mixed-language habits. Write `language-dna.md`.
4. **Extract structure patterns:** Mark openings, turns, body organization, and endings, then turn repeated article shapes into `structure-patterns.md`.
5. **Identify cognitive frames:** Distill topic logic, source preferences, values, assumptions, and recurring propositions into `cognitive-framework.md`.
6. **Document visual style:** When the corpus includes images or distinctive formatting, analyze image roles, screenshot evidence, typography, color, and text-image collaboration. Write `visual-style-guide.md`.

The agent then combines the results into `Writing-DNA.md`, the main document to reread before writing in the distilled style.

## Output

A complete project usually produces:

```text
author-or-publication/
├── raw/                    # Complete source articles
├── _meta/                  # Article-level metadata
├── language-dna.md          # L1 analysis
├── structure-patterns.md    # L2 analysis
├── cognitive-framework.md   # L3-L5 analysis
├── visual-style-guide.md    # L6 analysis
└── Writing-DNA.md          # Integrated style document
```

`Writing-DNA.md` is the primary reusable context for future writing sessions.

## Quick Start

We recommend opening [`writing-dna-skill` directly on MoxtHub](https://moxt.ai/hub?view=skill&id=writing-dna-skill), where Moxt's large context window and AI-native file workflow make it easier for an agent to process complete long-form corpora.

1. Collect or ask an agent to collect at least 20 complete articles and place them in `raw/` or `raw-corpus/`.
2. Ask the agent to use `writing-dna-skill`, or to read `SKILL.md` and `references/workflow.en.md`, before processing the corpus.
3. Wait for the agent to produce:
   - `language-dna.md`
   - `structure-patterns.md`
   - `cognitive-framework.md`
   - `visual-style-guide.md`
   - `Writing-DNA.md`
4. Before future writing tasks, ask the agent to reread all distilled style documents.

Start a distillation with:

```text
Use writing-dna-skill to distill the writing style from every article in this directory.
```

## Writing With a Distilled Style

For more consistent results, do not load the style documents only once. Before each writing task:

1. Give the agent the topic, audience, purpose, and relevant context.
2. Ask it to reread every distilled style document.
3. Require the draft to follow the language, structure, cognitive, and visual rules.
4. If the result does not feel accurate, ask the agent to audit the draft against `language-dna.md`, `structure-patterns.md`, and `cognitive-framework.md`, then rewrite it.

Example:

```text
Read every distilled style document in this author's directory, especially
Writing-DNA.md, language-dna.md, structure-patterns.md,
cognitive-framework.md, and visual-style-guide.md.

Then write an article for the target audience using those rules.
Topic: ...
```

## Why It Works

The skill separates writing style into layers that an agent can inspect, execute, and audit. Instead of relying on a vague impression of similarity, it records explicit style rules and directs the agent's attention back to them before each writing task.

The result is a reusable set of instructions rather than a one-time imitation prompt.

## Important Boundaries

This project is intended for learning, analysis, style research, and building personal writing assets. Do not use it to impersonate an author, mislead readers, or violate copyright.

Do not place unauthorized source articles in a public repository. Public releases should contain directory templates, field schemas, documentation, and examples you have permission to share.

## Repository Structure

```text
writing-dna-skill/
├── SKILL.md
├── README.md
├── README.en.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── references/
│   └── workflow.en.md
├── docs/
│   ├── release-checklist.md
│   └── usage-boundaries.md
├── templates/
│   └── author-corpus/
│       ├── zh/                  # Chinese templates and filenames
│       └── en/                  # English templates and filenames
└── examples/
    └── format-only/
```

## License

[**Use writing-dna-skill on MoxtHub →**](https://moxt.ai/hub?view=skill&id=writing-dna-skill)

MIT
