---
name: blog-prose
description: Rules for writing, revising, or reviewing blog posts and other public web prose — devlogs, technical write-ups, opinion pieces, tutorials, announcements, and READMEs-as-posts. Use whenever the task involves a blog post, a Markdown post, a personal-site article, or whenever the user asks to write, edit, polish, restructure, or check a post, even if they only say "write a post about X", "tighten this intro", or "make this readable". Also use before declaring any post finished, to run the pre-publish self-check. For academic papers (.tex, journal/conference submissions), defer to the academic-prose skill instead.
---

# Blog Prose

This skill ports the academic-prose voice to the blog. It keeps the parts that travel — the refusal to put rhetoric ahead of substance, and the habit of making claims checkable — and relaxes the academic machinery (no abstract word limits, no claims box, no "the remainder of this post is structured as follows", no Protocol paragraphs). A blog post should read like a clear person talking, not like a paper with the formatting filed off.

Four rule sets, applied in this order whenever blog prose is written or edited:
1. **Voice** — plain, first-person, conversational but precise (§1).
2. **No hype** — strip constructions that put rhetoric ahead of substance (§2). Kept strict from the paper rules; the temptation to be punchy is higher on a blog, not lower.
3. **No self-sabotage** — keep every fact and caveat, but never word the work down more than it deserves (§2b).
4. **Claims are checkable** — when a claim is empirical or factual, make it easy to verify (§3). This is evaluability, relaxed for the web.

Then run the **pre-publish self-check** (§4) before calling a post done. If an instruction in the conversation conflicts with a rule here, flag the conflict rather than silently overriding.

Rationale (one line): a reader decides in the first paragraph whether to keep reading and whether to trust you; plain prose earns the first, checkable claims earn the second.

## 1. Voice — plain, first-person, precise

Write the way a clear, honest person explains something they actually did or thought. Plain, direct, economical — but a blog is allowed warmth, narrative, and a point of view that a paper is not.

- **Person:** first-person singular — "I built", "I found that", "I was wrong about". Address the reader as "you" when it helps ("you might expect X; it turns out Y"). Use "we" only for genuinely shared work or when walking the reader through a derivation together.
- **Openings:** start with the concrete thing — a problem you hit, a result that surprised you, a question worth an afternoon. No throat-clearing ("In today's fast-moving world…"), no abstract-style "This post studies…", and no slogan or aphorism (see §2). A short scene or a blunt statement of the result both work.
- **Contractions and rhythm:** contractions are fine ("it's", "didn't"). Vary sentence length for rhythm — a short sentence after two long ones lands. But still aim for one main claim per sentence; rhythm is not an excuse for a clause pile-up.
- **Intuition first, formalism optional:** lead with the plain-language reading; bring in notation, equations, or code only when they earn their place, and gloss them immediately. A blog reader will forgive you for skipping the proof; they won't forgive an unglossed symbol.
- **Show the thing:** prefer a concrete example, a code block, a chart, or a real number over an abstract description of it. "It dropped p99 from 800ms to 90ms" beats "it substantially improved latency".
- **Structure by scent, not by signposting:** use descriptive headings so a scanner can navigate, but drop the academic "The remainder of this post is structured as follows" and "In this section we…". Let the headings and the first sentence under each do that work.
- **Formatting for the screen:** bold for genuine emphasis or scannability is allowed in moderation (a paper bans this; a blog reader skims). Bullet lists for genuinely list-shaped content. Don't bold whole sentences, don't bullet prose that wants to be a paragraph, and don't let formatting substitute for a clear sentence.
- **Opinion is allowed, and marked as opinion:** a blog can argue and take sides. Say "I think" / "my guess is" / "I'd bet" so the reader can tell a judgement from a measurement. Don't dress an opinion as a finding, and don't dress a finding as a mere opinion (§2b).
- **Endings:** close on what you'd do next, what you're still unsure about, or what the reader should take away — not a triumphant restatement and not a limp "anyway, that's it". One honest forward-looking sentence beats a summary paragraph.
- **Spelling:** pick one variant (British or American) and hold it with zero mixing. Default to British unless the venue says otherwise.

