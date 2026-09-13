---
name: skills-sync
description: Keep the mllewellynjones/skills GitHub repo in sync with the user's locally installed Claude skills. Use whenever the user says "sync my skills", "diff my skills against the repo", "push my skill changes", "update the skills repo", "is the skills repo up to date", or after any edit to a skill that is published in the repo.
---

# Skills sync

The GitHub repo is the source of truth for published skills; locally installed copies (claude.ai uploads) drift. This skill diffs and reconciles the two.

## Repo facts

- Repo: `mllewellynjones/skills` (public), branch `main`
- Marketplace name: `mllewellynjones-skills`, defined in `.claude-plugin/marketplace.json`
- Layout: `plugins/<name>/.claude-plugin/plugin.json` and `plugins/<name>/skills/<name>/SKILL.md`
- `README.md` carries a prose summary per skill; `ROADMAP.md` carries what's planned next
- A GitHub Action rebuilds one zip per skill into the rolling **latest** release on every push touching `plugins/` — those zips are how claude.ai users install and update
- The published list is whatever `marketplace.json` names. Anything installed locally but not listed there is **private by default** — never publish a new skill without explicit confirmation, and never mention private skills' contents in public files

## Sync procedure

1. **Read local copies.** In a chat environment, installed skills live under `/mnt/skills/user/` and `/mnt/skills/plugins/`.
2. **Fetch published copies** of each skill listed in `marketplace.json` via the GitHub connector.
3. **Diff and classify** each difference by direction:
   - **Repo ahead** (the published copy was edited or sanitised after upload): the user's claude.ai copy is stale — point them at the skill's zip in the latest release to re-upload. Do not "fix" the repo back to the local wording: published sanitisations are deliberate.
   - **Local ahead** (the user edited their installed copy): propose a push, showing the delta first.
4. **Privacy pass before any push** — the standing rule of this repo. Strip or replace: personal names, employer/client/tool/project names, figures traceable to real work (round or alter them), and references to the user's personal stack or self-disclosures. Where a sanitisation would gut the content, flag it and ask rather than push.
5. **On every pushed change:** bump the version in both the skill's `plugin.json` and its `marketplace.json` entry (patch for edits, minor for new capability) — installed Claude Code users only receive updates when the version string changes — and refresh the skill's README summary if behaviour changed.
6. **Report**: what differed, what was pushed, and what the user still needs to do by hand (claude.ai re-uploads).

## Adding a new skill

Follow the one-at-a-time ritual: read the local skill in full; flag anything personal or identifying with proposed fixes; agree edits with the user; then publish as a new plugin (folder + plugin.json + marketplace entry + README summary), and remove it from ROADMAP.md if listed there.

## Known limits

- claude.ai has no skills API: uploading to it is always a manual click. This skill minimises drift; it cannot eliminate that step.
- In a chat environment the GitHub connector cannot create repositories or write workflow files — those need the GitHub web UI.
