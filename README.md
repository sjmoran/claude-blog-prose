# blog-prose

A Claude Code skill for writing blog posts that read as if a person wrote them.

![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-skill-d97757)
![License: MIT](https://img.shields.io/badge/license-MIT-blue)
![Status](https://img.shields.io/badge/status-v0.2-brightgreen)

LLMs write blog posts in a recognisable register: em-dash drama, triadic punchlines, "it's not X — it's Y" pivots, "delve", "leverage", "game-changer", and a title engineered to withhold its own point. Many readers now recognise it within a sentence, and in my experience that costs the post their trust. `blog-prose` is a set of rules that strips all of that out, keeps your work honest in both directions (no overselling, no imposter-voice underselling), and makes every factual claim checkable.

It's the blog-facing port of [`academic-prose`](https://github.com/sjmoran/claude-academic-prose): the same refusal to put rhetoric ahead of substance, in the first person, with the paper machinery taken off.

---

## The difference, in one example

**Before**, in the default LLM blog voice:

> In today's fast-paced engineering landscape, caching is more crucial than ever. We embarked on a journey to supercharge our API — and the results were nothing short of game-changing. It's not just faster; it's *transformative*. By leveraging a cutting-edge approach, we unlocked blazing-fast performance that delighted our users. The lesson? Sometimes the biggest wins come from the smallest changes.

**After**, the same post under `blog-prose`:

> A query that used to take 40ms started taking four seconds last week. I went looking, expecting a slow database, and found the cache was the problem, not the fix. Swapping the JSON parser cut p99 from 800ms to 90ms on production traffic (benchmark and flame graphs below). I'm still not sure it holds under concurrent writes; everything here was single-writer.

Both describe the same fix. The second is shorter, says what happened, gives a number you can check, and states what it doesn't know.

---

## What it enforces

The rules, in the order they appear in [`SKILL.md`](skills/blog-prose/SKILL.md):

| Section | What it does |
|---|---|
| **§1 Voice** | Plain, first-person, precise. Open on the concrete thing. Show the artifact. Mark opinion as opinion. Structure by descriptive headings, not "in this section we…". |
| **§1a Technical audience** | Defaults to an average practising data scientist unless another audience is specified. Explain unfamiliar concepts and missing reasoning steps; keep useful mathematics and remove unhelpful inventories. Applies to captions, footnotes and references too. |
| **§1b Structure for understanding** | Lowers the reader's load while keeping the depth. Intuition before implementation, each term after the idea it names, one concept per paragraph. Each section answers the question the last one raised, written as a claim rather than printed as a question. |
| **§1c Concrete explainer** | For posts that explain a technical result. Open with a concrete scenario that matches the idea, then give the formal term. Follow an impressive claim with its intuition and its inconvenient fact, and put each caveat where it applies. |
| **§1d Intellectual stakes** | For posts that report a result or a change of mind. Establish what experts believed before, and let significance come from that contrast and the evidence. Keep observation, inference, and prediction apart; separate discovery from understanding; show genuine belief updates; state the strongest objection fairly; reach a strong conclusion only once the evidence has earned it. |
| **§2 No hype** *(kept strict)* | Bans em-dash chains, rhetorical inversion, the "not X — it's Y" pivot, triadic drama, clickbait/aphoristic titles, intensifier adverbs, hype vocabulary, and "load-bearing"-style LLM-tell metaphors. |
| **§2b No self-sabotage** | The opposite failure: the imposter preamble ("I'm no expert but…"), false modesty, hedging a result you actually measured. Keep every caveat; never word the work down below what it deserves. |
| **§2c–§2e Calm register** | No rhetorical-question scaffolding, no manufactured suspense or dramatic headings, and a pass for the structural tells that word lists miss: em-dash density, meta-narration, reflexive both-sides framing. Remove defensive qualifications that add no information; retain meaningful limitations where they matter. |
| **§3 Claims are checkable** | Every empirical or factual claim that matters is verifiable in under a minute: a linked source, a number, code, or a chart. Don't blur a measurement with a guess. |
| **§4 Builder's map** | For landscape and architecture posts: plain entry, naive path, failure modes, trade-offs, design families, operational realism, modest conclusion. |
| **§4b Research synthesis** | For posts on how an idea or field developed: build an evidence map and a thesis first, tell the history as causation, group papers by argument, and calibrate certainty throughout. |

The 14-item **pre-publish self-check** (§5) runs a mechanical grep pass (em-dashes, banned vocabulary, LLM tells) and a semantic read-through, which works best as a fresh-context subagent pass on a long post. It reports pass/fail per item before the post is called done.

## Install

**As a symlinked skill** (simplest):

```bash
git clone https://github.com/sjmoran/claude-blog-prose.git
ln -s "$(pwd)/claude-blog-prose/skills/blog-prose" ~/.claude/skills/blog-prose
```

**As a plugin**, from inside Claude Code:

```
/plugin marketplace add sjmoran/claude-blog-prose
/plugin install blog-prose@claude-blog-prose
```

Once installed, Claude Code loads it automatically whenever you ask it to write, edit, or review a blog post, devlog, or Markdown article. Or invoke it explicitly with `/blog-prose`.

## Usage

Ask in plain language:

- *"Write a blog post about the caching bug I just fixed."*
- *"Tighten this intro; it's too throat-clear-y."*
- *"Review this draft for AI-slop tells before I publish."*
- *"Run the pre-publish check on this post."*

## How blog-prose differs from academic-prose

`blog-prose` and [`academic-prose`](https://github.com/sjmoran/claude-academic-prose) share three rules (no hype, no self-sabotage, checkable claims) but differ on everything formal:

| | `academic-prose` | `blog-prose` |
|---|---|---|
| Voice | collective "we" | first-person "I" |
| Structure | claims box, signposting, ≤160-word abstract | headings by scent, no abstract |
| Evidence | one protocol per headline table | link the source, show the number |
| Emphasis | no bold in running prose | bold for scannability, in moderation |
| Use for | `.tex`, journal/conference submissions | blog posts, devlogs, READMEs, web prose |

If a draft is really a paper, use `academic-prose`. If it's really a post, use this.

## Contributing

Issues and PRs are welcome, especially new banned-construction patterns as the LLM register drifts, and counter-examples where a rule misfires. The rules live entirely in [`skills/blog-prose/SKILL.md`](skills/blog-prose/SKILL.md); the voice examples in [`voice-exemplars.md`](skills/blog-prose/voice-exemplars.md).

## License

[MIT](LICENSE) © Sean Moran
