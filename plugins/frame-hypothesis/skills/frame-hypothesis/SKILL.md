---
name: frame-hypothesis
description: >-
  Hypothesis-driven problem framing for the start of a project or case: tighten the problem statement, form and stress-test a lead hypothesis against rivals, decompose it into a MECE hypothesis tree (what would have to be true, then the analyses that prove or kill each branch), prioritise the branches by impact, tractability and prior certainty, and hand off a ghost-deck storyline. Use this whenever the user is at the front end of a problem — "frame this", "what's my hypothesis", "build an issue tree / hypothesis tree", "what would have to be true", "is this problem statement tight enough", "which branches should the team chase", "set up the case", "day-zero framing", or any time they describe a question they've been asked to answer and haven't yet decided what to investigate — even if they don't use the word hypothesis.
---

# Frame a hypothesis

A method for the first days of a problem: get the question right, commit to an answer early enough to be wrong, break that answer into the smallest set of things that would have to be true, and decide which of them the team actually chases. It is the upstream half of a loop whose downstream half is a **framing-review** of the deck that eventually argues the answer.

Everything needed is in this file. There are no external files to load.

## Where this sits

- **Upstream:** a problem the user has been handed, in any state — a crisp statement, a vague brief, or an email from a sponsor.
- **This skill:** problem statement → hypothesis → hypothesis tree → prioritised branches → ghost-deck storyline.
- **Downstream:** work packets (splitting the chosen branches into owned workstreams with analyses, data, dates) belong to a separate skill — stop at the prioritised branches and the storyline, and say so. The ghost-deck storyline is built in the exact format the framing-review skill maps (`Slide | Key message | Detail`), so the user can run framing-review on it mid-project to check whether the evidence still argues the original hypothesis or has quietly changed it.
- **Vocabulary:** keep the method's vocabulary generic. If the user has a separate house-language skill, that layer rewrites the outputs; this skill does not.

## Working posture (every stage)

- **The user sets the answer; you test it.** The problem statement, the hypothesis, and the final call on the tree are theirs. Your job is to find the hole, name the missing branch, and generate the rival they haven't considered — not to hand them a finished framing they didn't ask for.
- **Ask before generating.** If the user hasn't put down their own view at a stage, ask for it first. The one deliberate exception is rival hypotheses (stage 2), which you generate on purpose so the user has something to defend against.
- **Challenge until told to stop.** Push on weak statements, hypotheses and branches plainly. But when the user says they're comfortable and want to proceed with what they have, stop challenging and proceed — recording any unresolved objection as a kill-test inside the tree rather than relitigating it. The user's comfort is the exit condition, not yours.
- **Be harsh, not kind.** A problem statement that could be read three ways, a hypothesis that can't be false, a tree with an overlap — flag them. Softening a real gap is not useful.
- **Turn open issues into questions.** Hand unresolved points back as a numbered question set — one decision at a time. Only ask what needs the user's judgement.

---

# Stage 1 — Problem statement

A hypothesis about the wrong question is worse than no hypothesis, because it looks like progress. So this stage runs every time, even when a statement is supplied — fast when the statement is already tight.

## If a statement is provided: assess it

Test it against the seven elements below. Report each as **present / weak / missing**, quote the offending phrase, and say what a tight version would need. Do not rewrite the statement; hand back the gaps as questions.

1. **The decision-maker.** Who, by name or role, acts on the answer? "The business" or "the client" is not a decision-maker.
2. **The decision.** What will they do differently once this is answered? If no action depends on the answer, it is a research question, not a problem.
3. **The success measure.** How will they know it worked — a number, a date, a condition? "Improve" and "optimise" without a measure are placeholders.
4. **Scope.** What is explicitly in, and what is explicitly out? Geographies, segments, products, time horizon.
5. **Constraints.** What the answer may not do — budget, headcount, regulatory, political, timing.
6. **Timeframe.** When is the answer needed, and over what horizon must the answer hold?
7. **The one-sentence form.** Can the whole thing be stated as a single question the decision-maker would recognise as theirs?

Three traps to check for explicitly:

- **Solution dressed as problem.** "How do we implement X?" presumes X. Ask what X was meant to achieve, and whether that is the real question.
- **Too broad to be wrong.** "How do we grow?" admits any answer. A tight statement makes some answers obviously out of scope.
- **Symptom, not problem.** "Costs are too high" is an observation. "Which cost lines can be cut by [measure] by [date] without [constraint]?" is a problem.

## If no statement exists: help build one

Ask, in this order, one or two at a time: who decides; what they will do with the answer; what good looks like and by when; what is out of bounds; what has already been tried or ruled out. Draft the one-sentence form only after the user has answered — then put it to them to accept or correct.

**Exit condition:** the user confirms a one-sentence problem statement that names the decider, the decision, the measure and the scope.

---

# Stage 2 — The lead hypothesis

A hypothesis is a provisional *answer* to the problem statement, stated specifically enough that evidence could prove it wrong. Its purpose is to make the work efficient: a good hypothesis implies the analyses, and the analyses imply the data, so the team knows on day one what to go and get.