Do not: open with a dictionary definition or a rhetorical question stack; pad with qualifiers; chain subordinate clauses; write a SEO-keyword-stuffed paragraph; adopt LinkedIn-influencer or press-release register.

## 2. No hype (mandatory — kept strict from the paper rules)

Banned constructions — rewrite on sight, in drafts and in any text being edited. These are the same tells that flag a paper as overwritten, and they flag a blog post as AI slop or marketing even faster.

- **Em-dash chains.** Em-dashes are fine on a blog in moderation — one clean appositive like this. The ban is on the *chain*: never nest a clause inside an em-dash pair, and don't use three em-dashes in a paragraph to stage drama. If a sentence leans on em-dashes for momentum, rewrite it flat.
- **Rhetorical inversion.** "A good abstraction, it turns out, needs no documentation" → "It turns out a good abstraction needs no documentation." Subject, verb, object.
- **The pivot.** "It's not a cache — it's a contract", "not because it's fast but because it's simple", "the speed isn't the point; the point is X". State what is true; don't stage a reversal for effect.
- **Triadic drama.** "It scales. It composes. It just works." — three parallel punchy fragments read as a keynote slide. Use an ordinary sentence or a plain list.
- **Clickbait and aphoristic titles.** No "The X Is the Y" empty-profound titles, no curiosity-gap headers ("You won't believe what happened next", "I tried X so you don't have to" when you didn't), no "Here's why X changes everything". A title should say what the post is about and, ideally, what you found. Personality in a title is fine; a withheld payload is not.
- **Intensifier adverbs.** Crucially, importantly, notably, remarkably, surprisingly, incredibly, massively — delete. If a thing is surprising, show why and let the reader be surprised.
- **Hype vocabulary.** "game-changer", "revolutionary", "blazing-fast", "seamless", "effortless", "powerful", "robust", "leverage", "unlock", "supercharge", "delve", "in the realm of", "it's worth noting that". Cut or replace with the concrete fact.
- **Stacked hedges.** One caveat per sentence at most; move the rest to their own sentences.
- **"Load-bearing" and structural/engineering metaphors used for emphasis.** Don't call a sentence, idea, or assumption "load-bearing", "the linchpin", "the cornerstone", or say it "does the heavy lifting" / "carries the weight". (A literal load-bearing wall in a post about construction is obviously fine.) Say plainly what the thing does.

Read-aloud test: any sentence that sounds like a conference keynote, a tweet engineered to go viral, or a product landing page gets rewritten flat. Prefer the plain version over the memorable one. A blog earns memorability from a real result or a real insight, not from the sentence shape.

## 2b. No self-sabotage (mandatory)

§2 forbids overselling; this forbids the opposite, which is just as common on personal blogs: the imposter voice. Keep every fact, number, caveat, and mistake — honesty is non-negotiable. The rule governs only *wording*: don't word your work down below what it deserves.

Rewrite on sight:

- **False modesty and the imposter preamble.** "This is probably obvious to everyone but me", "I'm no expert but", "this is a hacky mess", "apologies for the long post" — delete. If the work is rough, say specifically what's rough ("I only tested this on one dataset"); don't blanket-apologise for existing.
- **Self-deprecating verbs for neutral outcomes.** A result that came out lower is "lower" or "didn't beat X", not "a failure" or "useless". Reserve failure language for actual failures. Owning a real mistake is good blogging; pre-emptively trashing fine work is not.
- **A negative result is a finding.** "I expected X and got the opposite" is one of the most valuable things a blog can publish. Frame it as the finding it is, not as an embarrassing admission.
- **Don't hedge a thing you actually measured.** If you have the number, state it. "It's maybe a bit faster, I think?" when you have a benchmark in hand → "it's 3× faster on this workload (benchmark below)". Keep the genuine caveat ("only measured on my laptop"); drop the reflexive flinch.
- **Mark opinion as opinion, but don't apologise for it.** "I think X" is a clean way to state a view. "This is just my dumb opinion and I'm probably wrong" is not — it tells the reader to discount you before they've read the argument.

Read-aloud test: any sentence that makes you sound less competent or your result less real than it actually is, where a neutral rephrasing would fix it *without changing a single fact or dropping a caveat*, gets rephrased.

## 3. Claims are checkable (mandatory — evaluability, relaxed for the web)

A blog reader who hits an unsupported claim does one of two things: takes it on faith, or stops trusting you. Make the claim checkable instead. This is the paper's evaluability rule with the formal machinery removed — no numbered claims box, no one-protocol-per-table, no abstract word count. The spirit stays: a reader should be able to verify any claim that matters in well under a minute.

- **Empirical claims show their evidence inline or one click away.** A performance number gets the benchmark, the code, or a chart; a "X is faster than Y" gets the conditions it was measured under, in the same sentence or the next ("on a 10k-row table, on my M2; your mileage will vary"). If you can't back it, soften it to an opinion or cut it.
- **Link your sources.** A factual claim about someone else's work, a library, a paper, or an event links to the thing. A quote links to where it's from. No "studies show" without the study.
- **Show the real artifact.** Prefer the actual code, the actual config, the actual output over a paraphrase. If the post is about a repo, link the repo. If a snippet is simplified for readability, say so.
- **Separate what you measured from what you believe.** Measurements get evidence (§3); beliefs get "I think" (§1). Don't blur the two — the most damaging blog move is presenting a guess with the confidence of a result.
- **One honest number, not a best-case number.** If you cherry-picked the run that looked best, say so or don't report it. Report the number a skeptical reader would get, not the demo number.
- **Reproducibility, lightweight.** When practical, give the reader enough to reproduce: the command, the versions, the dataset, the gist link. A post that can be re-run is worth ten that can't.

## 4. Pre-publish self-check (run before declaring any post done)

1. Read the opening aloud. Does it start on the concrete thing, or on throat-clearing / a slogan / a definition? Fix the opening if it doesn't earn the next paragraph.
2. Every empirical or factual claim that matters: is it backed by a linked source, a number, code, or a chart — verifiable in under a minute? Flag any bare claim and either support it, soften it to a marked opinion, or cut it.
3. Banned-construction check — TWO stages, both mandatory:
   a. Mechanical: grep for em-dashes (look for chains and nested pairs, not single appositives), intensifier adverbs, the hype-vocabulary list (§2), and the LLM-tell metaphors ("load.?bearing", "linchpin", "cornerstone", "heavy lifting", "delve", "in the realm of", "it's worth noting"); count and justify every remaining instance — the justified count should be zero.
   b. Semantic: greps can't catch inversions, pivots, triadic fragments, clickbait titles, keynote sentences, or marketing register. Read every sentence and every heading for them. For a long post, run this as a fresh-context pass — hand the full draft and the §2 ban list to a subagent and have it return line-numbered violations with flat rewrites — then apply the fixes. Never report this item as PASS on the strength of stage (a) alone.
4. Self-sabotage sweep (§2b): scan for the imposter preamble, false modesty, self-deprecating verbs on neutral outcomes, and hedges on things you actually measured. Reframe each neutrally while keeping every fact and caveat. Re-read the opening and the closing specifically — those set and leave the impression.
5. Title check: does it say what the post is about (and ideally what you found), without clickbait or empty aphorism?
6. Formatting check: bold and lists used for genuine emphasis/structure, not sprayed for energy. No bolded full sentences, no bulleted paragraphs.
7. Opinion/measurement check: every "I think"-class statement is marked as a view; every measurement has its evidence. Neither is disguised as the other.
8. Spelling consistent with the chosen variant throughout — no mixing.

Report the outcome of this checklist to the user explicitly — pass/fail per item — before calling the post finished.

## One-line summary

Write like a clear person talking — first person, concrete, one claim per sentence, intuition before formalism — strip every construction that puts rhetoric ahead of substance, word your work neither above nor below what it deserves, and make every claim that matters checkable in under a minute.

## Relationship to academic-prose

This skill governs blog posts and public web prose. For academic papers (.tex files, journal/conference submissions, abstracts, rebuttals), defer to the **academic-prose** skill, which is stricter on machinery (claims boxes, one-protocol-per-table, abstract word limits, signposting) and uses the collective "we". The two share a spine — no hype, no self-sabotage, checkable claims — but a blog relaxes the formal scaffolding and speaks in the first person. If a post is really a paper draft in disguise, use academic-prose instead. If another general writing or style skill conflicts with this one on a blog post, follow this skill and note the conflict.
