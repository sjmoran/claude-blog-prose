---
name: blog-prose
description: Rules for writing, revising, or reviewing blog posts and other public web prose — devlogs, technical write-ups, opinion pieces, tutorials, announcements, and READMEs-as-posts. Use whenever the task involves a blog post, a Markdown post, a personal-site article, or whenever the user asks to write, edit, polish, restructure, or check a post, even if they only say "write a post about X", "tighten this intro", or "make this readable". Also use before declaring any post finished, to run the pre-publish self-check. For academic papers (.tex, journal/conference submissions), defer to the academic-prose skill instead.
---

# Blog Prose

This skill ports the academic-prose voice to the blog. It keeps the parts that travel — the refusal to put rhetoric ahead of substance, and the habit of making claims checkable — and relaxes the academic machinery (no abstract word limits, no claims box, no "the remainder of this post is structured as follows", no Protocol paragraphs). A blog post should read like a clear person talking, not like a paper with the formatting filed off.

Seven rule sets, applied in this order whenever blog prose is written or edited:
1. **Voice** — plain, first-person, conversational but precise (§1).
2. **Structure for understanding** — sequence the piece so depth arrives in an order a first-time reader can absorb: intuition before implementation, terminology after the idea it names, one concept per paragraph, each section answering the question the last one raised (§1b). This is the primary lever on reader cognitive load, and it preserves technical depth rather than trimming it — the depth simply arrives later in the arc.
3. **No hype, no machine-texture** — strip constructions that put rhetoric ahead of substance (§2), and the structural tells that make clean prose still read AI-generated: em-dash density, meta-narration scaffolding, compulsive both-sides balancing, marching cadence (§2e).
4. **No self-sabotage** — keep every fact and caveat, but never word the work down more than it deserves (§2b).
5. **No rhetorical-question scaffolding** — state the argument; don't keep prompting the reader with questions (§2c). Note the deliberate seam with §1b: the reader's *implicit* next question drives the structure, but you answer it in declarative prose, not by posing the question on the page.
6. **Calm, measured register, no sensationalism** — descriptive titles, proportionate claims, no manufactured drama or "breakthrough" framing, plus the four-level anti-sensationalism pass that removes staged stakes and suspense at the sentence, paragraph, heading, and conclusion levels (§2d).
7. **Claims are checkable** — when a claim is empirical or factual, make it easy to verify (§3). This is evaluability, relaxed for the web.

Plus an additive **style layer** (§1c, concrete-explainer techniques for technical results), which yields to every rule above wherever they conflict.

