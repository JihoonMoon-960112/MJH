# Finding the candidate's own materials

The candidate's CV, manuscripts, drafts, figures, cover letters and past correspondence
are usually already on their machine. Find them rather than asking the candidate to
re-describe work they have already written up — their own writing is more accurate than
their recollection, and a draft in progress is invisible to any literature search.

**This step only works in a local session.** A cloud session cannot see the user's
filesystem; there, ask them to upload. Say which it is rather than searching fruitlessly.

## Ask before searching broadly

A home directory holds things unrelated to this task. Say what you are about to look for,
and prefer the narrowest scope that will work: a stated project directory, then
`~/Documents`, `~/Desktop`, `~/Downloads`, and any Dropbox/Drive/OneDrive sync folder.
Do not read files outside what the task needs, and do not open anything that looks
personal and unrelated.

## What to look for

| Target | Typical shape |
|---|---|
| **CV / résumé** | `*CV*.pdf`, `*CV*.docx`, `*resume*`, often several dated versions |
| **Manuscripts** | `*.docx` / `*.pdf` with journal names, `manuscript`, `MS`, `draft`, `revision`, `R1`, `R2`, `submitted`, `revised` in the name |
| **Preprint PDFs** | `biorxiv`, `preprint`, bare DOI-like filenames |
| **Figures** | `Fig*`, `*.ai`, `*.pptx`, `*.psd` — and the figure legend documents beside them |
| **Rebuttals** | `response to reviewers`, `rebuttal`, `point-by-point` — the most revealing document the candidate owns |
| **Cover letters** | `cover*letter*`, often one per application |
| **Thesis** | `thesis`, `dissertation`, `defense`, `proposal` |

Search by content as well as filename; people name files badly. Grep for the candidate's
surname, their gene or system names, and journal names across likely directories.

## Resolve versions

Expect five files with similar names. **Always confirm which is current with the user
before quoting from it** — writing a cover letter from a superseded draft is a silent,
expensive error. Prefer the one with the latest mtime, but verify; people copy files
and reset timestamps.

## Why the rebuttal matters most

A response-to-reviewers document is the only place the candidate has already written, in
their own words and under adversarial pressure:

- the strongest objections their work attracts
- how they answer them
- which objections they conceded
- what they could not do and why

That is most of the expected-questions section and the whole of the honest
limitation statement, pre-written. Read it before drafting anything. If the candidate has
one, it is worth more than the paper.

## Past correspondence

Earlier cover letters and application emails show the candidate's natural register and
which framings they have already used. Reuse their voice; do not reuse stale content —
a letter visibly recycled from another application is worse than a plain one.

## Feed it forward

Everything found here goes into `05-candidate-profile.md`: exact authorship positions,
accurate publication status, the competence/tool split, and the blanks that must stay
blank.
