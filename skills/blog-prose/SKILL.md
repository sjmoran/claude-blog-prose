---
name: blog-prose
description: Rules for writing, revising, or reviewing blog posts and other public web prose — devlogs, technical write-ups, opinion pieces, tutorials, announcements, and READMEs-as-posts. Use whenever the task involves a blog post, a Markdown post, a personal-site article, or whenever the user asks to write, edit, polish, restructure, or check a post, even if they only say "write a post about X", "tighten this intro", or "make this readable". Also use before declaring any post finished, to run the pre-publish self-check. For academic papers (.tex, journal/conference submissions), defer to the academic-prose skill instead.
---

# Blog Prose

This skill ports the academic-prose voice to the blog. It keeps the parts that travel — the refusal to put rhetoric ahead of substance, and the habit of making claims checkable — and relaxes the academic machinery (no abstract word limits, no claims box, no "the remainder of this post is structured as follows", no Protocol paragraphs). A blog post should read like a clear person talking, not like a paper with the formatting filed off.

Six rule sets, applied in this order whenever blog prose is written or edited:
1. **Voice** — plain, first-person, conversational but precise (§1).
2. **No hype, no machine-texture** — strip constructions that put rhetoric ahead of substance (§2), and the structural tells that make clean prose still read AI-generated: em-dash density, meta-narration scaffolding, compulsive both-sides balancing, marching cadence (§2e).
3. **No self-sabotage** — keep every fact and caveat, but never word the work down more than it deserves (§2b).
4. **No rhetorical-question scaffolding** — state the argument; don't keep prompting the reader with questions (§2c).
5. **Calm, measured register, no sensationalism** — descriptive titles, proportionate claims, no manufactured drama or "breakthrough" framing, plus the four-level anti-sensationalism pass that removes staged stakes and suspense at the sentence, paragraph, heading, and conclusion levels (§2d).
6. **Claims are checkable** — when a claim is empirical or factual, make it easy to verify (§3). This is evaluability, relaxed for the web.

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

## 2c. No rhetorical-question scaffolding (mandatory)

A blog post can use an occasional genuine question — especially in the opening, if it frames the problem naturally — but repeated question-answer structures are a strong LLM tell. They give prose an "AI explainer" rhythm: the writing keeps prompting the reader instead of stating the argument cleanly. Prefer declarative statements.

Rewrite on sight. Examples:

- Bad: "Residualisation is useful when the question is: what does this add on top of what I already know?" → Good: "Residualisation is useful for estimating incremental contribution."
- Bad: "The first residual asks: what part of price is not explained by square footage?" → Good: "The first residual is the part of price not explained by square footage."
- Bad: "Is this model layered on top of another model, or is it the whole prediction system?" → Good: "The decision depends on whether the model is layered on top of another model or whether it is the whole prediction system."
- Bad: "So if the question is 'how accurately can I predict house prices?', I would first try a joint model." → Good: "For house-price prediction, I would first try a joint model."

Guidance:

- Permit at most one or two genuine questions in a post, and only when they are doing real conceptual work.
- Do not use questions as section openings by default.
- Do not use repeated "the question is…" phrasing.
- Do not set up a paragraph by asking a question and immediately answering it, unless the question is genuinely useful.
- Prefer direct claims: "This estimates…", "This separates…", "This fails when…", "The decision depends on…".

## 2d. Calm, measured register & anti-sensationalism (mandatory for technical essays)

§2 strips the loudest hype; this rule governs the quieter sensationalism that creeps into technical writing — dramatic section titles, "breakthrough" framing, manufactured suspense, and inflated historical claims. The target voice is a technically competent practitioner explaining a mechanism carefully: grounded, precise, readable, modest about claims, clear about limitations. Not dull — clear and engaging — but never breathless, punchline-driven, suspenseful, or artificially contrarian. The aim is a measured technical essay, not a promotional explainer, a Twitter thread, or an AI-generated piece trying to manufacture excitement. This applies by default to all blog posts, and especially to Medium/TDS-style AI, ML, RL, and practitioner essays.