Plus two **mode layers**, each applied on top of the seven rule sets for a specific kind of post:
8. **Builder's-map mode** — for posts that map a confusing technical area for other builders (how-X-systems-work explainers, which-tool-should-I-use landscapes, architecture and agentic-system walkthroughs), adopt the guided-design-walkthrough structure and framing in §4. It is the landscape-and-architecture specialisation of the §1b progression: the same intuition-first, one-concept-at-a-time spine, plus the compare-on-axes and operational-realism framing. It composes with §1–§3 and inherits every ban; it does not relax them. Skip it for a plain devlog or single-result post — those stay on §1–§3 alone.
9. **Research-synthesis mode** — for posts that survey or reconstruct how an idea or a research area evolved (a technique's history, a literature synthesis, a "what changed and why" piece), adopt the investigation arc in §4b: build an evidence map and a thesis before drafting, and structure the piece as history + mechanism + interpretation rather than a paper-by-paper survey. It composes with §1–§3 and inherits every ban; it does not relax them, and it is a *structural and reasoning* method, not a licence to imitate any particular writer's sentence-level style. Skip it for a devlog, a single-result post, or a landscape/tool-comparison post (use §4 for the last of those).

Then run the **pre-publish self-check** (§5) before calling a post done. If an instruction in the conversation conflicts with a rule here, flag the conflict rather than silently overriding.

Rationale (one line): a reader decides in the first paragraph whether to keep reading and whether to trust you; plain prose earns the first, checkable claims earn the second, and structure that adds depth in an order the reader can absorb earns the read all the way to the end.

## 1. Voice — plain, first-person, precise

Write the way a clear, honest person explains something they actually did or thought. Plain, direct, economical — but a blog is allowed warmth, narrative, and a point of view that a paper is not.

- **Person:** first-person singular — "I built", "I found that", "I was wrong about". Address the reader as "you" when it helps ("you might expect X; it turns out Y"). Use "we" only for genuinely shared work or when walking the reader through a derivation together.
- **Openings:** start with the concrete thing — a problem you hit, a result that surprised you, a question worth an afternoon. No throat-clearing ("In today's fast-moving world…"), no abstract-style "This post studies…", and no slogan or aphorism (see §2). A short scene or a blunt statement of the result both work.
- **Contractions and rhythm:** contractions are fine ("it's", "didn't"). Vary sentence length for rhythm — a short sentence after two long ones lands. But still aim for one main claim per sentence; rhythm is not an excuse for a clause pile-up.
- **Intuition first, formalism optional:** lead with the plain-language reading; bring in notation, equations, or code only when they earn their place, and gloss them immediately. A blog reader will forgive you for skipping the proof; they won't forgive an unglossed symbol. This is the sentence-level face of §1b's structural rule — intuition before implementation, the term after the idea it names.
- **Show the thing:** prefer a concrete example, a code block, a chart, or a real number over an abstract description of it. "It dropped p99 from 800ms to 90ms" beats "it substantially improved latency".
- **Structure by scent, not by signposting:** use descriptive headings so a scanner can navigate, but drop the academic "The remainder of this post is structured as follows" and "In this section we…". Let the headings and the first sentence under each do that work.
- **Formatting for the screen:** bold for genuine emphasis or scannability is allowed in moderation (a paper bans this; a blog reader skims). Bullet lists for genuinely list-shaped content. Don't bold whole sentences, don't bullet prose that wants to be a paragraph, and don't let formatting substitute for a clear sentence.
- **Opinion is allowed, and marked as opinion:** a blog can argue and take sides. Say "I think" / "my guess is" / "I'd bet" so the reader can tell a judgement from a measurement. Don't dress an opinion as a finding, and don't dress a finding as a mere opinion (§2b).
- **Endings:** close on what you'd do next, what you're still unsure about, or what the reader should take away — not a triumphant restatement and not a limp "anyway, that's it". One honest forward-looking sentence beats a summary paragraph.
- **Spelling:** pick one variant (British or American) and hold it with zero mixing. Default to British unless the venue says otherwise.

Do not: open with a dictionary definition or a rhetorical question stack; pad with qualifiers; chain subordinate clauses; write a SEO-keyword-stuffed paragraph; adopt LinkedIn-influencer or press-release register.

## 1b. Structure for understanding — lower the reader's load, keep the depth (mandatory)

§1 governs how a sentence sounds; this governs how the whole piece is sequenced. The objective is to reduce the reader's cognitive load while preserving technical depth — not to make the material shallower. The move is to introduce depth in an order a first-time reader can absorb: one concept at a time, intuition before machinery, terminology after the idea it names. Technical accuracy and architectural depth stay; what changes is the order and pacing in which they arrive. The paragraph-level rules below apply to every post. The full teaching progression applies to explanatory or tutorial articles and scales down for a short devlog, opinion piece, or announcement (those keep the paragraph-level rules but not the seven-beat arc). For a landscape or architecture post, §4 is the specialised form of this pillar.

- **Lead with intuition, name the term afterward.** Give the plain-language reading and a mental model the reader can hold before you introduce notation, an equation, code, or a named concept. Introduce a term only once the reader understands the thing it labels — the word is a handle for an idea they now have, not a prerequisite for it. (§1's intuition-first bullet stated in full; §4's "plain entry before jargon" is this same rule for landscape posts.)

- **Separate what a thing does from how it does it.** Describe observable behaviour before, and separately from, internal implementation. A reader who only needs to know *what* a component does should be able to stop before the internals; a reader who needs the mechanism reads on. Blurring the two forces everyone to load the implementation just to understand the behaviour. Behaviour is usually the intuition; implementation is the machinery that follows it.

- **Follow the teaching progression whenever the piece is explaining something.** For an article whose job is to teach an idea, the default arc through each major concept is:

  **concept → mental model → concrete example → why it matters → implementation → nuances → research caveats.**

  Start with the bare concept in plain words; give a mental model or analogy the reader can reason with; ground it in one concrete example — a real number, a small code block, a worked case — before generalising; say why it matters (what it lets you do, or what breaks without it) as a plain statement, never a "why does this matter?" heading (§2d); *then* show the implementation; then the nuances and edge cases; then the honest research caveats and limits. Depth lives in the later beats, which is how the arc keeps early paragraphs light without making the piece shallow. Not every idea needs all seven beats or in lockstep — but a jump straight from concept to implementation has almost certainly skipped the intuition the reader needed.

- **Layer complexity; don't step from beginner to expert in one move.** Introduce one new idea at a time and let it settle before the next depends on it. If a paragraph assumes something you haven't built yet, move it or build the missing step first. A reader should never have to hold two unexplained things at once.

- **Summarise before you add complexity.** At each real threshold — before a section that leans on everything so far — consolidate the idea in a sentence or two, then push forward. This is where deliberate repetition earns its keep. It is not the tidy-summary-per-paragraph tic §2e bans: a recap belongs at a genuine complexity step and must consolidate, not decorate.

- **Repeat a concept only when the repetition adds understanding.** Restate an important idea when the restatement consolidates it, reframes it, or connects it to something new — each repeat teaching a little more than the last. A recap that only re-says the words is the §2e cadence tell; cut it.

- **Each paragraph holds one concept, and every paragraph earns its place.** Keep a paragraph to a single idea, typically two to five sentences. Every paragraph must do one of five jobs: introduce, explain, contrast, motivate, or summarise; if a paragraph does none of these, cut it.
  - **Sentence count is a flag, not a verdict.** A long paragraph is a prompt to check, not an order to split. The test is what the sentences are doing. Split when the paragraph bundles separable concepts a reader would navigate between — a definition with a vendor list stuck on the end, or a paragraph that is really a list of findings. Leave it when the sentences are one argument building to a single claim, each one evidence for the same point; breaking that paragraph severs the thread into fragments and weakens the claim.
  - **Don't over-split.** Chopping every long paragraph into one-idea slivers manufactures exactly the marching, one-thought-per-paragraph cadence §2e bans — that tell reads as machine-generated as strongly as a wall of text does. Length is typical, not a quota: §1 and §2e want varied, lumpy rhythm, a one-line paragraph that lands a point is fine, and a coherent seven-sentence argument that earns its length stays.

- **Let the reader's next question pull the piece forward — but answer it in statements.** The strongest technical writing reads as if each section answers the question the previous one naturally raised, so the reader always knows why they're reading on. Build the outline that way: every section should leave a specific question that the next one answers. But realise that momentum in *declarative* prose. Open a section by stating the answer or naming the topic, not by posing "So what happens next?". This is the seam with §2c and §2d: the question-driven *structure* is the goal; the question-driven *surface* is the banned LLM tell. The §2c budget still holds — at most one or two genuine questions in a whole post, only where a human author would really pause to ask one.
  - Bad (question on the page): "So how does the model avoid decoding the whole row? The answer is byte offsets." → Good (implicit question, declarative answer): "The model never decodes the whole row. It reads a small header of byte offsets and jumps straight to the three fields it needs."

- **Orient the reader with transitions that mark a real move.** A short connective that says where the reader is — "Next," "We'll return to this," "In other words," "Having established X, we can now Y," a one-line recap before a turn — is good writing; use them continuously. Keep each honest: "In other words" must precede a genuine restatement that adds clarity, and a transition must introduce a real conceptual step. The §2e ban is on scaffolding that *announces explaining instead of explaining* ("Here's the part that makes this worth reading"). Marking a step is good; narrating that you're about to teach is cut. The §2e em-dash cap still applies to these connectives. (Same reconciliation §4 makes for its guide phrases.)

- **Address a misconception the moment it becomes relevant.** When a natural but wrong reading of what you just said would take root, name it and correct it right there — not in a later "common mistakes" appendix, and not before the reader knows enough to hold the misconception. State it plainly ("It's tempting to read X as Y; it isn't, because…"), fix it, move on.

- **Headings tell the story on their own.** A reader skimming only the headings should get a coherent, correct outline of the argument. Each heading names what its section establishes (declarative), reads as the next step after the one before, and never teases a withheld payload (§2d Level 3) or poses a question (§2c). If the headings alone don't narrate the piece, the structure is wrong, not just the wording.

- **Figures support the narrative; they don't replace it.** A visual is evidence for a point the prose is already making, not a substitute for making it. Set up in words what the figure shows and what to look for; the reader should grasp the point from the prose and see it confirmed in the figure. Keep visuals strong — a diagram, an axis chart, or an architecture sketch that carries real structure is worth building — but never let one carry a point the text never states. (This generalises §4's visuals rule to every post and pairs with §3: a figure is one of the checkable artifacts.)

