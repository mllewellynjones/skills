# skills

Claude skills for structured knowledge work, published as a [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces).

## Install

### In claude.ai (easiest — no tools needed)

1. Download the zip for the skill you want from the **[latest release](https://github.com/mllewellynjones/skills/releases/latest)** — one zip per skill, rebuilt automatically whenever a skill changes.
2. In claude.ai, go to **Settings → Capabilities → Skills** and upload the zip.
3. That's it — Claude uses the skill automatically when a conversation matches it. To update later, download the new zip and upload again; it replaces the old version.

### In Claude Code

```
/plugin marketplace add mllewellynjones/skills
/plugin install cv-review@mllewellynjones-skills
```

Installed plugins update automatically when their version is bumped.

## Skills

### cv-review

A structured methodology for critiquing CVs. Runs an intake (target role, market, career goal), scores the CV against nine weighted criteria calibrated to the candidate's seniority, applies a "30-second recruiter test", scans for red flags with remedies (short tenures, gaps, downward moves), adjusts for jurisdiction norms (UK / US / DACH / CEE) and sector, then delivers a bullet-by-bullet critique with KEEP / STRENGTHEN / REWRITE / CUT / RESTRUCTURE verdicts and suggested rewrites, closing with a ranked priority action list.

### framing-review

Structure, framing, and storyline review for slide decks and written documents — judging the *argument*, not the wording or visuals. Four workflows (create or review × deck or document) share one process: fix the framing first (audience, priors, governing message, the ask), map the as-is storyline, have the author set the should-be spine, test it against objections, then score a harsh coverage check (alternatives, external benchmark, cost, risk, dependency floor vs ceiling). Includes action-title guidance for decks, message-first prose guidance for documents, and rebuildable framing templates and feedback packs.

### deep-reading

A post-reading debrief that turns non-fiction into active learning, with Claude as a demanding tutor. The reader produces first — free recall with the book closed, their own connections, their own attack on the argument — and Claude challenges second: finding gaps, stress-testing analogies, sharpening generic scepticism into specific counter-cases, and running a source-credibility check. Every session includes a mandatory challenge and a three-dimension grade (recall, depth, challenge) that stays comparable across chapters and books. Works chapter-by-chapter with a whole-book synthesis at the end, or as a single session for articles, papers, and reports — with honest calibration of how well Claude actually knows the specific text.

### decision-deep-dive

A structured decision-making process for situations with real trade-offs, with Claude as a sceptical Chief of Staff. The user writes their own unfiltered first draft before anything else — the process sharpens and tests their thinking rather than generating it. Ten steps follow: a one-sentence decision statement, context and timing (including the cost of inaction), a bounded and then locked option set that always includes "do nothing", decision-specific evaluation criteria, honest pros / cons / risks / irreversibility assessment with no scoring matrices, assumptions and unknowns (with an offer to research the resolvable ones), a forced commitment with consciously accepted trade-offs, second-order effects, and explicit revisit / do-not-reopen triggers. Ends with a decision record for the user's notes system and, if a task manager is connected, a single next action.

### project-setup

A Chief-of-Staff intake for anything that might become a project. Claude classifies it as an Execution Project (the outcome is delivery), a Strategic Bet (learning or validation), or a Decision Project (commitment to a course of action), explains why in one sentence, and waits for confirmation. Each type then gets a deliberately minimal setup. Execution projects get a primary outcome and exactly one next action — no plan. Strategic Bets start with the user's own unfiltered draft, then a hypothesis (If we… / Then we expect… / Because…), success signals, a short pre-mortem, assumptions, three to five validation moves, and an execution boundary defining what AI may generate. Decision Projects get a decision statement, deadline, and first draft, with execution blocked until the decision is made — handing off to decision-deep-dive if the user wants to decide now. Closes with a project summary for the user's notes system and an explicit statement of what is *not* being done yet.

### skills-sync

The maintenance skill for this repo itself. Diffs locally installed skill copies against the published versions, classifies drift by direction (stale local upload vs unpushed local edit), runs a privacy pass before any push, bumps versions so installed users receive updates, and reports what still needs a manual claude.ai re-upload.

---

*What's coming next: see the [roadmap](ROADMAP.md).*