The first part of this rule sets the register; the second part is the operational anti-sensationalism pass that removes drama at four levels — sentence, paragraph, heading, conclusion (run it explicitly per §4 item 3e). The target is removing unnecessary drama, not removing voice: a good opening, a stated point of view, and readable transitions all stay. Calm confidence is not blandness — a specific, checkable claim said plainly reads stronger than a staged reveal, not weaker.

**Frame a method as solving a specific technical problem, not as a heroic leap.**
- Bad: "DDPG broke through the wall that stopped DQN from controlling robots." Better: "DDPG adapted DQN-style value learning to continuous-control settings by adding a deterministic actor that proposes the action directly."
- Bad: "TD3 and SAC fixed what DDPG got wrong." Better: "TD3 and SAC are easier to understand as later methods that retained DDPG's off-policy actor–critic structure while addressing specific sources of instability."

**Keep importance claims proportionate.** Distinguish, and do not let one imply another: importance at the time, current practical usefulness, influence on later methods, benchmark performance, reproducibility. Do not imply an influential method is still the best today unless that is explicitly true.
- Preferred: "DDPG matters less because it remains the default algorithm today, and more because it established a template that later methods refined."
- Avoid: "DDPG changed reinforcement learning forever."

**Use calm transitions.** Drop the rhetorical pivot — "But here's the problem.", "The real issue is…", "This is where everything breaks.", "And that is the key insight." Prefer plain connectives: "The difficulty is…", "This creates a practical problem…", "The next step is…", "This is where the actor becomes useful.", "The limitation is worth making explicit."

**Do not lean on question-structure** (reinforces §2c): a few genuine questions are fine, but avoid headings and openers like "So what does this mean?", "Why does this matter?", "What happens next?", "Is this enough?". Prefer declarative headings and topic sentences.

### The four-level anti-sensationalism pass

**Level 1 — sentence-level stakes phrases.** These manufacture suspense or inflate importance by *announcing* that something is interesting, hidden, surprising, key, or world-changing instead of just stating it. The announcement does no work the content can't do better. Rewrite each on sight as a plain descriptive claim (keep the explanation, drop the rhetorical force):

- "the real question is" → state the question, or just answer it
- "the key insight" / "the most interesting part" / "the surprising part" → drop the label; state the thing
- "the hidden problem" / "the hidden flaw" / "the catch" / "the twist" / "the part everyone misses" → "the limitation is", "one problem is", "an often underemphasised point"
- "what this really means" → "this means"
- "this changes everything" / "revolutionised" / "the breakthrough" → name the specific change ("helped establish…", "an important contribution because…")
- "the trick" / "the magic" / "the secret" → "the central move is", "the mechanism is"
- "where things get interesting" → just continue; let the reader decide what's interesting
- "why this matters" / "what happens next" → say why, or say what happens
- "the wall" → "the difficulty"; "closed that gap" → "addressed this problem"; "a resounding yes" → "yes, on the basis of influence"; "dead end" → "does not scale well"; "all it could do was…" → "was limited to…"
- "the future of X" / "X is dead" / "X is not enough" / "X finally works" → make the specific, checkable claim instead ("X handles Y but not Z", "X now does Y", "X is slower than Z on W")

Rule of thumb: never label a point as interesting, key, hidden, surprising, or game-changing. If it is any of those, the content shows it and the label is redundant; if it isn't, the label is a lie. Either way, cut it.

**Level 2 — paragraph-level suspense.** A paragraph must not be built as *setup → delayed point → punchline reveal*. State the factual point in the first sentence, then give the evidence, then add the caveat. Don't withhold the point to create a small reveal at the end.
- Bad (setup, delay, reveal): "A tutorial example is only useful if the model is good enough to take seriously. For that, I used GIFT-Eval."
- Better (point first): "The main benchmark here is GIFT-Eval."

