# Writing DNA Distiller

> Skill name: `writing-dna-skill`
>
> Use this workflow for English-language artifacts and the templates in `templates/author-corpus/en/`.

## Goal

Distill a reusable Writing DNA from the historical work of an author, publication, brand, or account. The result must be an operational rule set rather than a summary.

Use the distilled artifacts to:

1. Understand the subject's language, editorial judgment, topic logic, and visual presentation.
2. Produce style-consistent drafts without claiming they were written by the original author.
3. Compare how different authors or publications approach the same subject.

## Six Layers

| Layer | Analyze | Method | Main Output |
| --- | --- | --- | --- |
| L1 Surface Language | Vocabulary, sentence length, punctuation, rhetoric | Text statistics and close reading | `language-dna.md` |
| L2 Article Structure | Hooks, body architecture, transitions, endings | Structural annotation | `structure-patterns.md` |
| L3 Topic Logic | Timing, angle selection, priorities, exclusions | Classification and synthesis | `cognitive-framework.md` |
| L4 Source Strategy | Authorities, examples, data, screenshots | Source-role analysis | `cognitive-framework.md` |
| L5 Cognitive Frames | Values, assumptions, recurring propositions | Deep reading | `cognitive-framework.md` |
| L6 Visual Style | Images, layout, typography, color | Visual sampling and formatting analysis | `visual-style-guide.md` |

L1-L2 describe how the subject writes. L3-L5 describe how the subject selects and interprets material. L6 describes how the work is presented.

## Image Evidence

Images may carry evidence that is absent from the prose. Open and inspect screenshots, comments, conversations, charts, tables, and interface captures.

For image-heavy corpora, inspect every image in a representative sample of at least 5-10 articles. Record whether each image is evidentiary, explanatory, data-bearing, narrative, emotional, authoritative, or decorative.

## Step 1: Collect The Corpus

- Collect at least 20 complete articles.
- Prefer coverage across different periods, topics, and formats.
- Store `.md` or `.txt` files in `raw/` or `raw-corpus/`.
- Preserve images and meaningful formatting when available.
- Do not publish source material without permission.

Recommended filename format:

```text
YYYY-MM-DD article-type article-title-source.md
```

If the corpus is too small, present the result as a workflow demonstration rather than a reliable style model.

## Step 2: Build Metadata

Create one `_meta/` record per article. Include:

```json
{
  "title": "Article title",
  "date": "YYYY-MM-DD",
  "author": "Author or publication",
  "column": "Series or column name",
  "article_type": "interview | analysis | commentary | observation | review",
  "topic_tags": ["tag-1", "tag-2"],
  "hook_type": "question | scene | data | assertion | suspense",
  "structure_pattern": "thesis-body-conclusion | chronology | comparison | Q&A",
  "source_types": ["primary source", "public reference", "case comparison"],
  "word_count": 0,
  "notable": "Optional notable traits"
}
```

Do not skip metadata. It is the basis for cross-article comparison.

## Step 3: Analyze Surface Language

Measure and interpret:

- recurring nouns, verbs, modifiers, phrases, and terminology
- sentence-length distribution and paragraph rhythm
- short-sentence and long-sentence ratios
- punctuation, quotation, parenthetical, and dash habits
- heading length and title construction
- formality, directness, humor, and mixed-language habits

Do not treat frequency alone as style. Distinguish topic vocabulary from stable voice markers.

Write `language-dna.md`.

## Step 4: Extract Structure Patterns

Annotate each article as:

```text
[opening hook and length]
→ [first turn or central question]
→ [body architecture]
→ [transition pattern]
→ [closing pattern]
```

Group recurring structures by content type. For every structure, record when it is used, what reader expectation it creates, and which variations are allowed.

Write `structure-patterns.md` with at least three recurring structures when the corpus supports them.

## Step 5: Distill Topic Logic And Cognitive Frames

Analyze three connected layers.

### Topic Logic

- Which events or moments trigger publication?
- Which angles are preferred?
- Which topics are ignored or rejected?
- Does the subject lead, follow, reinterpret, or retrospectively explain a conversation?

### Source Strategy

- Which types of sources carry authority?
- How are examples, data, anecdotes, and counterexamples used?
- How is uncertainty or controversial information handled?
- What role do screenshots and other visual evidence play?

### Cognitive Frames

- What recurring assumptions shape interpretation?
- Which values determine what counts as good, bad, important, or credible?
- Which non-obvious propositions recur across unrelated topics?

Write `cognitive-framework.md`. Separate evidence-supported patterns from tentative inferences.

## Step 6: Analyze Visual Style

Record:

- image count, placement rhythm, and image-to-text ratio
- cover-image and illustration patterns
- screenshot, chart, photo, interface, meme, and decorative-image usage
- heading hierarchy, paragraph density, bolding, quotations, and separators
- recurring colors, highlight conventions, backgrounds, and callouts
- the division of labor between prose and images

When HTML is available, inspect typography and color properties. When only Markdown is available, analyze headings, emphasis, quotations, links, and image placement.

Write `visual-style-guide.md`.

## Step 7: Integrate Writing DNA

Combine the findings into `Writing-DNA.md`:

```text
Writing-DNA.md
├── Language characteristics
├── Structure patterns
├── Topic-selection rules
├── Source strategy
├── Core cognitive frames
└── Visual style
```

Keep the document concise enough to reread before every writing task. Preserve the most predictive rules, meaningful exceptions, and clear failure modes.

## Output Structure

```text
author-or-publication/
├── raw/
├── _meta/
├── language-dna.md
├── structure-patterns.md
├── cognitive-framework.md
├── visual-style-guide.md
└── Writing-DNA.md
```

## Quality Checks

- Metadata covers at least 80 percent of the corpus.
- Structure patterns cover at least three content types when supported by the corpus.
- The cognitive analysis contains at least three non-obvious, evidence-backed propositions.
- The visual analysis covers images, layout, typography, and color when those signals exist.
- `Writing-DNA.md` is concise, operational, and internally consistent.
- A draft written from the artifacts can be audited against explicit rules rather than a vague similarity judgment.
- Public output does not impersonate the source author or misrepresent authorship.