## What a good one looks like

- **Answer-first.** It states what the answer *is*, not what will be investigated. "Margin decline is driven by channel mix shifting to the lowest-margin partner tier" — not "we will analyse margin by channel."
- **Falsifiable.** The give-away test: could the evidence come back and show it's wrong? If nothing could contradict it, it's a label, not a hypothesis.
- **Specific enough to imply work.** Read it and you should be able to name the first three analyses. If you can't, it's too abstract.
- **Causal, not descriptive.** It explains *why*, or *what would work and why* — which is what makes the tree build itself in stage 3.
- **One sentence.** If it needs two, it is probably two hypotheses; pick the lead one and park the other as a rival.

Ask the user for their hypothesis first. If they have none yet, ask what their gut says the answer is and why — most people have one and are reluctant to commit to it. The reluctance is the thing to push through; a wrong hypothesis committed to early is cheap to kill, a hypothesis withheld costs a week of unfocused analysis.

## Generate rivals, then let the user defend

Once the user has a lead hypothesis, generate **two to four rival hypotheses**. Rivals must be *different explanations*, not restatements or weaker versions of the lead — each should imply different analyses and a different answer for the decision-maker. Useful angles for finding them:

- A different causal driver (demand vs supply, price vs volume, capability vs incentive, structure vs behaviour).
- A different unit of analysis (segment, geography, channel, time period).
- The sponsor's own favourite explanation, stated at its strongest.
- The uncomfortable one — the explanation that would make the project unnecessary, or point the finger at the sponsor.
- The null: the thing the user thinks is a problem is within normal variation and will revert.

For each rival, state in one line what evidence would distinguish it from the lead. Then ask the user to defend their lead against each — or to switch.

**The override.** When the user says they are comfortable with their hypothesis and want to proceed, proceed. Do not keep relitigating. Fold any rival that survived into stage 3 as an explicit kill-test branch ("if [rival] is true, we would see [X]; checking [X] rules it in or out"), so it is tested cheaply rather than argued about.

**Exit condition:** one lead hypothesis in a single falsifiable sentence, plus a short list of surviving rivals to carry into the tree as kill-tests.

---

# Stage 3 — The hypothesis tree

Decompose the lead hypothesis top-down. This is a hypothesis tree, not an issue tree: every node is a claim that could be true or false, not a question or a topic.

## Structure

```
Lead hypothesis (the answer, one sentence)
├── Condition 1 — what would have to be true
│   ├── Sub-hypothesis 1.1 — a narrower claim
│   │   └── Analysis: what to do · Data: what it needs · Kill signal: what result disproves it
│   └── Sub-hypothesis 1.2
│       └── ...
├── Condition 2
│   └── ...
└── Kill-test — surviving rival from stage 2
    └── Analysis that rules it in or out
```

- **Level 1 — necessary conditions.** Ask "for the hypothesis to be true, what would *have* to be true?" Aim for three to five conditions. Each must be a claim, phrased so it could be false.
- **Level 2 — sub-hypotheses.** Narrow each condition until a leaf is reached.
- **Leaf = an analysis someone can start on Monday.** A leaf names the analysis, the data it needs, and the *kill signal* — the result that would disprove the branch. Stop decomposing when you reach that; going deeper is planning, not framing.

## The MECE tests — run both, separately

- **Mutually exclusive (no overlap).** The practical test: would the same analysis resolve two branches? If yes, they overlap — merge or re-cut. Overlap is where teams duplicate work and where two workstreams reach contradictory conclusions from the same data.
- **Collectively exhaustive (nothing missing).** The practical test: if every level-1 condition were proven true, would the hypothesis be *proven* — or could a sceptic who knows the domain still say "yes, but…"? Whatever the sceptic would say is the missing branch. Run this at each level, hardest at level 1.

Report overlaps and gaps plainly, with the branch that needs merging or adding. Then put the tree to the user: the cut is theirs, the test is yours.

**Where the user's draft tree is a list of topics** (functions, regions, workstreams-in-waiting) rather than claims, say so: a topic tree can be MECE and still tell the team nothing about what to prove. Convert the topics to the claims they imply, and check the result against the hypothesis.

**Exit condition:** a tree where every node is a claim, level 1 passes both MECE tests, every leaf names an analysis, its data and its kill signal, and surviving rivals appear as kill-test branches.

---

# Stage 4 — Prioritise the branches

Not every branch gets chased. Two separate judgements, kept separate because collapsing them biases the team toward what fits rather than what matters.

## First: rank the branches on what they're worth

Score each level-1 condition (and any leaf that stands out) on three dimensions. Use High / Medium / Low; precision here is false.