The good shape is: point first, evidence next, caveat if needed. The bad shape reads as a magician's pause; on a technical blog it just slows the reader down.

**Level 3 — heading-level teasing.** A heading names what the section covers; it never teases a withheld payload or creates artificial suspense. If a reader can't tell from the heading what the section is about, it's teasing. Rewrite dramatic, journalistic, or punchy titles to descriptive ones:
- "The wall: argmax over a continuous action" → "Why continuous actions are difficult for value-based RL"
- "DDPG's trick" → "Using an actor to choose continuous actions"
- "The part retrospectives skip" → "Reproducibility and implementation sensitivity"
- "Why this changes everything" → "How the method works"
- "Where the field is moving" → "Hybrid routing and ensembles"
- "The benchmark gives the example some weight" → "GIFT-Eval benchmark setup"
- "What t0-alpha teaches us" → "Task-level strengths and weaknesses"
- "The hidden weakness" → "Leakage flags"
- "The frontier" → "Simulator-trained estimators"
- "The catch" → "Comparison with classical baselines"

**Level 4 — conclusion-level grandeur.** A conclusion ends on a concrete next step or a practical takeaway, not a grand claim, a dramatic future-framing, or an inflated field-level prediction. Replace the prophecy with the specific action you'd actually take next.
- Bad: "That is the practical frontier I would bet on." / "This is where the next weekend afternoon should go." / "The field is moving beyond architecture."
- Better: "The next experiment I would run is a non-oracle ensemble using validation data." / "For production use, I would compare the foundation model with a tuned classical baseline and a simple router."

A first-person "the next thing I'd run is X" is a stronger, more honest ending than a field-level forecast you can't check.

Read-aloud test: if a sentence or heading sounds suspenseful, contrarian for effect, or like a punchline; if a sentence announces that something is interesting rather than showing it; if a paragraph saves its point for a reveal; or if the closing line is a forecast rather than a next step — flatten it to the plain claim. Strong explanation stays; rhetorical force goes.

## 2e. Machine-texture tells (the ones greps miss — mandatory)

§2 catches word-level tells; this catches the structural ones that make clean-vocabulary prose still read machine-generated. A post can pass every banned-word grep and still feel like an AI essay because of cadence, scaffolding, density, and compulsive symmetry. None of these show up in a word search, so they have to be read for — and they are the single most common reason "it passed the checks but reads LLM".

- **Em-dash density, not just chains.** §2 bans the chain; this caps the rate. Working limit: at most one em-dash per ~150 words (roughly one every three or four paragraphs). A page peppered with individually-legal single-appositive em-dashes still reads generated. Convert the rest to full stops, commas, or parentheses. Rule of thumb: if a paragraph has two em-dashes, one is wrong.
- **No meta-narration scaffolding.** Cut the "let me tell you what I'm about to tell you" framing: "One thing worth saying plainly", "Here is the part that makes X worth reading", "The easiest way to picture it", "I'll be explicit about", "It's worth being precise about", "The thing that would…", "What this comes down to", "the thread that matters", "Two things to note". State the thing; don't announce that you're about to state it.
- **Don't compulsively balance.** "Two things hold at once", "it cuts both ways", "the honest reading sits between the two", "on the one hand… on the other" — reflexive even-handedness is a strong tell. Take the position the evidence supports and state it; add the counterpoint only where it genuinely changes the reading, not as automatic symmetry.
- **Break the tidy-summary cadence.** If every paragraph ends on a neat one-line moral ("…and that is the property I value", "…not a ranking I would defend"), the regularity itself reads generated. Let some paragraphs stop on a plain fact. Vary sentence length hard: a three-word sentence after a long one does more than another balanced clause.
- **Read for march.** If consecutive sentences share a shape (subject–verb–appositive, or "It does X. It does Y. It does Z."), rewrite for irregular rhythm. Human prose is lumpier and occasionally just blurts the point.

