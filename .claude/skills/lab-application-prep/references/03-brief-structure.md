# The interview brief

One HTML artifact, published via the Artifact tool. The candidate reads it the night
before and glances at it during the call. Design for 6am, under stress, on a laptop
next to a Zoom window.

Load `artifact-design` before writing it, and `artifact-diagramming` if you will draw
schemes.

## Section order

Priority order, not narrative order. The things needed soonest go first.

| # | Section | Contents |
|---|---|---|
| 00 | **Tonight** | Time-boxed checklist. 3–5 items, each with a minute budget. Nothing else. |
| 01 | **One page to carry into the call** | Opening script; the candidate's publication table with exact authorship; a numbered list of what the PI is likely to say so none of it is a surprise |
| 02 | **Questions I will ask** | Collapsible. One-line headline per question; expanded body holds the full wording plus the evidence block |
| 03 | **Questions I expect** | Answers in the candidate's voice, with blanks left blank |
| 04 | **How the lab works** | Models, systems, reagents, people. Schemes here |
| 05 | **Paper trajectory** | Chronological, starting with the PI's own first-author work |
| 06 | **Established / open / what they want** | The gap map |
| 07 | **Adjacent labs** | What constrains or races them |
| 08 | **Shared ground** | Overlap between the candidate's current lab and the target |
| 09 | **Talks** | What the PI said recently, with dates |

## Two languages, one rule

The brief is bilingual, and the split is **not** by section — it is by **what the
candidate does with the sentence**.

| | Language | Why |
|---|---|---|
| Anything they **read** — analysis, context, reasoning, source grades, the gap map, your warnings, scheme labels in prose, the tonight checklist | **The candidate's own language** (Korean by default here) | Read at speed, under stress, at 6am. Comprehension per second is what matters, and that is highest in their first language |
| Anything they will **say or send** — opening script, the questions they will ask, answers to expected questions, email and letter text, phrasings to have ready | **English, verbatim-ready** | It must be usable as-is, with no translation step |

**Do not provide a translation of the spoken parts.** A Korean gloss under an English
question invites the candidate to think in Korean and translate live, which is slower and
produces stilted phrasing under pressure. Give the English only. If a phrase is genuinely
hard, explain the *difficulty* in Korean next to it — nuance, register, what it implies —
but leave the line itself English and alone.

**Explanation about an English line stays in the candidate's language.** "Say this
plainly, don't soften it" is reading material. The line it refers to is speaking material.
Keep them visually distinct — different weight, a left rule, or a label — so the eye never
has to ask "am I reading this or saying this?"

**Technical terms stay English inside Korean prose.** Write `HPCS가 quiescent하다`, not a
translated coinage. The candidate will say the English term in the call, and inventing a
native-language equivalent in the brief creates a word they must then translate back.

If the user asks for a section to be converted, convert it fully — a half-translated
question sheet is worse than either language alone.

## Source grading — mandatory

Every factual claim is marked at one of three levels, visually distinct:

- **Full text verified** (green) — main text, legend, extended data, or methods read directly
- **Abstract only** (amber) — claim read, body not obtained
- **My inference / candidate's own documents** (garnet) — reasoning, not a quotation

Put the grade next to the claim, not in a footnote. The candidate must be able to tell
at a glance how hard they can lean on a sentence in conversation.

State explicitly in the brief: **"You almost never need to say a figure number out loud."**
The figure-level citations exist so the candidate can survive a follow-up, not so they can
recite. Reciting figure numbers sounds rehearsed and invites a test.

## Layout constraints

- **Collapsible question sheets.** `<details>` with a one-line `<summary>`. A sheet that
  runs three screens tall cannot be used during a call.
- **Tables over prose** for anything comparative.
- **Inline SVG schemes** for mechanism. A PI's model is usually a flow between states or
  compartments; draw that, with the real labels, legible in both light and dark themes.
- Dark-mode tokens on `:root`, as the artifact design skill requires.

## Questions: the evidence block

Each question the candidate will actually ask carries a small block:

```
Source   Nature 2026, Fig 3e + ED Fig 7c-f        [full text verified]
Claim    Ki-67 9.1±2.7% (3d) → 15.1±1.8% (14d) in exited cells;
         no S-phase length difference
Why      Separates cycle re-entry frequency from cycle speed —
         the paper does not make this distinction explicitly
```

The `Why` line is what makes the question land. A question with a citation but no `Why`
is trivia.

## What to leave out

- Anything applying the candidate's prior tool to the lab's work. See the skill's primary rule.
- Background the candidate already knows. The brief is not a textbook.
- More than six questions. They will get through two or three in thirty minutes.
