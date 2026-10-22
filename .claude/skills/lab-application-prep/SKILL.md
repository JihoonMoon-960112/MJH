---
name: lab-application-prep
description: Prepare a postdoc/PhD application to a specific lab — recruiter email, cover letter, and a night-before interview brief as an HTML artifact. Use when the user names a PI or lab they are applying to, interviewing with, or emailing, or asks to prepare for an academic interview, draft a cover letter to a professor, or research what a lab is working on next. Reads the full text of the lab's recent papers and preprints (never abstracts alone), then derives what the lab is trying to do, what it currently cannot do, and where the candidate fits.
---

# Lab application prep

Produce three artefacts for one target lab: **correspondence** (email threads with the PI
and their assistant), a **cover letter**, and a **night-before interview brief** published
as an HTML artifact.

The brief is the centre of gravity. The letter and the emails are downstream of the same
research. Do the research once, properly, and all three get easier.

## The one rule that overrides everything

**Never propose applying the candidate's own prior tool or system to the target lab's
research.** Not in the letter, not in the brief, not as a question, not as a "this could
be useful for" aside.

It reads as a sales pitch, it presumes the PI has not thought about their own problems,
and it is the single fastest way to sound like a technician looking for a host rather than
a scientist choosing a question. The candidate's prior work belongs in exactly two places:
a one-line statement of what they built, and an honest statement of where it breaks.

If the connection is real, **the PI will draw it themselves** — and when they do, it is
their idea, which is worth far more. Prepare the candidate to be ready for that moment,
not to manufacture it. Teach them to stop talking and let the silence sit.

## Workflow

Run these in order. Steps 1–3 are research; do not start writing until they are done.

### 1. Build the candidate profile

**Find the candidate's own materials first.** In a local session, locate their CV,
manuscripts, drafts, figures, rebuttals and past cover letters on disk rather than asking
them to re-describe work they have already written. A response-to-reviewers document, if
one exists, is worth more than the paper: it is the expected-questions section already
written under adversarial pressure. Scope, version resolution and what to search for:
`references/06-local-materials.md`. In a cloud session the filesystem is not visible —
say so and ask for uploads.

Then read the CV in full before anything else. Get the authorship positions **exactly
right** — sole first, co-first (marked `*`), and middle author are three different things
and conflating them is a credibility-destroying error in a document the PI will read
alongside the CV. Publication status (published / in press / under review / preprint) must
match reality, not optimism.

Record what is theirs to claim and what is not. See `references/05-candidate-profile.md`.

### 2. Acquire the lab's corpus — full text, not abstracts

Identify every paper and preprint from the lab in roughly the last five years, weighted
toward the last two, **plus the PI's own first-author papers from their training years**.
Those last ones are routinely missed and they are where the PI's actual scientific
instincts live.

Then read them. **Main text, figure legends, extended data, methods.** An abstract tells
you the claim; only the legends tell you the n, the model, the timepoint, and the caveat —
and the caveat is where the interview happens.

**Search independently for talks and news**, do not wait to be given links. A recent
seminar is often more current than any preprint, and an abstract for a talk not yet given
states claims the papers do not support — that delta is unpublished work. Check NIH
RePORTER for funded-but-unpublished aims, and check for lab moves, new grants, company
founding and any corrections. Mine the Q&A separately from the talk body: it is where a
PI says what they would never write.

Acquisition playbook, talk and news discovery, rate-limit handling, PDF and caption
extraction: `references/01-sourcing.md`.

### 3. Derive the gap map

This is the analytical core and the part the user explicitly asked for. From the full text,
derive four things:

| | Question | Where the evidence lives |
|---|---|---|
| **Wants** | What is the lab trying to establish next? | Discussion final paragraphs, "future directions", grant-style framing in talks |
| **Cannot** | What can they not currently do? | Methods workarounds, acknowledged limitations, clonal lines made to rescue a failing allele |
| **Unproven** | What is claimed but not shown? | "consistent with", "suggests", one organ's result generalised to two |
| **Fit** | Where could this candidate contribute? | Intersection of Cannot/Unproven with the candidate's *demonstrated competence* — not their tools |

The full method, with the textual tells that mark each category:
`references/02-gap-analysis.md`.

A gap map with no "Cannot" row is a sign you read abstracts. Go back to step 2.

### 4. Build the brief

Publish an HTML artifact. Structure, section order, source-grading scheme and layout
constraints: `references/03-brief-structure.md`.

Non-negotiables:
- **Bilingual by function, not by section.** What the candidate *reads* goes in their own
  language; what they will *say or send* goes in English, verbatim-ready, with no
  translation beneath it. Full rule in the reference.
- Every factual claim carries a **source grade**: full-text verified / abstract only /
  my inference. Three visually distinct levels.
- Questions the candidate will actually ask out loud get a figure-level citation —
  but the brief should say plainly that **they rarely need to say the figure number out loud.**
  The citation is there so they can withstand a follow-up, not so they can perform.
- A time-boxed "tonight" checklist at the very top.
- Question sheets go in collapsible `<details>` with one-line headlines. A sheet that
  scrolls for three screens is unusable at 6am.

### 5. Write the correspondence and the letter

Correspondence and the letter are **English only** — they are sent, not read. Any
commentary you attach about them (why a line is phrased that way, what to cut) goes in the
candidate's own language, clearly separated from the text they will send.

Register rules, time-zone notation, the no-flattery rule, apology and reschedule handling,
and the recommendation-letter conversation: `references/04-correspondence.md`.

## Standing discipline

**Never cite a source you did not open.** A search-result snippet is not a source. If a
page 404s or is paywalled, check the Wayback Machine, and if that fails, record it as
*unverifiable* and remove it from the argument. Do not let it sit in a table looking
like evidence. The user may ask how you found something — be able to answer.

**Re-read the primary material before building an argument on it.** If the user shares an
email thread, read the whole thread before drafting a reply; a script built on a question
that was already asked and answered is worse than no script.

**Correct errors in place and move on.** When the user catches a factual error — an
authorship position, a missed paper, a misread figure — fix it, state the correction in one
line, and continue. Do not perform contrition.

**Leave the candidate's own blanks blank.** The specific failure mode of their own work,
their personal reason for wanting this lab, their account of a difficult advisor
relationship — mark these as `[in my own words]` and do not invent them. Inventing them
produces answers that collapse under one follow-up question.