Read-aloud test: if a paragraph sounds like a well-organised essay machine that never simply says the thing, it needs roughening — fewer dashes, no throat-clearing scaffold, less symmetry, lumpier rhythm.

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
   c. Calmness pass (§2d): review every section title, caption, transition, and historical claim. Are the titles descriptive rather than dramatic? Are importance claims proportionate (importance-at-the-time vs usefulness-today vs influence)? Are limitations stated plainly? Is there any unnecessary "breakthrough", "wall", "trick", "hidden", "the part everyone misses", "changed everything", or "resounding yes" phrasing? Does the piece read as a measured technical essay rather than a promotional explainer? Replace sensational wording with the calmer alternative, keeping the explanation intact.
   d. Machine-texture pass (§2e): count the em-dashes (flag if more than roughly one per 150 words, or two in any paragraph) and thin them to full stops/commas; grep for the meta-narration scaffolds ("one thing worth", "the easiest way", "here is the part", "I'll be explicit", "what this comes down to", "the thing that") and cut them; check for compulsive both-sides framing ("two things at once", "cuts both ways", "sits between") and the tidy-summary-per-paragraph habit, and break both. This is the pass that stops a clean-vocabulary draft from still reading LLM; never skip it on the strength of (a).
   e. Anti-sensationalism pass (§2d, four-level pass), four levels: (1) Sentence — grep for the stakes phrases ("the real question", "key insight", "hidden", "the surprising part", "what this really means", "the most interesting part", "changes everything", "breakthrough", "the trick", "the catch", "the twist", "the magic", "the secret", "where things get interesting", "why this matters", "what happens next", "the future of", " is dead", "is not enough", "finally works") and rewrite each as a plain descriptive claim; the justified remaining count should be zero. (2) Paragraph — confirm no paragraph is built setup → delay → reveal; move any withheld point to the first sentence. (3) Heading — every heading describes its section, none teases a payload. (4) Conclusion — the closing lines end on a concrete next step or practical takeaway, not a grand claim, dramatic future-framing, or field-level prediction.
4. Self-sabotage sweep (§2b): scan for the imposter preamble, false modesty, self-deprecating verbs on neutral outcomes, and hedges on things you actually measured. Reframe each neutrally while keeping every fact and caveat. Re-read the opening and the closing specifically — those set and leave the impression.
5. Rhetorical question sweep (§2c): count every question mark and every phrase like "the question is", "asks whether", "what does X add", "what remains", "why does this matter". Keep only questions that a human author would naturally ask. Rewrite all scaffolding questions as declarative claims.
6. Title check: does it say what the post is about (and ideally what you found), without clickbait or empty aphorism?
7. Formatting check: bold and lists used for genuine emphasis/structure, not sprayed for energy. No bolded full sentences, no bulleted paragraphs.
8. Opinion/measurement check: every "I think"-class statement is marked as a view; every measurement has its evidence. Neither is disguised as the other.
9. Spelling consistent with the chosen variant throughout — no mixing.

Report the outcome of this checklist to the user explicitly — pass/fail per item — before calling the post finished.

## One-line summary

Write like a clear person talking — first person, concrete, one claim per sentence, intuition before formalism — strip every construction that puts rhetoric ahead of substance, keep the register calm and measured (descriptive titles, proportionate claims, no manufactured drama), word your work neither above nor below what it deserves, and make every claim that matters checkable in under a minute.

## Relationship to academic-prose

This skill governs blog posts and public web prose. For academic papers (.tex files, journal/conference submissions, abstracts, rebuttals), defer to the **academic-prose** skill, which is stricter on machinery (claims boxes, one-protocol-per-table, abstract word limits, signposting) and uses the collective "we". The two share a spine — no hype, no self-sabotage, checkable claims — but a blog relaxes the formal scaffolding and speaks in the first person. If a post is really a paper draft in disguise, use academic-prose instead. If another general writing or style skill conflicts with this one on a blog post, follow this skill and note the conflict.
