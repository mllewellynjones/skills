---
name: cv-review
description: Run a structured CV critique for a client, producing a written section-by-section, bullet-by-bullet assessment with verdict labels and rewrite suggestions. Use this skill whenever the user is reviewing someone's CV, asks for CV feedback, or is helping a client improve their application materials — even if the request is phrased casually ("take a look at this CV", "what do you think of her CV", "help me fix this", "can you review this for me").
---

# CV Review

A structured methodology for critiquing CVs, producing a written critique with verdict labels
and rewrite suggestions for every bullet. Default output is a Markdown artifact. Offer to
convert to .docx at the end, or proceed directly if the user requests it upfront.

---

## Step 1: Intake

Before reviewing, ask for the following. Accept partial answers — gaps inform the critique.

1. **Target role/sector:** What role or sector is this CV aimed at? Accept "don't know" or
   "undecided" as valid — this changes the lens applied (see Step 2).

2. **Primary market:** Which country/market will this CV be submitted in primarily? Are there
   secondary markets to consider? This affects formatting norms, personal details conventions,
   and language calibration (see Jurisdiction norms below).

3. **What is this person trying to achieve?** A lateral move, a step up, a sector change, a
   return from a gap, a first role — each requires different framing of the same career history.
   This is the most important intake question.

4. **Purpose of this review:** Specific live application, general refresh, or exploratory?
   This determines how hard to push on tailoring.

Do not infer seniority or years of experience from the intake — read them from the CV itself.
If the CV fails to make seniority legible, that is feedback on the CV.

---

## Step 2: Select the lens

### If target role/sector is known
Apply all nine scoring criteria (see Step 3) plus a **specialist lens** — flag where the CV
should emphasise domain credentials, technical depth, or sector-specific language that the
generalist criteria don't capture.

### If target role/sector is unknown
Apply the nine generalist criteria only. Note explicitly in the output that tailoring and the
specialist lens should be revisited once direction is clearer. Goal: a strong sector-agnostic
CV that can be sharpened later.

---

## Step 3: Scoring criteria

Score each criterion 1–5. Scoring is **relative to the candidate's seniority level** — a
bullet that would be impressive at mid-level may be unremarkable at Director or C-suite level,
and vice versa. Always ask: *is this impressive for someone at this level, in this field?*

**Structure (15% of total)**

- **Layout & presentation (8%)** — formatting consistency; ATS compatibility (single column
  layout is essential — two-column layouts are frequently mangled by ATS parsers and should
  be flagged); appropriate length for seniority; ease of skim-reading; no text boxes, tables
  used for layout, or content buried in headers/footers
- **Language & tone (7%)** — active verbs; consistent tense; no clichés; no errors

**Content (85% of total)**

- **Professional summary (10%)** — punchy, tailored, leads with strongest material, no filler
- **Impact & quantification (22%)** — achievements numerical where possible; specific and
  credible; targets clearly labelled as targets, never presented as achievements; numbers
  calibrated to seniority (£200k is notable for a team leader, unremarkable for a Head of)
- **Personal ownership (18%)** — "I" not "we"; individual contribution unambiguous; no
  "co-led", "played key role", or "we delivered" without a clear statement of personal scope
- **Editorial focus (18%)** — fewer stronger bullets over comprehensive coverage; older/less
  relevant roles condensed; no padding; the most impressive material is most prominent
- **Excellence (17%)** — at least one or two moments that are genuinely exceptional and
  specific to this person; something a reader pauses at; see Excellence Benchmarks below
- **Career narrative (5%)** — does the CV tell a legible story? Is there a thread a reader
  can follow across roles? Especially important for career changers, returners, or anyone
  undecided on direction
- **Tailoring & relevance (5%)** — CV speaks to the specific role; keywords aligned; most
  relevant experience foregrounded. If target role is unknown, score on internal coherence
  instead.

*Note: career narrative and tailoring are lower-weighted but must still be assessed in detail
— a weak score on either warrants specific, actionable feedback.*

