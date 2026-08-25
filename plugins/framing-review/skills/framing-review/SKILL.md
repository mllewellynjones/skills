---
name: framing-review
description: >-
  Structure, framing, and storyline review for slide decks and written documents. Use this whenever the user wants to build or pressure-test the ARGUMENT of a deck or a document — either creating a new one (a memo, report, brief, proposal, or a new PowerPoint / pitch deck) or reviewing an existing one. Trigger it for requests like "review this deck", "pressure-test my presentation", "help me structure this memo/report/proposal", "does this actually argue", "is my storyline right", "frame this before I write it", "give me feedback I can send the author", or any question about whether a deck or document makes its case to its audience — even when the user does not name this method.
---

# Framing & review

A method for building and critiquing the *argument* of a deck or document — not its wording or visuals, but whether it moves a specific audience from their prior to a decision. It works by separating two jobs: **you (the AI) build the as-is picture; the user sets the should-be.**

Everything needed is in this file — the full framework, the coverage check, the titles guidance, and the layouts to rebuild the templates. There are no external files to load.

## The golden rule: output matches the target artefact

Default: a deck in → deck out (`.pptx`); a document in → document out (`.docx`). **The user's explicit request overrides the default** — a memo-to-deck conversion, or "review this deck but give me the feedback as a doc", targets whatever they asked for. What's forbidden is *silently* switching container. Rebuild the relevant scaffold from the layouts in the last section. **If there's no file-creation environment** (a plain chat with no code tools), deliver the same content inline — the storyline map and feedback as markdown tables, or as an artifact — rather than refusing; the thinking is identical, only the container changes.

## Working posture (every workflow)

- **You build the as-is; the user sets the should-be.** Mapping and gathering are yours. The spine and the ordering are theirs. Do not hand them a finished should-be they didn't ask for.
- **Ask before generating.** If the user hasn't shared their own view, ask for it first — don't produce a rewrite or framework pre-emptively.
- **Critique before replacing.** Engage with their draft: find gaps, steelman alternatives, stress-test assumptions. Don't silently substitute your framing for theirs unless theirs is demonstrably wrong.
- **Be harsh, not kind.** Flag weak links, unearned claims, and missing pieces plainly. Kindness that softens a real problem isn't useful.
- **Turn open issues into questions.** Hand unresolved points back as a numbered question set — one decision at a time — rather than resolving them yourself. Only ask what genuinely needs the user's judgement.

## Pick the workflow

Two axes — create vs review, deck vs document — give four workflows. **All four run the shared process in "The process" section below**; only these deltas differ:

- **A — Create a new document.** No as-is map (there's nothing to map). Rebuild the document framing template; challenge weak framing answers — don't accept a governing message that isn't a real causal chain. Only after the framing and section map are set, help draft → `.docx`.
- **B — Review an existing document.** Full process. Map into the section map and give the diagnostic read. Output is the feedback deliverable for the author → `.docx`.
- **C — Create a new PowerPoint.** No as-is map. Rebuild the deck framing template; one key message per slide; every slide gets an **action title** (see titles guidance). Only after the framing is set, help build slides → `.pptx`.
- **D — Review an existing PowerPoint.** Full process. Map into the charter (framing fields + storyline table); diagnostic read: do the titles argue top-to-bottom, or are they topic labels? Output is the five-slide feedback pack (layout below) → `.pptx`.

---

# The framework — judge at three altitudes, in this order

## Purpose & audience — the governing lens, assessed first

Everything else is judged through this. Propose a *candidate* reading from the artefact itself (most state their audience and ask) and put it to the user to confirm or correct. The final call is theirs.

- **Who does it address, and who does it arm?** Name the specific person who acts on it. Are they the decider, or a sponsor who has to carry it onward to *other* deciders? A piece aimed at a decider argues *to* them; a piece that arms a sponsor must give them an argument they can rebuild in a room the author isn't in, in their own language. If the intent is to *equip* someone to approve some things and carry others onward, it should read as equipping them — not as assigning them work.
- **Ask-owner fan-out.** List every ask and its owner. If the asks fan out to several owners — especially across teams or business units — each owner has a different fear. Either each fear gets its own answer, or the piece explicitly arms one person to carry the others. A single artefact trying to persuade five owners at once usually persuades none; ask whether it should even be one artefact.
- **What are their priors?** Hostile, neutral, or sponsoring? What do they already believe, and what's the single strongest reason they'd say no? It must meet the *real* objection, not a convenient version.

## The governing message & the argument

- **The governing thought.** The whole case in one sentence. A strong one is already a causal chain (X → so Y → so Z), because then the structure almost falls out of it — each link is a claim a unit must establish. Every unit must ladder up to it; if one doesn't, it's a cut candidate.

  **Worked example — to be captured from live use.** *[Placeholder — deliberately empty. On the first live use of this skill: once the user lands a governing message that passes the causal-chain test, propose adding a before/after pair here — their weak first attempt vs the final chain. This file is published publicly, so anything added to it must be fully anonymised first: strip or replace organisation, product, tool, and team names; round or alter any figures traceable to real work; keep only what teaches the pattern. Then update this file and hand back a repackaged `.skill` for the user to re-save. Until then, judge governing messages by the test directly: does it chain (X → so Y → so Z), and could each link be false?]*

- **The load-bearing claim (the crux).** Find the single claim the whole argument rests on — the one that, if the reader rejects it, collapses everything downstream. Check it is *evidenced, not asserted*. This is where evidence-vs-assertion matters most and where drafts most often leave a bare assertion. If it can't be fully evidenced, name the honest fallback claim that still survives a sceptic who knows the domain.
- **Necessary and sufficient.** *Necessary*: remove any unit and the argument breaks. *Sufficient*: nothing load-bearing is missing — including for any secondary owner the artefact must stand alone for. Run both.
- **No redundancy.** Is the same point made under different headings/titles? Reinforcement is deliberate and earns its place; repetition is padding.
- **The shortest chain.** The ideal structure is the shortest sequence of claims that moves the reader from their prior to the ask. Start from the ask and the strongest objection, and work back.

## Credibility for a decision

An all-upside case reads as naive to a senior reader. These are **separate bars** — a piece can clear one and fail its neighbour, so score them individually, never bundled:

- **Alternatives considered** — the real option space, weighed and rejected for reasons (not one strawman). Including the *do-nothing* option, named as the sceptic would actually frame it (e.g. "renew and change nothing"), not a convenient version.
- **External benchmark** — what comparable organisations do. Cheap credibility, often missing. Separate from alternatives.
- **Cost & resourcing** — named honestly, not buried.
- **Risk** — named, with mitigations. Separate from cost — a piece can commit to one and not the other.
- **Dependency floor vs ceiling** — where value depends on an external or uncommitted dependency (another team's roadmap, a hire, a data estate), split what the thing delivers *standalone* (the floor) from what the dependency *unlocks on top* (the ceiling). Otherwise the headline value is hostage to something outside the decider's control, and the ask becomes conditional.
- **Grounded in the specific organisation** — at least some of it must turn on real teams, numbers, and constraints of *this* org, not generic best practice. Name the honest seams too: where the argument has grey areas, say so rather than pretend it's clean — a sharp reader will find them anyway.
- **Evidence vs assertion** — how much is claimed vs shown. Assertion-led is fine for a discussion draft; name it as a dimension either way.

## Each unit holds up

- **One point per unit** (slide, or section/paragraph). Everything in it supports that one point. Two points = split it.
- **The message carries** — via the title (decks) or the topic sentence (documents). See the titles section.

---

# The process

All four workflows follow this spine; creates skip step 2 (there's no artefact to map yet — the map is built *from* the user's spine in step 3).

1. **Fill the framing first.** For a review, extract a candidate framing from the artefact and put it to the user to confirm or correct; for a create, help the user fill it, challenging weak answers. Distinguish the one *governing* ask from any *enabling* asks beneath it. Fix type/length/register (documents) or read-vs-live mode (decks) up front.
2. **Map the current artefact (you do this — reviews only).** Build the storyline map. Deck: `Slide | Key message | Detail`. Document: `Section title | Key message | Supporting detail`. Write the *key message* as the claim the unit actually advances, not its label. Then read the key-message column top to bottom and report: does it argue or just list; where is it redundant; does it lead with the answer or build to it.
3. **Build the should-be map (the user does this).** From the governing message, the user lays out the shortest chain of claims — the spine and the order. Once set, you help turn it into the key-message column and flag where a claim is still an assertion. **Do not pre-empt this. Challenge the user to set it; do not build it for them.**
4. **Objection test.** For each distinct reason the audience would say no — and, for a multi-owner artefact, for each owner — confirm a unit neutralises it, or that the piece arms someone to carry it.
5. **Convert the gaps into questions.** Hand the user a numbered question set to work through, one decision at a time.
6. **Compare and give feedback (reviews) or help build (creates).** Reviews: three buckets — *what's good (keep)*, *what's changed*, *why these are the right changes*. Don't rewrite the artefact; surface the delta and the reasoning, and let the user decide. Creates: only after the framing is set, help draft the document or build the slides.
7. **Run the coverage check** (below), harshly.

**Reusable feedback deliverable.** When the output is feedback to hand to an author, package it as: (a) the current storyline, (b) the suggested storyline, (c) a change-and-rationale table — framed as *"here's what I'd do; incorporate it if you agree, or challenge it otherwise."*

---

# The coverage check — score the plan, harshly

Score each bar **strictly, against the structure/plan — not the finished prose or visuals.** Keep them separate; a bundled line hides a split verdict.

- **Alternatives** — real alternatives, incl. an honestly-framed do-nothing, weighed and rejected for reasons?
- **External benchmark** — any external comparison?
- **Cost** — cost/resourcing addressed?
- **Risk** — risk addressed, with mitigations?
- **Dependency floor vs ceiling** — where value rests on an external or uncommitted dependency, is standalone value split from what the dependency unlocks? Score this only where such a dependency exists (mark n/a otherwise) — but check honestly whether one exists before waving it through; most decision cases have at least one.
- **Business-specific** — turns on specifics of this organisation?
- **Skim test** — read titles (decks) or headings + topic sentences (documents) alone: do they form the argument?
- **One point per unit** — does each unit make a single point?

Alongside the ticks, report **evidence vs assertion** as a graded dimension — *assertion-led / partly evidenced / evidenced* — not a pass/fail bar; where it sits determines what the artefact can honestly claim to be (discussion draft vs decision case).

**Scoring rule:** the check reviews the *plan*, not the finished text. If a unit explicitly commits to covering something — in its title/heading or stated content — it counts as covered; assume it'll be delivered. **But it must be explicit, never "this could plausibly fit under that title/heading."** A named placeholder (e.g. `[cost + risk TBC]`) counts; vague adjacency does not. This rule pulls its weight hardest on live drafts, which are placeholder-heavy.

---

# Titles & messages

The underlying principle is universal — *message-first, structure-as-argument* — but the instrument differs by medium.

## Decks

**Action titles** (a.k.a. message or takeaway titles; from consulting practice and Barbara Minto's Pyramid Principle). Each title is a specific assertion — the "so what" — not a topic label. Two sharpenings:

- The title must be a *specific assertion*, not a less-vague label. "Q3 AI containment performance" is still a topic. "AI containment rose from 30% to 50% after the chatbot rollout" is a message. **The give-away test: could the title be false?** If it can't be contradicted, it's a label wearing a message's clothes.
- **Test the whole deck:** read only the titles, top to bottom. If they tell the complete story on their own, it's right — and each slide's body is then just the evidence for its title's assertion.

**Boundary condition — read decks vs live presentations.** Action titles are best practice for *read decks*: board packs, consulting deliverables, leave-behinds, anything that circulates without the presenter in the room. For *live keynote-style* presentations there's a legitimate opposing school (Duarte, Reynolds): slides should be near-textless and the message should live in the presenter's mouth, not on the slide. Establish which mode the deck is in before applying action titles reflexively.

## Documents

The Pyramid Principle was written mostly about *writing*, so the message-first logic applies strongly: lead with the answer (BLUF), make each section open with its governing point, and let structure carry the argument. But the tactic "put the message in the heading" transfers only *partially*:

- A slide is a discrete unit, skimmed and read out of order, so the title does all the connective work alone. A document has prose, transitions, and paragraph flow doing that work, so the assertion can safely live in the **opening sentence of a section** rather than being crammed into the heading.
- In formal reports, forcing every heading into a full declarative sentence reads oddly and clutters the page; conventional practice keeps headings as concise informative labels and puts the punch in the first line beneath. Message-headings in documents are a legitimate but register-dependent *choice*, not the near-universal rule action titles are for decks.
- The document-level equivalent of the title-flow test: **strong topic sentences plus an executive summary that states conclusions, not contents.** The skim test runs on headings + topic sentences.

Same principle, different instrument. A useful diagnostic for the author: *where is the document losing the reader — at the heading level, or in the first sentence under each heading?* That tells you which lever to pull.

---

# Deck ↔ document adaptations

- **Unit of argument.** Deck = slide; document = section/paragraph. Storyline table → section map.
- **Where the message lives.** Deck: in the title (action title). Document: in the topic sentence; heading-as-claim optional and register-dependent.
- **Front-load the answer.** Documents want BLUF *or* a standalone executive summary (~½ page) carrying the whole argument. Prefer the standalone summary when the document is forwardable or serves several owners.
- **The ask.** Deck lands on one ask; a document usually has one *governing* ask plus *enabling* asks, each with an owner.
- **The destination echoes the opening.** The deck's landing slide becomes a recommendation/conclusion that echoes the opening summary.
- **Connective tissue matters more** in a document (read in one linear pass); each section should follow from — and close the open question left by — the last.
- **Exhibits stay a live check** for exhibit-heavy documents (comparison tables, financials, risk tables): is the comparison a fair fight, does the financial framing match the ask, does each exhibit make one point. Only slide-real-estate mechanics (overflow) drop away.
- **Register and length replace "altitude."** Fix document type, length, and register up front.
- **What stays identical.** Audience-as-lens; the governing thought; necessary-and-sufficient; no redundancy; the credibility bars; the fill-the-framing-first process; the load-bearing-claim and dependency floor/ceiling checks; and the harsh, explicit-commitment scoring rule.

---

# Rebuilding the scaffolds on demand

There are no bundled template files. When a workflow needs a template or feedback pack, build it fresh from these layouts (use the `pptx` / `docx` skills when a file environment is available; otherwise reproduce the same structure inline as markdown tables or an artifact). House palette if useful: navy `#12243F`, teal `#2E8B76`, amber `#E3A22E`, light card `#EEF1F5`.

## Document framing template (`.docx`)

A two-part document. **Part 1 — How to use:** title "Document framing template", then the seven principles (condensed from the framework above): 1 start with the framing; 2 lead with the answer (BLUF / standalone summary); 3 let topic sentences carry the argument (skim test; heading-as-claim optional); 4 one point per section; 5 make the argument chain (necessary & sufficient, no redundancy, shortest chain); 6 evidence the load-bearing claim; 7 earn the decision (separate bars incl. dependency floor/ceiling). **Part 2 — The blank template:** framing fields (*Who does it address / who does it arm?* · *Priors* · *Governing message* · *Load-bearing claim* · *Document type · length · register*); an **ask-owner fan-out** table (`Ask type [Governing/Enabling] | Ask | Owner`); a **section map** table (`Section title | Key message (the claim, not the label) | Supporting detail`, ~8 blank rows); and a **coverage check** as a ☐ checklist of the coverage bars above (Cost, Risk, and Dependency floor/ceiling as separate lines; evidence-vs-assertion as a graded line, not a tick).

## Deck framing template + feedback pack (`.pptx`)

Widescreen (13.3×7.5). **Slide 1 — How to use:** title "Build a deck that argues", six principle cards (start with the framing; put the message in the title [action title]; one point per slide; make the storyline argue; earn the decision; ground it in the business), and a footer stating the harsh, storyline-scoring review posture. **Slide 2 — Blank template ("Deck framing template"):** down the left third, the charter — *Who is this for? · What are their priors? · What's the ask? · Governing message* — with a coverage-check card beneath (the coverage bars; render as a compact grid, Cost / Risk / Dependency floor-ceiling separate); the right two-thirds is a full-height storyline table (`Slide | Key message | Detail`).

**Feedback pack (five slides, for a review):** slide 1 how-to-use; slide 2 blank template; slide 3 **original charter** (framing filled in as-is + storyline table + coverage ticks); slide 4 **proposed charter** (should-be framing + revised storyline + coverage ticks); slide 5 **feedback** in three columns — *What was good (keep)* · *What's changed* · *Why these are the right changes*. Coverage ticks follow the scoring rule: an explicit commitment in a key message or detail counts; vague adjacency does not.