- **Impact.** If this branch turned out false, how much of the answer collapses? A branch whose failure kills the hypothesis outright is the highest impact there is. This is the load-bearing claim.
- **Tractability.** Can the team get the data and run the analysis within the time available? Be honest about data that "exists somewhere".
- **Prior certainty.** How confident is the user — or the sponsor — that it's already true? High prior certainty does not mean skip it; it means *verify cheaply, don't investigate at length*. Low prior certainty on a high-impact branch is where the project's real risk lives.

Then apply two rules:

- **Kill-tests first.** Anything cheap that could disprove the lead hypothesis runs in the first days, before the team is invested. The branches most likely to kill it and the rivals from stage 2 are where to look.
- **Disproportionate effort on the crux.** The branch with the highest impact and the lowest prior certainty is where the project is won or lost. Flag it explicitly; it should get the strongest analyst and the earliest sponsor conversation.

Produce a ranked table: `Branch | Impact | Tractability | Prior certainty | Kill-test? | Verdict (chase / verify cheaply / park)`.

## Second: size against the team

Only now bring in the team. Two inputs, asked for rather than assumed:

- **The team.** How many people, for how long, with what skills — and whether the team is *fixed* (size and people already set) or *flexible* (the user can still shape it). This changes the direction of the fit: a fixed team is sized to; a flexible team is sized from the branches.
- **The effort per chased branch.** For each "chase" verdict, a rough load — small (days), medium (a week or two), large (most of the project) — and whether it needs a particular skill (modelling, interviews, data engineering). Effort is a property of the analysis at the leaves, not of the branch's importance; a crux can be small and a low-priority branch can be large.

Then fit one to the other:

- Bundle small branches: one person can hold two or three if they share data or method. Split a large branch only if its sub-hypotheses can be worked independently; otherwise it is one person's whole project.
- Keep the spine free: whoever synthesises across branches should not also own the largest one.
- **Fixed team, load exceeds capacity:** go back to the ranking and move branches from "chase" to "verify cheaply" or "park" — don't thin every branch's analysis, because a branch done shallowly proves nothing.
- **Flexible team:** state the team the chased branches actually need, by number and skill, and let the user decide whether to ask for it or cut scope.
- Branches ranked "chase" that don't fit are **parked with a trigger** — the condition under which they get picked up (a kill-test fails, a sponsor asks, a branch closes early). Parked is not dropped; say which is which.

**Exit condition:** a ranked table with verdicts, the crux named, kill-tests identified for the first days, and a parked list with triggers. Stop here on workstreams — handing the chased branches to the work-packets skill is the next step, not this one.

---

# Stage 5 — The ghost-deck storyline and handoff

Write the answer deck now, before any analysis, as a storyline of claims. This is the ghost deck: each row is a slide whose title is the hypothesis or branch stated as a claim, and whose body will be the evidence once gathered. Its value is that it makes the end-state visible on day one and shows immediately where the storyline has a hole.

Build it in the format the framing-review skill maps, so it can be reviewed directly:

```
Slide | Key message (the claim, stated so it could be false) | Analysis that would prove it | Status
```

- Row 1 is the lead hypothesis as the governing message.
- One row per chased branch, in the order the argument needs — not the order of the tree.
- Mark the **load-bearing claim** (the crux from stage 4) explicitly; framing-review will look for it.
- Status column starts as *assertion* for every row. As evidence arrives it moves to *partly evidenced* / *evidenced*; a row that moves to *disproved* is the signal to re-run stage 2.
- Parked branches do not get rows. If the storyline can't argue without one of them, it wasn't parked, it was chased — go back.

**Handoff.** Tell the user, in one line each: the storyline is ready for a framing-review (workflow C, create a new deck) whenever they want the argument pressure-tested; the chased branches are ready for the work-packets skill to turn into owned workstreams.

---

# Output — the hypothesis charter

Deliver one artefact, the **hypothesis charter**, as a document (`.docx` when a file environment is available; otherwise inline markdown or an artifact — the content is identical, only the container changes). Sections, in this order:

1. **Problem statement** — the confirmed one-sentence form, then the seven elements as a short table (`Element | Content`).
2. **Lead hypothesis** — one sentence. Beneath it: *Rivals considered* (one line each, with the evidence that distinguishes it) and *Rivals carried as kill-tests*.
3. **Hypothesis tree** — the full tree, as an indented list or table (`Level | Claim | Analysis | Data | Kill signal`). Note the MECE check results beneath.
4. **Prioritisation** — the ranked table with verdicts, the crux named, team sizing and the parked list with triggers.
5. **Ghost-deck storyline** — the four-column storyline table.
6. **Open questions** — the numbered set the user still needs to decide.

Don't pad it. A charter the user can read in five minutes before a sponsor meeting is the point.

---

# Worked examples

*[Placeholder — deliberately empty in the published version. Examples are built up locally from live use (a loose problem statement and its tight form; a lead hypothesis with the rivals that nearly beat it; a level-1 cut that failed the sufficiency test and the branch that was missing) and removed before the file is pushed publicly. Until then, judge each stage by its tests directly: can the statement be read one way only; could the hypothesis be false; would one analysis resolve two branches; would a domain sceptic still say "yes, but".]*
