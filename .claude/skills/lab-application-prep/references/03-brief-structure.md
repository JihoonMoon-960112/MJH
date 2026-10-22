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