### Score descriptors
- 1 — Absent or actively harmful
- 2 — Present but weak; significant problems
- 3 — Adequate; does the job but misses opportunities
- 4 — Strong; clear and effective
- 5 — Exceptional; this criterion is a positive differentiator

### Verdict bands
- 42–50: Outstanding — interview-ready
- 35–41: Strong — minor refinements only
- 25–34: Solid with gaps — good foundations, key criteria need work
- 15–24: Needs significant work — structure may be fine, content too weak
- Below 15: Not ready — fundamental rework needed

---

## Step 4: The 30-second test

Before the section-by-section critique, run this test explicitly and report the result.

A recruiter at a top-tier firm decides whether to read further within 30 seconds. In that
window they look at: current title and employer, the most recent role headline, one or two
numbers that catch the eye, and whether the career reads as upward. Ask:

1. **Is the current title immediately legible?** Not buried, not vague.
2. **Is there at least one strong number visible in the top half of page one?**
3. **Do the employer names carry weight, or are they clearly contextualised?** An unknown
   employer with no descriptor leaves the reader guessing.
4. **Does each role have a one-line context setter before the bullets?** What the company
   does, scope of the role, size of team/budget. A reader should not have to infer this.
5. **Does the career read as upward?** Titles, responsibilities, and scope should suggest
   progression. Anything that breaks that read needs to be explained or reframed.
6. **What would a recruiter conclude about this person in 30 seconds — and is that the right
   conclusion?** State the likely conclusion explicitly. If it's wrong, say what's causing
   the misread.

---

## Step 5: Red flags

Before the section-by-section critique, scan for and report on the following. For each flag,
apply the guidance below — it is not useful to identify a flag without advising how to
address it.

**Short tenures (under 18 months)**
Flag but don't condemn. Advise: add a brief context clause if there's a legitimate reason
(contract role, redundancy, company folded, health). If no context is available, consider
whether the role is worth including at all — or whether date formatting (year only, not
month/year) reduces the visual prominence of the gap.

**Employment gaps**
Same as above. Gaps are more acceptable post-pandemic and for caregiving. Advise: a short
parenthetical in the role list ("career break — caregiving / health / travel") is better
than silence. Silence invites the worst interpretation.

**Frequent employer changes**
More than three employers in five years warrants a note. Advise: if the pattern is genuine
career acceleration, the increasing seniority should be visible and should explain it. If
it isn't, the CV needs restructuring to lead with achievements not job-hopping.

**Downward title moves**
A step down in title — even for good reasons (joining a startup, sector change, family) —
reads badly without context. Advise: add scope context that reframes the level of the role
regardless of title, and/or address it in the cover letter.

**Unexplained sector or function jumps**
A reader who can't connect the dots will fill the gap with doubt. Advise: the professional
summary should carry the thread explicitly — "Having spent X years in Y, now applying that
to Z" — so the reader isn't left wondering.

**Stale or junior content at the top**
Older roles, junior responsibilities, or early-career content appearing too early. Advise:
restructure so seniority and recency lead.

---

## Step 6: Jurisdiction norms

Adjust feedback based on primary market. Flag jurisdiction-specific issues explicitly.

**UK**
- Photo: not standard, not expected, potentially problematic
- Date of birth / nationality / marital status: not required, inadvisable
- Full home address: city and county/region is sufficient; full address is unnecessary
- Length: 2 pages standard for most roles; 1 page for early career; academic CVs longer
- "CV" not "resume"

**US**
- Photo: do not include
- Date of birth / nationality / marital status: do not include — legal exposure for employer
- Full address: city and state only
- Length: 1 page junior, 2 pages senior; longer only for academic/research
- "Resume" not "CV" (flag if document is titled "CV" for a US application)

**Germany / DACH**
- Photo: expected and standard — flag if missing
- Date of birth: standard to include
- Nationality: commonly included
- Lückenloser Lebenslauf: gaps are more scrutinised than in UK/US — advise explicit coverage

**Poland / CEE**
- Photo and date of birth: commonly included
- Consent clause for data processing: standard in Polish CVs (RODO/GDPR boilerplate at foot)
- Flag if missing for a Polish market submission