- **Prefer precise, simple English.** Say it in the plainest words that are still exact. Simpler wording almost always reads as *more* competent; academic hedging and corporate register (§2's hype vocabulary) read as less. Cut adjectives that add heat but no information — the credibility comes from the specific, checkable fact, so let it do the work an intensifier was reaching for. (This is §2 and §2d restated as a positive.)

Read-aloud test: read only the headings — do they narrate the piece? Then read it as a first-time reader — does each section answer the question the last one raised, does every term arrive after its idea, does any paragraph make you hold two unexplained things at once, and does every paragraph introduce, explain, contrast, motivate, or summarise? If a section jumps from concept to implementation with no intuition between, or a heading poses a question or teases a payload, restructure.

## 1c. Concrete-explainer layer — rigorous but readable (additive style layer)

An extra layer on top of §1 and §1b for any post that explains a technical, mathematical, or scientific result. It adds techniques; it does not replace the voice. The target is rigorous technical writing that stays concrete, sceptical, and readable: confident but willing to say "we don't know", conversational without chatty, concise without terse. Complexity belongs in the research process, clarity in the post. These are techniques to absorb into this skill's voice, not a style to imitate: do not copy any particular writer's phrases, sentence shapes, or jokes. **Where a rule here conflicts with §1–§2e, the earlier rule wins** (specific reconciliations are marked below).

- **Concrete situation before abstraction.** Find the simplest real scenario that preserves the structure of the idea and open with it ("say you run a city that wants every street watched from at least one end") before the graph-theoretic term. The analogy has to correspond to the idea; never trade correctness for accessibility, and drop the analogy where it distorts. Prefer a memorable human scenario over generic nodes A, B, C (matching as a dating app, covering as street surveillance, sampling as an engine burning expensive fuel). After the intuition, give the precise concept.
- **Intelligent reader, not specialist.** Remove prerequisites, not difficulty. Give the one or two pieces of background needed to see why a result matters, then move on. No textbook definitions unless the argument needs them. Keep technical terms that earn their place: name the concept, explain it in one clean sentence, say why it matters, continue. The reader should finish knowing slightly more vocabulary than they started with.
- **Answer "so what" for each major result, in statements.** Say what was known before, what changed, why experts care, whether it matters outside the field, and what limits it. Keep theoretical importance, practical usefulness, and sociological significance apart; a result can be profound and practically useless, and the post should say so. (Declarative only; §2c and §2d still ban the posed question and the "why this matters" heading.)
- **Escalating specificity, with the inconvenient fact.** The core pattern is impressive claim → intuitive explanation → inconvenient fact. Ordinary-language claim, then an example, then the technical result, then the caveat. "The algorithm is polynomial time" means something specific; then state that the exponent is 150,020, then translate that into a physical quantity. Use numbers to make scale tangible, and only with comparisons that are mathematically defensible (seconds, lifetimes, age of the universe, atoms in the observable universe, storage, money).
- **Caveats are part of the story.** Don't bury a limitation at the end of a paragraph; it is often the most interesting fact, so give it its own sentence at the point it applies. Natural forms: "Except that…", "In theory, yes. In practice…", "That sounds impressive until…", "Technically speaking…", "Which is true, but not especially helpful." Use sparingly and never as a repeated template. **Reconciliation with §2d:** "the catch", "the twist", and "the hidden problem" stay banned as labels; state the limitation plainly instead.
- **Dry humour from the facts.** Understatement where reality meets a theoretical claim: absurd bounds, correct-but-useless results, academic terminology against ordinary life. Deadpan over punchline, no inserted jokes, no joke that isn't carried by a fact. **Reconciliation with §2e:** at most a few such moments per post, otherwise it becomes the staccato-defensive register.
- **Vary length on purpose, within §2e.** A very short sentence can land a conclusion after dense material. **Reconciliation:** this is the occasional rhythm break §2e allows, not a habit; fragments like "Phew." or "Not yet." are rare, and never several in a row.
- **Headings that carry a claim.** Prefer a heading that states the section's finding ("Perfect radar exists, but nobody can construct it") over a topic label ("Applications to radar"). **Reconciliation with §2c and §2d Level 3:** the claim must be a plain descriptive statement that gives the point away, never a question, tease, or withheld payload, and never a punchline.
- **Footnotes as a second voice, where the format has them.** Use them for technical qualifications, history, method detail, exceptions, and asides that would interrupt the main line. They must contain useful information, may be a little more technical or wry, and are never there only to show off. If the format has no footnotes, put the material in a short parenthetical or drop it.
- **Epistemic discipline on impressive claims.** Check whether the theorem establishes what is claimed, whether the algorithm is practical, whether an implementation or benchmark exists, whether "polynomial" hides an enormous exponent, whether an existence proof gives a construction, whether an approximation recovers the underlying solution, whether the assumptions do the work, and whether the impact is real or a plausible future connection. Where evidence is weak, narrow the claim instead of adding confidence (§3, §4b).
- **Restrained author.** First person is for methodology, uncertainty, and judgement ("I wanted to know whether this matters in practice"), not for centring the author. Curious, sceptical, technically literate; "my read is" over "here is my definitive assessment".
- **Widen the lens at the end, only if earned.** Move from specific result to pattern across results to a broader consequence, which may concern research practice, institutions, incentives, or how people relate to the technology rather than the obvious application. Don't manufacture profundity; if the broader implication is uncertain, say so. **Reconciliation with §2d Level 4:** the widened point is stated as a modest observation, not a field-level forecast, and a concrete next step is still a valid ending.

## 1d. Intellectual-stakes layer — evidence, belief-updating, lived expertise (additive style layer)

An extra layer on top of §1–§1c for posts that report a result, a development, or a change in what the author believes. §1c supplies the explanatory machinery; this layer supplies the stakes: what the old picture was, what evidence forces it to change, and what the author now thinks. These are techniques to absorb into this skill's voice, not a persona to imitate: do not copy any particular writer's wording, cadence, jokes, or recurring expressions. **Where a rule here conflicts with §1–§2e, the earlier rule wins** (reconciliations marked below).

- **Significance by contrast, not adjectives.** Establish the old world first: what experts believed, for how long, how much work went into it, what would have counted as extraordinary progress. Then show the evidence that breaks it. "For twenty years this was the barrier everyone worked around. Yesterday it disappeared" beats "an incredibly significant breakthrough". Organising question: what fact about the world is different today from what I reasonably believed yesterday? Build the post around that delta. **Reconciliation with §2d:** the contrast must be factual and checkable; "breakthrough", "changes everything" and the like stay banned.
- **Expert reaction as evidence.** Use reactions from people who worked on the problem to answer: did experts expect this, is the technique new, is the proof comprehensible, does it contradict the field's intuition, are experts changing their minds. A sceptic conceding is stronger than an advocate agreeing. Say why the person's reaction carries weight.
- **Show belief updating.** Allow genuine changes of mind: "I initially assumed X. After looking at Y, I no longer think that." "The first version of this post overstated this point." Never manufacture uncertainty for effect; when evidence changes, update visibly. A correction is evidence of seriousness, not embarrassment (consistent with §2b).
- **Separate observation, inference, prediction.** Make clear which a claim is, and do not slide from one to the next. A dramatic observation does not justify a dramatic prediction; an uncertain implication does not justify downplaying the observation.
- **Keep the mess when it matters.** Do not make events look inevitable. "We don't yet know", "three results have already failed", "experts are still working through the proof" are fine. Be decisive about what happened and uncertain about what it means.
- **Discovery is not understanding.** For AI-assisted science especially, treat as separate: producing an answer, verifying it, understanding why it is true, explaining it, connecting it to existing knowledge, and what it enables next. Do not equate a verified result with understanding.
- **Move between three scales.** Micro (the theorem, benchmark, experiment), meso (what it changes for the field or industry), macro (science, work, institutions). Do not stay macro for long; the micro level earns the right to discuss the macro.
- **Second-order consequences.** After the immediate result, say what changes because people now know it: effort redirected, benchmarks obsolete, expertise revalued, verification or explanation becoming the bottleneck. This is often more interesting than the result.
- **Personal experience only when it carries information.** An anecdote earns its place by supplying evidence a press release lacks: someone close to the problem trying to follow a proof, the author's earlier prediction being falsified, researchers changing workflow. Observed adaptation beats generic futurism; one small story can carry a thesis. No autobiography for warmth. Show experts as people thinking, getting confused, changing their minds, not as quotations that certify claims.
- **Strongest objection.** For a consequential claim, state the best counterargument fairly and say what evidence would distinguish the readings. Dispatch weak objections quickly; do not invent foolish opponents. **Reconciliation with §2c/§2e:** state it declaratively, and do not add symmetry the evidence does not support.
- **Earned strong conclusions.** Do not sound equally cautious regardless of evidence. If something extraordinary happened, say so, after evidence → context → comparison. One plain declarative after paragraphs of evidence has more force than constant superlatives. The reader should think "I see why the author thinks so", not "the author keeps telling me". **Reconciliation with §2d:** escalation is by accumulated evidence only (fact → context → surprising implication → human reaction → broader consequence); no suspense paragraph shape, no grand forecast.
- **Analogies for structural change.** Use analogies to capture discontinuity, changed incentives, obsolete expertise, new access, or answer-versus-understanding, with several points of structural correspondence. Return to reality once the analogy has worked; do not extend it until it breaks.
- **Lists only when accumulation is the point.** Keep items compact with just enough context, stop when the point lands, then interpret what the accumulation means. Never leave a run of unexplained technical names.
- **Humour releases pressure.** One line of juxtaposition, understatement, or ordinary life against grand technical material can reset the reader. Sparse, carried by a fact (§1c limits apply).
- **Memorable compression, rarely.** After an argument is carefully made, one short sentence may compress it ("The proof is finished. The understanding isn't."). **Reconciliation with §2/§2e:** at most one or two per post, never a tidy aphorism closing each section, and never an empty-profound title.
- **Texture.** Parenthetical qualifications, short asides, corrections, specific technical detail, and carefully chosen first-person observations are welcome; the post should read as a person thinking clearly. Texture is not rambling. Rhetorical questions stay governed by §2c.
- **Endings.** A genuine tension may be left unresolved rather than forced into a verdict, leaving the reader with a sharper model of the problem. **Reconciliation with §2d Level 4 and §2e:** the ending still prefers a concrete next step or practical takeaway where one exists, and the unresolved tension is stated once, plainly, not as a reflexive "two things hold at once" pair.

Target combination: concrete explanation and practical scepticism (§1c), evidence-first reasoning, analogies that map, willingness to say "this evidence changed what I believe", dry humour, technical specificity, and human-scale anecdote, in the author's own voice, strengthened rather than replaced.

## 2. No hype (mandatory — kept strict from the paper rules)

Banned constructions — rewrite on sight, in drafts and in any text being edited. These are the same tells that flag a paper as overwritten, and they flag a blog post as AI slop or marketing even faster.

- **Em-dash chains.** Em-dashes are fine on a blog in moderation — one clean appositive like this. The ban is on the *chain*: never nest a clause inside an em-dash pair, and don't use three em-dashes in a paragraph to stage drama. If a sentence leans on em-dashes for momentum, rewrite it flat.
- **Rhetorical inversion.** "A good abstraction, it turns out, needs no documentation" → "It turns out a good abstraction needs no documentation." Subject, verb, object.
- **The pivot.** "It's not a cache — it's a contract", "not because it's fast but because it's simple", "the speed isn't the point; the point is X". State what is true; don't stage a reversal for effect.
- **Triadic drama.** "It scales. It composes. It just works." — three parallel punchy fragments read as a keynote slide. Use an ordinary sentence or a plain list.
- **Clickbait and aphoristic titles.** No "The X Is the Y" empty-profound titles, no curiosity-gap headers ("You won't believe what happened next", "I tried X so you don't have to" when you didn't), no "Here's why X changes everything". A title should say what the post is about and, ideally, what you found. Personality in a title is fine; a withheld payload is not.
- **Intensifier adverbs.** Crucially, importantly, notably, remarkably, surprisingly, incredibly, massively — delete. If a thing is surprising, show why and let the reader be surprised.
- **Hype vocabulary.** "game-changer", "revolutionary", "blazing-fast", "seamless", "effortless", "powerful", "robust", "leverage", "unlock", "supercharge", "delve", "in the realm of", "it's worth noting that". Cut or replace with the concrete fact.
- **Corporate-polish and landscape-post clichés.** "this changes everything", "the future of AI" / "the future of X", "the ultimate framework", "a comprehensive deep dive", "unlocks unprecedented capabilities", "Cambrian explosion", "production-grade paradigm". These are the register a tool-comparison or system-design post drifts into most; rewrite each to the specific, checkable claim ("handles Y but not Z", "faster to start than X, harder to debug than W").
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

**Reconciliation with §1b.** §1b wants each section to answer the question the previous one naturally raised — that is the reader's *implicit* question driving the structure, and it is encouraged. This rule bans the *surface* form: posing that question on the page and then answering it. Keep the question-driven outline; write the answers as declarative topic sentences. The two rules point the same way — a piece whose structure is genuinely question-driven rarely needs to print the questions at all.

## 2d. Calm, measured register & anti-sensationalism (mandatory for technical essays)

§2 strips the loudest hype; this rule governs the quieter sensationalism that creeps into technical writing — dramatic section titles, "breakthrough" framing, manufactured suspense, and inflated historical claims. The target voice is a technically competent practitioner explaining a mechanism carefully: grounded, precise, readable, modest about claims, clear about limitations. Not dull — clear and engaging — but never breathless, punchline-driven, suspenseful, or artificially contrarian. The aim is a measured technical essay, not a promotional explainer, a Twitter thread, or an AI-generated piece trying to manufacture excitement. This applies by default to all blog posts, and especially to Medium/TDS-style AI, ML, RL, and practitioner essays.

The first part of this rule sets the register; the second part is the operational anti-sensationalism pass that removes drama at four levels — sentence, paragraph, heading, conclusion (run it explicitly per §5 item 3e). The target is removing unnecessary drama, not removing voice: a good opening, a stated point of view, and readable transitions all stay. Calm confidence is not blandness — a specific, checkable claim said plainly reads stronger than a staged reveal, not weaker.

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
- **No staccato-terse-defensive register.** A distinctive current-model tell: wall-to-wall clipped sentences and fragments ("Which is the point.", "That's fine.", "Not ideal."), terseness as the default register rather than a rhythm break, and a defensive crouch — pre-empting objections nobody raised ("To be clear…", "This isn't to say…", "None of this means…"). The prose reads like it's bracing for criticism instead of explaining. The occasional short sentence that breaks a march (above) is good; uniform clippedness is the opposite defect. Write full, relaxed sentences by default, and answer an objection only where a real reader would raise it — once, plainly.

Read-aloud test: if a paragraph sounds like a well-organised essay machine that never simply says the thing, it needs roughening — fewer dashes, no throat-clearing scaffold, less symmetry, lumpier rhythm.

## 3. Claims are checkable (mandatory — evaluability, relaxed for the web)

A blog reader who hits an unsupported claim does one of two things: takes it on faith, or stops trusting you. Make the claim checkable instead. This is the paper's evaluability rule with the formal machinery removed — no numbered claims box, no one-protocol-per-table, no abstract word count. The spirit stays: a reader should be able to verify any claim that matters in well under a minute.

- **Empirical claims show their evidence inline or one click away.** A performance number gets the benchmark, the code, or a chart; a "X is faster than Y" gets the conditions it was measured under, in the same sentence or the next ("on a 10k-row table, on my M2; your mileage will vary"). If you can't back it, soften it to an opinion or cut it.
- **Link your sources.** A factual claim about someone else's work, a library, a paper, or an event links to the thing. A quote links to where it's from. No "studies show" without the study.
- **Show the real artifact.** Prefer the actual code, the actual config, the actual output over a paraphrase. If the post is about a repo, link the repo. If a snippet is simplified for readability, say so.
- **Separate what you measured from what you believe.** Measurements get evidence (§3); beliefs get "I think" (§1). Don't blur the two — the most damaging blog move is presenting a guess with the confidence of a result.
- **One honest number, not a best-case number.** If you cherry-picked the run that looked best, say so or don't report it. Report the number a skeptical reader would get, not the demo number.
- **Reproducibility, lightweight.** When practical, give the reader enough to reproduce: the command, the versions, the dataset, the gist link. A post that can be re-run is worth ten that can't.

## 4. Builder's-map mode — the guided design walkthrough (mandatory for landscape & architecture posts)

This is a mode layer, not a separate voice. It composes with §1–§3 and inherits every ban above — it changes the *structure and framing* of a post, not the register. Use it for posts that map a confusing technical area for other builders: how-a-class-of-systems-works explainers, which-tool/framework/model-should-I-use landscapes, architecture explainers, and agentic-AI or LLM-system design walkthroughs. Do not use it for a plain devlog or single-result post; those stay on §1–§3.

The target is the voice of a practical builder walking another builder through the space: approachable, lightly conversational, and useful — but not chatty, promotional, or over-polished. It should read as a guided design walkthrough, not an academic survey, a vendor whitepaper, a thought-leadership essay, or a hype post.

The default arc, applied to the post as a whole and often to each section: **plain entry → naive path → failure modes → trade-offs → design families → operational realism → modest conclusion.** This is the §1b teaching progression (concept → mental model → concrete example → why it matters → implementation → nuances → research caveats) specialised for a design-space post: the naive path is the concrete example, the failure modes and trade-offs are the why-it-matters and nuances, and the modest conclusion is the research-caveat beat. Everything §1b says about intuition-first, one-concept paragraphs, and question-driven-but-declarative momentum holds here too.

### Plain entry before jargon
- This is §1b's rule (lead with intuition, name the term after) applied to a landscape post: give the plain-language version of the problem and a simple mental model first, and name the jargon only once the reader understands the underlying idea.
- Bad: "Stateless inference requires externalised persistence layers." Better: "LLMs don't remember anything between calls. That's what people mean when they say they're stateless."

### Progressive discovery as the backbone
- Start with the naive solution a competent person would reach for first. Say why it's reasonable and where it works (usually: at small scale), then show where it breaks. Introduce each more advanced architecture only after the previous one has failed naturally.
- The rhythm: naive idea → why it seems reasonable → failure mode → better architecture → new trade-off → practical recommendation.
- Don't present the sophisticated answer cold. Earn it with the failure that motivates it.

### Failure modes are central
- Explain any technology by what it solves, what it breaks, and what new trade-off it introduces. Never present a framework, model, architecture, or tool as simply "better".
- For every option, say where it helps, where it becomes painful, and what happens as usage, complexity, or scale grows.

### Motivate requirements from concrete scenarios
- Move example → required capability → architectural implication. Lead with a real user question, product scenario, or implementation example, then derive the requirement from it.
- Bad: "The system needs temporal reasoning." Better: show the query — "When did I say that?" or "Did this preference change?" — then explain why temporal reasoning follows.

### Compare on axes, not rankings
- Avoid "best tool" framing. Compare along dimensions. Useful axes include: high vs low abstraction; plug-and-play vs custom control; fast to start vs easy to debug; high agency vs tightly controlled workflow; cloud vs self-hosted; vector-first vs graph-first; beginner-friendly vs engineering-heavy; prototype-friendly vs production-ready; popular/community-backed vs specialised/transparent; built-in features vs manual wiring.
- First state what all the options have in common. Separate table-stakes capabilities from the true differentiators.
- Group options into design families and explain each family's design philosophy before naming individual examples. Don't treat every option as unrelated.

### Abstraction is a trade-off, not a virtue
- High abstraction speeds prototyping but can hide failure modes and make debugging harder. Low abstraction improves transparency, validation, and control but raises the implementation burden. Keep that tension visible; don't praise abstraction as an unqualified good.

### Make the agency assumption explicit (agentic AI / LLM systems)
- Some systems assume the model should decide the next step; others assume the engineer should constrain the workflow tightly. State which assumption a system makes, and frame it as a reliability philosophy, not just an implementation detail.

### Keep operational reality visible
- Where relevant, cover cost, latency, scale, security, observability, database growth, maintainability, debugging, evaluation, developer experience, and migration paths. A technical post does not stop at the architecture diagram or the model description. This is §3 applied to the boring-but-decisive parts: give the real number where you have it, and name the cost even when you don't.

### Vendors, frameworks, papers, and tools are examples of the design space
- Use each as a representative of a design choice: what it stands for, what user or use case it fits, and where it is likely to struggle. Not a shallow list.
- Popularity is a signal, not proof of fitness. GitHub stars, mentions, and adoption tell you something real; they do not tell you a tool fits your case. Don't equate popular with suitable. (Reinforces §3: back a "widely used" claim, and don't let it stand in for "right for you".)

### Voice: modest and practical, mildly opinionated
- Be mildly opinionated, not dogmatic. It's fine to say something feels easier, harder, cleaner, more brittle, or more painful to debug — frame these as practical observations, not universal truths. (This is §1's mark-opinion-as-opinion rule and §2b's no-self-sabotage rule doing double duty.)
- Natural guide phrases are allowed here as light connective tissue, in moderation: "Let's walk through…", "Your first thought may be…", "The issue is…", "This works at small scale, but…", "This gets you further, but…", "That said…", "To be fair…", "From what I've seen…", "You'll need to test this yourself."
- **Reconciliation with §2c and §2e:** these phrases are permitted because they mark genuine walkthrough steps, not because the scaffolding bans are lifted. Keep them sparse (don't open three paragraphs in a row with one), never use them to announce that you're about to explain instead of explaining, and don't let "your first thought may be…" grow into a rhetorical-question stack (§2c). The §2e em-dash cap and meta-narration ban still apply. If a guide phrase isn't introducing a real step in the walk, cut it.

### Contrast, uncertainty, short paragraphs
- Short, single-concept paragraphs are the §1b default; here each does one of these jobs: introduce the idea, give the example, name the failure mode, state the trade-off, or draw the practical implication.
- Explain through contrast pairs: simple vs complex, fast-to-start vs hard-to-debug, abstraction vs control, vector-first vs graph-first, cloud vs self-hosted, high-agency vs tight-workflow, benchmark result vs production reliability.
- Keep uncertainty visible: "seems to", "may", "likely", "from what I've seen", "I haven't tested this thoroughly", "you'll need to validate this yourself". Used honestly this builds trust; it does not conflict with §2b, whose ban is on wording your work *down*, not on stating genuine limits.

### End with modest confidence
- Close by leaving the reader a useful map, not a verdict. Say what's still uncertain, what you didn't test, and what they should validate in their own environment. This is §2d Level 4 (next step over forecast) applied to a landscape post: the honest ending is "here's the map and where its edges are", not "here's the winner".

### Visuals that map the space
- When a visual helps, prefer ones that clarify the map: comparison matrices, axis charts, architecture sketches, feature maps, workflow diagrams, cost tables, simple landscape maps. Let the prose set up the taxonomy the visual shows — a visual should carry the structure, not decorate the page.

Read-aloud test: does the post read like a builder who has actually worked in this area walking a peer through it — naive attempt first, each step earned by the failure before it, options grouped into families and compared on axes with the operational costs named — or like a survey/whitepaper/hype post that ranks tools and skips the failure modes? If the latter, restructure to the arc above.

## 4b. Research-synthesis mode — the investigation arc (mandatory for history/literature-synthesis posts)

This is a mode layer, not a separate voice — it composes with §1–§3 and inherits every ban above. Use it for posts that reconstruct how a technique, idea, or research area got to where it is: "why did X come back", "what changed in the last two years", "a history of Y", posts that synthesise a body of papers into a single narrative. Do not use it for a plain devlog, a single-result post, or a tool/framework landscape (§4 covers that). This is a reasoning and structuring method, extracted from what makes research-history writing work — **not** an instruction to reproduce any particular author's distinctive wording, catchphrases, or sentence rhythm. Apply the method; write the sentences in this skill's own voice (§1–§3).

**Philosophy.** The piece should feel like an expert investigating a question alongside the reader, not a textbook chapter or a generated literature review. It answers not just *what is this* and *how does it work*, but *why did people try this*, *why did earlier attempts succeed or fail*, *what changed recently*, *which assumptions are doing the real work*, *what's established versus speculative*, and *what's still unresolved*. Default shape: **tension → history → conceptual foundations → technical decomposition → current landscape → synthesis → open questions.** Not every post needs every beat, and this is the same §1b teaching progression (concept → mental model → example → why it matters → implementation → nuances → research caveats) run at the scale of a whole literature rather than one idea — reuse it, don't duplicate it.

### Build the evidence map before drafting
For any research-heavy post, do this before writing prose. For each claim that matters, note: the claim, its source, the type of evidence behind it, your confidence, whether it's fact or interpretation, any conflicting evidence, and whether newer work supersedes it. Then work out, from the map: the central question the post is investigating, three to six major themes, the real turning points, where genuine disagreement exists, your own interpretation, and what remains unresolved. Draft only after this exists. This step is what prevents an encyclopedic, paper-by-paper survey — the piece needs a thesis and a causal shape (initial promise → stall → why it stalled → what changed → resurgence → what that implies) before it needs sentences. If the underlying research doesn't cleanly resolve to a thesis, say that honestly rather than forcing one.

### Open on a tension, not a definition
Skip "X is a technique that…" openings entirely (§1 already bans this; this is the research-post case of it). Open on the recent development, why it's surprising or important, the question the post will investigate, and — briefly, if relevant — the author's own stake or prior involvement. The goal is curiosity, not a table of contents.

### Tell the history as causation, not a timeline
When the subject evolved over time, organise it around turning points, not a list of papers by year. For each period, cover what practitioners believed, what problem they were solving, the live alternatives, what evidence shifted opinion, and what constraint (compute, data, hardware, an adjacent breakthrough) mattered. Date-stamped headings ("2022: the first attempts", "2024: why it stalled") are fine when the dates genuinely carry the story; don't force them where they don't. The history should explain the present, not just precede it — every historical beat should answer "and that's why the current approach looks the way it does."

### Alternate exposition, intuition, and interpretation
Don't stay in literature-summary mode for paragraphs at a stretch. Move between: explaining the mechanism precisely, giving the reader a mental model for why it behaves that way, and saying what the result means or where the uncertainty sits. After laying out technical facts, periodically answer the unspoken "so what" — in declarative prose, not as a posed question (§2c still applies).

### Decompose the system into ingredients, then reuse them
For a complex family of methods, name a small number of real design dimensions (representation, objective, training procedure, inference procedure, evaluation, scaling behaviour — whatever actually varies here) and give each a short subsection: intuition, mechanics, trade-off. Then reuse those same dimensions when comparing specific systems later, so the reader compares against a schema instead of re-learning each paper from scratch. A compact label or symbol for a recurring dimension is fine if it earns its keep — deliberate recurrence (a concept introduced once becomes shorthand later) is a real technique for managing a long piece; don't reintroduce a concept from scratch once it's been established (§1b already asks for this at the paragraph level — this is the same rule at the scale of a whole vocabulary).

### Explain mechanisms causally
Don't stop at "method A beats method B." Ask what information each method has access to, what constraint changes, what assumption is being made, where information is lost, what happens in the limiting case (one step, infinite capacity, an empty or enormous input), and what gets expensive as scale grows. Prefer a small thought experiment over an unexplained claim.

### Ground abstractions in a tiny concrete example
The moment an abstract property is introduced, reach for a small, specific example that makes the mechanism visible rather than decorating the prose. This is §1b's "concrete example" beat, applied specifically to conceptual/theoretical claims.

### Treat papers as evidence for an argument, not as the structure of the post
Never write "Paper A did X. Paper B did Y. Paper C did Z." Work out the underlying question first, then group papers by what they're evidence for: competing solutions to the same problem, generations of one idea, a shared recipe, theory versus empirics, papers that moved the field's consensus. A paper earns a mention because it's evidence for the argument, not because it exists in the space. When a specific recipe recombines known ingredients (e.g. "this system pairs a pretrained representation with a fixed noise schedule and self-conditioning"), name the combination and explain the trade-off it buys — don't just enumerate the parts.

### Calibrate certainty explicitly
Distinguish, in the prose itself, between what's established (direct strong evidence), what's likely (a reasonable read of indirect evidence), what's speculative (a hypothesis about why the field moved), and what's genuinely unknown. Ordinary phrases do this: "the evidence suggests…", "a plausible explanation is…", "it's hard to know for certain…", "my read is…", "I'm less convinced that…", "this remains unclear." Never let a hypothesis read as an established fact. This sharpens §1's existing opinion-marking rule (mark a judgement as a judgement) specifically for claims about *why* a field moved the way it did, which is exactly where writing tends to slide from evidence into narrative certainty without noticing.

### Say why the idea showed up when it did
Research doesn't happen in a vacuum. Where it's genuinely relevant, connect a method's timing to available compute, the dominant architecture of the day, a new training objective, a changed evaluation norm, cheaper inference, new open-source tooling, or an adjacent breakthrough. "Why was this compelling now and not three years earlier?" is often the most informative question in the piece. Where the field's consensus visibly shifted, say so with a hedge appropriate to the evidence — "a rough consensus formed around…", "research activity shifted toward…" — rather than "everyone believed X," unless that's actually well supported.

### Anchor new ideas against the baseline the reader already knows
For each new approach, compare it to the dominant baseline on training, inference, what it newly enables, what it makes harder, and the compute trade-off. Repeated anchoring against something familiar does more work than an isolated description of the new thing.

### Include the dead ends, and the ugly tricks that work anyway
A mature synthesis includes what didn't work: what was attractive about the idea, what actually went wrong (theoretical, empirical, scaling, or just implementation), and whether later work fixed it. Separately, flag any technique that's empirically essential despite conflicting with the elegant theoretical story — and dig into why. That tension is often the most interesting part of a research post; don't smooth it over.

### Separate elegance from empirical performance
Don't assume the theoretically cleaner method wins. Keep conceptual simplicity, theoretical guarantees, training efficiency, inference efficiency, scalability, implementation complexity, and raw empirical performance as separate axes, and say plainly when they pull in different directions.

### Read the evaluation critically before citing the numbers
Before reproducing a benchmark comparison, check whether the systems were compared at equal compute, equal parameter count, equal sampling budget, equal latency, on a proxy metric, or on a benchmark one side may have tuned against. If the evaluation methodology could change the conclusion, that belongs in the post, not just the number.

### Make the practical stakes explicit, once
Connect the research property to an actual consequence a practitioner cares about — fewer sampling steps means lower latency, more flexible generation means easier constrained decoding, and so on — without turning the post into a pitch (§2's hype ban still applies in full).

### Weave references into the argument
This sharpens §3 for research posts specifically: a citation belongs at the exact point it substantiates a claim, not in a detached related-work block. Name the specific contribution being relied on, don't overstate what the cited paper actually showed, and keep the paper's claim distinct from your own interpretation of it. Never fabricate a citation, a result, or a date; if a claim can't be verified, mark it as uncertain or drop it. If you're claiming a trend across a literature, make sure more than one piece of evidence actually supports it.

### Article skeleton (default, adapt freely)
Opening tension → historical context → conceptual prerequisites → technical decomposition (ingredient by ingredient) → representative systems/recipes → recent developments organised by trend, not publication order → why now → the strongest competing interpretation, stress-tested → what remains unresolved → what's next, uncertainty marked → closing synthesis (what you now believe that you didn't before, not a section-by-section recap) → references. Use only the beats the subject actually needs — a mechanical run through all of them for a post that doesn't warrant it produces exactly the flat, encyclopedic survey this mode exists to avoid. Length is earned by genuine complexity, not padded to look thorough (§2's hype ban) or trimmed to hit a word count (§1b's depth-preservation rule) — this is a research post's version of "don't self-sabotage the work," so let it run long when the material actually requires it.

Read-aloud test: does the post read like someone who has followed the field for years, reconstructed why it moved the way it did, checked the evidence, and is now walking a curious reader through their reasoning — leaving both a working mental model *and* a sense of what's actually settled versus still open? Or does it read like a paper-by-paper survey with polished transitions? If the latter: check that the evidence map produced a real thesis, that papers are grouped by argument rather than listed, and that certainty is calibrated throughout, not just in a caveats paragraph at the end.

## 5. Pre-publish self-check (run before declaring any post done)

1. Read the opening aloud. Does it start on the concrete thing, or on throat-clearing / a slogan / a definition? Fix the opening if it doesn't earn the next paragraph.
2. Every empirical or factual claim that matters: is it backed by a linked source, a number, code, or a chart — verifiable in under a minute? Flag any bare claim and either support it, soften it to a marked opinion, or cut it.
3. Banned-construction check — TWO stages, both mandatory:
   a. Mechanical: grep for em-dashes (look for chains and nested pairs, not single appositives), intensifier adverbs, the hype-vocabulary list (§2) including the corporate-polish clichés ("changes everything", "future of AI", "ultimate framework", "comprehensive deep dive", "unlocks unprecedented", "Cambrian explosion", "production-grade paradigm"), and the LLM-tell metaphors ("load.?bearing", "linchpin", "cornerstone", "heavy lifting", "delve", "in the realm of", "it's worth noting"); count and justify every remaining instance — the justified count should be zero.
   b. Semantic: greps can't catch inversions, pivots, triadic fragments, clickbait titles, keynote sentences, or marketing register. Read every sentence and every heading for them. For a long post, run this as a fresh-context pass — hand the full draft and the §2 ban list to a subagent and have it return line-numbered violations with flat rewrites — then apply the fixes. Never report this item as PASS on the strength of stage (a) alone.
   c. Calmness pass (§2d): review every section title, caption, transition, and historical claim. Are the titles descriptive rather than dramatic? Are importance claims proportionate (importance-at-the-time vs usefulness-today vs influence)? Are limitations stated plainly? Is there any unnecessary "breakthrough", "wall", "trick", "hidden", "the part everyone misses", "changed everything", or "resounding yes" phrasing? Does the piece read as a measured technical essay rather than a promotional explainer? Replace sensational wording with the calmer alternative, keeping the explanation intact.
   d. Machine-texture pass (§2e): count the em-dashes (flag if more than roughly one per 150 words, or two in any paragraph) and thin them to full stops/commas; grep for the meta-narration scaffolds ("one thing worth", "the easiest way", "here is the part", "I'll be explicit", "what this comes down to", "the thing that") and cut them; check for compulsive both-sides framing ("two things at once", "cuts both ways", "sits between") and the tidy-summary-per-paragraph habit, and break both. Read for the staccato-terse-defensive register: runs of clipped sentences/fragments, grep for the defensive pre-emptions ("to be clear", "this isn't to say", "none of this means", "that's fine", "which is the point"), and relax each into full sentences with objections handled once. This is the pass that stops a clean-vocabulary draft from still reading LLM; never skip it on the strength of (a).
   e. Anti-sensationalism pass (§2d, four-level pass), four levels: (1) Sentence — grep for the stakes phrases ("the real question", "key insight", "hidden", "the surprising part", "what this really means", "the most interesting part", "changes everything", "breakthrough", "the trick", "the catch", "the twist", "the magic", "the secret", "where things get interesting", "why this matters", "what happens next", "the future of", " is dead", "is not enough", "finally works") and rewrite each as a plain descriptive claim; the justified remaining count should be zero. (2) Paragraph — confirm no paragraph is built setup → delay → reveal; move any withheld point to the first sentence. (3) Heading — every heading describes its section, none teases a payload. (4) Conclusion — the closing lines end on a concrete next step or practical takeaway, not a grand claim, dramatic future-framing, or field-level prediction.
4. Self-sabotage sweep (§2b): scan for the imposter preamble, false modesty, self-deprecating verbs on neutral outcomes, and hedges on things you actually measured. Reframe each neutrally while keeping every fact and caveat. Re-read the opening and the closing specifically — those set and leave the impression.
5. Rhetorical question sweep (§2c): count every question mark and every phrase like "the question is", "asks whether", "what does X add", "what remains", "why does this matter". Keep only questions that a human author would naturally ask. Rewrite all scaffolding questions as declarative claims.
6. Title check: does it say what the post is about (and ideally what you found), without clickbait or empty aphorism?
7. Formatting check: bold and lists used for genuine emphasis/structure, not sprayed for energy. No bolded full sentences, no bulleted paragraphs.
8. Opinion/measurement check: every "I think"-class statement is marked as a view; every measurement has its evidence. Neither is disguised as the other.
9. Spelling consistent with the chosen variant throughout — no mixing.
10. Builder's-map check (§4) — only for landscape, tool-comparison, architecture, or agentic-system posts; skip for a plain devlog or single-result post. Confirm: the post follows the arc (plain entry → naive path → failure modes → trade-offs → design families → operational realism → modest conclusion); jargon is introduced only after a plain-language mental model; each option is explained by what it solves, what it breaks, and its new trade-off (nothing is framed as simply "better"); comparisons use axes and design families, not rankings, with table-stakes separated from differentiators; the operational realities that apply (cost, latency, scale, security, observability, database growth, maintainability, debugging, evaluation, DX, migration) are visible; popularity is treated as a signal, not proof of fitness; abstraction is shown as a trade-off; for agentic posts the agency assumption is made explicit; and the conclusion leaves a map with its uncertain edges named, not a verdict.

11. Structure & cognitive-load check (§1b) — for every post. Read the headings alone: do they narrate a coherent, correct outline, each one a declarative next step, none posing a question or teasing a payload? Then read as a first-time reader: does each section answer the question the previous one raised, without a literal rhetorical question doing that work (§2c)? Does intuition precede every piece of implementation, and does each term arrive only after the idea it names? For any long paragraph, apply the concept test rather than a sentence count: split it only if it bundles separable concepts a reader would navigate between, and leave it if its sentences are one argument building to a single claim (over-splitting manufactures the §2e march, which reads as machine-generated as a wall of text). Cut any paragraph that does none of introduce/explain/contrast/motivate/summarise. For a teaching or tutorial piece, also confirm: the progression (concept → mental model → concrete example → why it matters → implementation → nuances → research caveats) holds where it applies; complexity is layered rather than jumped; misconceptions are handled where they arise, not deferred; observable behaviour is separated from internal implementation; and every figure supports a point the prose already makes rather than replacing it.

12. Research-synthesis check (§4b) — only for history/literature-synthesis posts; skip for a devlog, single-result, or landscape post. Confirm: an evidence map and a real thesis existed before drafting (not just a paper list); the opening states a tension, not a definition; the history explains the present rather than just preceding it; papers are grouped by argument (competing solutions, generations of an idea, a shared recipe) rather than enumerated by name; exposition/intuition/interpretation alternate rather than running in one long literature-summary block; certainty is calibrated throughout (established vs likely vs speculative vs unknown), not just hedged in a closing caveats paragraph; dead ends and any theory-defying-but-essential tricks are included; evaluation methodology is checked before a benchmark number is cited; references are woven at the point they substantiate a claim, not dumped in a block; and the ending states an updated view plus open questions, not a section-by-section recap.

13. Concrete-explainer check (§1c) — for posts explaining a technical or mathematical result. Confirm: each hard idea opens with a concrete scenario that genuinely matches it before the formal term; background is limited to what the reader needs; each major result states what was known, what changed, and what limits it, separating theoretical importance from practical use; scale numbers are translated into defensible physical comparisons; the impressive claim → intuition → inconvenient fact pattern appears where a claim warrants it; caveats sit at the point they apply, in plain words (no "the catch" label); humour, if any, comes from the facts and stays sparse; headings state findings without teasing; footnotes (if the format has them) carry real information; and any wide-lens ending is modest and flagged as uncertain where it is.

14. Intellectual-stakes check (§1d) — for posts reporting a result, development, or change of belief. Confirm: a technically literate outsider can see why it matters; the post states what experts believed before; every strong claim is earned by evidence → context → comparison rather than adjectives; observation, inference, and prediction are kept distinct; the strongest objection or caveat is stated fairly, not buried; theoretical and practical significance are separated; discovery, verification, and understanding are not conflated; any expert reaction or anecdote supplies information and any belief update is genuine; the post moves between micro, meso, and macro without staying macro; at least one concrete example makes the abstraction intuitive; compressed one-liners and jokes are few and earned; sentences that can be deleted without loss are deleted; and the ending shows a consequence or names an unresolved tension without breaking §2d Level 4.

Report the outcome of this checklist to the user explicitly — pass/fail per item — before calling the post finished.

## One-line summary

Write like a clear person talking — first person, concrete, one claim per sentence, intuition before formalism — and structure the piece to lower the reader's load without losing depth: each section answers the question the last one naturally raised (answered in statements, not posed as questions), every term arrives after the idea it names, and each paragraph holds one concept. Strip every construction that puts rhetoric ahead of substance, keep the register calm and measured (descriptive titles, proportionate claims, no manufactured drama), word your work neither above nor below what it deserves, and make every claim that matters checkable in under a minute. For a post that maps a technical design space, add the builder's-map layer (§4): a practical builder walking a peer through the arc plain entry → naive path → failure modes → trade-offs → design families → operational realism → modest conclusion — comparing on axes rather than rankings, keeping the operational costs visible, and ending on a map, not a verdict. For a post that reconstructs how an idea or research area evolved, add the research-synthesis layer (§4b): build an evidence map and a real thesis before drafting, open on a tension rather than a definition, tell the history as causation, alternate exposition/intuition/interpretation, group papers as evidence for an argument rather than list them, and calibrate certainty (established/likely/speculative/unknown) throughout — a structural and reasoning method, not licence to imitate any particular writer's sentences.

## Relationship to academic-prose

This skill governs blog posts and public web prose. For academic papers (.tex files, journal/conference submissions, abstracts, rebuttals), defer to the **academic-prose** skill, which is stricter on machinery (claims boxes, one-protocol-per-table, abstract word limits, signposting) and uses the collective "we". The two share a spine — no hype, no self-sabotage, checkable claims — but a blog relaxes the formal scaffolding and speaks in the first person. If a post is really a paper draft in disguise, use academic-prose instead. If another general writing or style skill conflicts with this one on a blog post, follow this skill and note the conflict.
