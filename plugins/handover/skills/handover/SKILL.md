---
name: handover
description: Write or update a handover of the current conversation so a fresh conversation can pick it up with full context, and pick up a conversation from an existing handover. Use this skill whenever the user says "handover", "prepare a handover", "write a handover", "update the handover", "hand this over", "I'm about to run out of context", or asks to save the state of the conversation for later. Also use it when a handover file is present (in the working folder, uploaded, or pasted) and the user says "pick up", "resume", "continue from", or "carry on" — that is the resume side. With no qualifier, the default is to write or update a handover of the current conversation.
---

# Handover

A handover equips a successor to act. It is not a summary: a summary compresses what happened; a handover records the state of the work, what is decided, what is not, and what must not be re-opened. The reader is almost always a fresh Claude conversation with none of this one's context. A human should be able to open it and understand it, but it is not formatted for them.

## Two sides, one skill

- **Write side** (default): produce or update a handover of the current conversation.
- **Resume side**: a handover file is present and the user asks to pick up from it.

With no qualifier, assume the write side. If a handover for this conversation already exists — created earlier in this conversation, or present in `handovers/` with a matching `source` link — update it rather than creating a new one.

## Write side

### Destination

One artefact, two destinations. The content is identical either way — never produce a lighter version for chat.

- **File** (default wherever files can be written): `handovers/handover-YYYY-MM-DD-<slug>.md` in the working folder. The date is the conversation's start date (the date of its first message, not today), and the slug is two to four words naming the topic. If there is no working folder, create the file for download.
- **Chat**: when the user asks for it in chat, or when no file can be written. Useful on a phone, where pasting beats files.

Pick the slug from the objective; don't ask. Don't ask about the destination either — default to the file unless the user said "in chat".

### Content, in priority order

Sections appear in this order so that a run squeezed by a context limit can stop part-way and still leave the most useful material. If you must stop early, end the file with the line `*(partial — stopped at <section>)*`.

1. **Objective** — what this conversation is for and what done looks like, in two or three lines. Where the work is now (phase, or step n of m).
2. **Verify first** — the two or three state claims the successor should check before trusting anything else, and how to check them. Dated.
3. **Next action** — exactly one concrete step the successor can start on without re-planning.
4. **State** — what exists now and where. Every line carries an evidence level: `[verified]` (tool output seen in this conversation), `[claimed]` (stated as done, output not seen), `[assumed]` (never checked). Abandoned attempts live here too: what was tried, why it was dropped.
5. **Outstanding** — decisions still to make (with the options in frame) and actions still to do, as two short lists.
6. **Decisions made** — one line each, with a provenance tag: `[user]` for the user's own call, `[proposed, accepted]` where Claude proposed it and the user accepted. Under each decision, the options discounted and one line on why. Inclusion test for a discounted option: would a fresh conversation plausibly re-propose it? If not, leave it out.
7. **Operating rules** — instructions about how to work that were set during the conversation: constraints, permissions, style, things not to touch. These are not decisions about the work, and they are the easiest thing to lose.
8. **Locators** — file paths, URLs, commit SHAs, issue and ticket numbers, artefact links not already given under State. Exact, never described.
9. **Quirks** — tool and environment behaviour learned the hard way.
10. **Vocabulary** — terms and working names coined in the conversation, defined.
11. **Open questions and assumptions** — what is unknown and matters, and anything the conversation proceeded on as if true without checking.

### What stays out

- Chronology and narrative — nothing is ordered by when it happened.
- The user's prompts restated, or the thinking behind a decision beyond the one-line why.
- Praise, preamble, caveats about the handover itself.
- Anything the successor can regenerate or re-query cheaply.

### Provenance discipline

Claude's own proposals, drafts and recommendations are not the user's decisions unless the user committed to them. Tag `[proposed, accepted]` only where the user said yes. A proposal the user has not answered belongs under Outstanding, listed as one of the options in frame.

### File skeleton

```markdown
---
title: <topic>
started: YYYY-MM-DD
updated: YYYY-MM-DD HH:MM
status: active | handed-over | closed
source: <conversation link, if one exists>
supersedes: <previous handover file, if any>
superseded_by: <next handover file, once split>
---

## Objective
## Verify first
## Next action
## State
## Outstanding
### Decisions
### Actions
## Decisions made
## Operating rules
## Locators
## Quirks
## Vocabulary
## Open questions and assumptions
```

`active` while the conversation is still running; `handed-over` once the user has signalled the conversation is ending; `closed` once a split has replaced it or the work is done. Omit empty sections rather than writing "none".

### Updating a rolling handover

The default rhythm is rolling: create the file at the first milestone, update it at each milestone, mark it `handed-over` at the end. On an update:

- Edit in place — change the lines that changed; don't rewrite the file. Near a context limit a full rewrite is the expensive move. (Where the file isn't persisted between turns, regenerate it; the content rules are the same.)
- Prune as you go. A completed action leaves Outstanding once its outcome is under State. A superseded decision leaves. A discounted option leaves once a successor would no longer re-propose it.
- Bump `updated`, and refresh Verify first and Next action every time — those go stale fastest.

### Keeping it small: split by prune-and-restart

A handover has to fit comfortably alongside a new conversation's context, not compete with it. Guard: roughly 1,500 words. When the file is near the guard, or the work changes phase (design to build, say), split:

1. Set the current file's `status: closed` and `superseded_by:` to the new file name.
2. Create a new file with today's date and a slug for the new phase, with `supersedes:` pointing back.
3. Carry over only live state: Objective (restated for the new phase), Verify first, Next action, current State, Outstanding, standing decisions that are still load-bearing (one line each; keep discounted options only where still re-proposable), Operating rules, Locators, Quirks, Vocabulary, open questions.
4. Where a rationale was compressed out, leave a pointer: "see <old file> for why".

Never split into part 1 / part 2. A successor reads one file to start and follows `supersedes` only when the live file points there. Do the split and report it; don't ask — nothing is lost, the old file is preserved.

### When context is running out

If the trigger is "I'm about to run out of context" or similar, write the file first and explain nothing. One line in chat: the file path, and whether it is complete or partial.

## Resume side

Trigger: a handover file is present and the user asks to pick up, resume or continue from it. Then:

1. **Read the live file only.** If `superseded_by` is set, go to that file instead. Follow `supersedes` only when the live file points there for a specific rationale.
2. **Run Verify first.** Check each claim with tools where available. Report what matches and what doesn't. Treat `[claimed]` and `[assumed]` lines as unverified until checked.
3. **Confirm in four lines, then wait for a yes:** the objective as you understand it, the next action you intend to take, the discounted options you will not re-open, and any Verify-first mismatch. If the user says "just go", go.
4. **Honour the handover.** Don't ask anything it already answers. Don't re-propose a discounted option; if you believe one deserves re-opening, say so explicitly with the new reason, never silently. Apply the Operating rules from the first message onward.
5. **Adopt the file.** It is now this conversation's rolling handover: set `status: active`, update `source` to this conversation, and keep it updated from here.

## Making it a habit

The skill cannot fire itself. To make rolling handovers routine in a project, add one line to the project's instructions (`CLAUDE.md` or equivalent): "Update the handover (handover skill) at every milestone and before the conversation ends." The skill handles the rest.