**Secondary markets**
If secondary markets are flagged in intake, note what would need to change for each —
typically personal details conventions and length norms.

---

## Step 7: Sector and seniority adjustments

Apply on top of baseline criteria.

**Consulting / professional services:** Ownership and excellence weighted most heavily.
Quantification expected on almost every bullet. Generalist criteria apply fully.

**Financial services / regulated industries:** Regulatory fluency and compliance outcomes
are a de facto additional criterion. Flag missing regulatory context as a gap.

**Technical / engineering / clinical:** Specialist credentials may outweigh excellence and
ownership. Add a specialist lens pass: are the right tools, languages, certifications, or
domain achievements present and prominent?

**Academic / research:** Publications, citations, and grant funding are primary excellence
signals. Ownership conventions differ — collaborative attribution is normal; adjust the
ownership criterion accordingly.

**Public sector / non-profit:** Impact may be harder to quantify; proxy measures (reach,
policy outcomes, service users, budget managed) should be encouraged. Ownership language
norms differ.

**Career changers or undecided:** Prioritise career narrative above tailoring. The thread
connecting roles matters more than keyword alignment at this stage.

---

## Step 8: Section-by-section critique

### Overall assessment
Open with 3–5 sentences: overall quality, the one or two most urgent issues, and what
the CV does well. Be direct. Do not soften findings that need to be acted on.

### Score summary table
Present scores for all nine criteria with a weighted total and verdict band.

### Sections to cover, in CV order
- Header
- Professional summary / executive summary
- Each role in professional experience (in CV order)
- Skills section (if present)
- Education and certifications
- Any additional sections

For each section, open with a 2–3 sentence section-level assessment before going
bullet by bullet.

### Bullet-by-bullet format

For every bullet point and every role intro paragraph, apply a verdict label:

- **KEEP** — strong as-is; at most a minor tweak noted
- **STRENGTHEN** — good bones but needs a metric, tighter ownership, or more specificity
- **REWRITE** — fundamental problem with framing, ownership, or accuracy
- **CUT** — adds no signal; dilutes the CV
- **RESTRUCTURE** — content is right, placement or structure is wrong

Format per bullet:
```
Original: [exact text]
Verdict: [label]
Critique: [specific, honest — what's wrong and why]
Suggested rewrite: [revised version with [placeholders] for numbers client needs to supply]
— omit suggested rewrite if verdict is KEEP or CUT
```

---

## Step 9: Priority action list

Close the critique with a ranked list of 5–8 actions, most impactful first.
Format: **action** / *why it matters*

---

## Step 10: Excellence benchmarks (end of session)

At the end of each review session, assess whether any bullets from this CV are strong
enough to serve as benchmark examples for the excellence criterion. Propose specific
additions in this format:

```
Proposed excellence benchmark addition:
Level: [junior / mid / senior / executive]
Sector: [sector if sector-specific, or "general"]
Example: [the bullet text]
Why it qualifies: [one sentence]
Suggested addition to SKILL.md: [exact text to paste into the Excellence Benchmarks
section below]
```

Present this to the user and wait for confirmation before treating it as adopted.

---

## Excellence Benchmarks

*This section grows over time. Each entry is a real example of a 5/5 excellence bullet,
anchored to level and sector.*

*(No benchmarks yet — will populate after first review sessions.)*

---

## Key principles

- **Be direct.** A critique that softens every finding is not useful.
- **Targets are not achievements.** Any bullet presenting a future goal as a delivered
  result must be flagged REWRITE.
- **"I" not "we."** Every instance of diffused ownership is a problem, though the
  correction may be gentler in collaborative cultures (academic, public sector).
- **The strongest material should be most prominent.** If the best achievement is at
  bullet 8 of 9, say so.
- **Numbers are almost always available.** If a bullet lacks quantification, assume the
  number exists and hasn't been surfaced — not that it doesn't exist. Prompt for it.
- **Seniority calibration is mandatory.** Always ask: is this impressive for someone
  at this level? A modest number that would be strong for a team leader is weak for
  a Head of.
- **Red flags need remedies.** Never flag a structural problem without advising how to
  address it.
