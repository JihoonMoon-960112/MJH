# Acquiring full text

The default failure of this whole workflow is reading abstracts and believing you have
read the paper. Budget real effort here.

## What to collect

1. **Last ~5 years of the lab's output**, weighted to the last 2.
2. **Preprints** — bioRxiv/medRxiv/Research Square. These are where the lab's *current*
   direction lives; the published record is 18 months stale.
3. **The PI's own first-author papers** from their postdoc and PhD. Routinely missed.
   A PI's first-author work tells you what they personally find interesting, which is
   often not what the lab's recent output looks like. Missing one can lead you to give
   flatly wrong advice about what a PI cares about.
4. **Recent talks** — YouTube, institutional seminar series, conference recordings.
   Abstracts of upcoming talks are especially valuable: they state claims the papers
   have not yet made.
5. **Adjacent labs** — direct competitors and frequent collaborators. Their newest
   papers constrain what the target lab can still claim as novel, and sometimes reveal
   what the target lab is racing on.

## How to get it

Try in this order; stop when you have main text + legends + methods.

**Europe PMC** — best single source, has full text for much of PMC-indexed work:
```
https://www.ebi.ac.uk/europepmc/webservices/rest/search?query=AUTH:"Lastname F"&format=json&pageSize=100
https://www.ebi.ac.uk/europepmc/webservices/rest/{SRC}/{ID}/fullTextXML
```

**NCBI E-utilities + BioC** — for PMC IDs:
```
https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=...&retmode=json
https://www.ncbi.nlm.nih.gov/research/bionlp/RESTful/pmcoa.cgi/BioC_xml/{PMCID}/unicode
```

**PMC article page** — when the XML route is empty, the rendered page often still has it.

**bioRxiv** — aggressively rate-limits. Expect HTTP 429. Use exponential backoff
(2s, 4s, 8s, 16s) and do not parallelise requests to the same host. The `+full` and
`.full-text` URL suffixes reach the reading view.

**PDFs the user supplies** — the most reliable route for paywalled work. Ask for them.
```
pdftotext -layout input.pdf output.txt
```
`-layout` matters: without it, multi-column figure legends interleave into nonsense.

## Talks and news — finding them, not just downloading them

A recent talk is often the single most current statement of a lab's direction, more
current than any preprint. Look for them deliberately; they do not surface from a paper
search.

**Where to search**

- **YouTube** — search the PI's name alone, and the name plus their central concept.
  Then check the institutional channels directly, because many talks are never titled
  with the PI's name: the host institute, the cancer centre, CSHL/Keystone/Gordon
  meeting channels, society channels (AACR, AACR/ASCO, EMBO), and seminar series
  channels at other universities that invited them. A PI gives roughly the same talk at
  four places in a year; any one recording will do.
- **iBiology, Cell/Nature video abstracts, journal podcasts** — short but tightly edited,
  so the framing is the PI's most considered version.
- **Institutional seminar listings and upcoming-talk abstracts.** An abstract for a talk
  they have not yet given is the highest-value document you can find: it states claims
  the published record does not yet support. Compare it line by line against the papers —
  the delta is unpublished work.
- **Recorded conference sessions** behind a society login are usually unreachable. Note
  and move on.

**News about the PI** — check for these; they change what the interview is about:

- New faculty hires, lab moves, or a new joint appointment
- Recently awarded grants (NIH RePORTER is searchable by PI name and gives the
  *abstract and specific aims* of funded but unpublished work — one of the best
  sources for "what are they about to do")
- Awards, named chairs, editorial roles
- Company founding, SAB membership, licensing — tells you which findings they believe
  are translatable
- Recent retractions or corrections anywhere in the lab's output. Rare, but you must not
  walk into an interview unaware of one.

**Extracting a talk** — captions via `yt-dlp`:
```
yt-dlp --write-auto-sub --sub-lang en --skip-download --convert-subs srt "URL"
```
Then strip timestamps and dedupe. Auto-captions mangle gene names badly
(`Slc4a11` → "slick for eleven") — read around them, and never quote a gene name from
a caption as if it were verified.

**Mine the Q&A.** The question period is where a PI says what they would never write:
what did not work, what they are unsure of, what a competitor has wrong. Extract the
questions and answers separately from the talk body and read them as their own document.
Note the timestamp of anything you plan to use.

If the user supplies a video link, use it — but still search independently. They will
have found the obvious one.

## Handling what you cannot get

Some things are genuinely unreachable: internal seminar pages, members-only abstracts,
institutional intranets. When a URL 404s or is gated:

1. Try the Wayback Machine (`http://archive.org/wayback/available?url=...`).
2. If that fails, **mark it unverifiable and remove it from the argument.**

Do not leave an unopened page in a citation table. If the user asks "how did you find
that?" — and they will — the honest answer must be available.

## Organising it

Put converted text in a scratch directory, one file per paper, with short stable names.
Keep a manifest mapping `filename → citation → how acquired → verification level`.
You will re-grep these files many times; make that cheap.

Grep aggressively for the tells in `02-gap-analysis.md` rather than re-reading linearly.
