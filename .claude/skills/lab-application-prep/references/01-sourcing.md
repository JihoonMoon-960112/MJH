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

**Talks** — captions via `yt-dlp`:
```
yt-dlp --write-auto-sub --sub-lang en --skip-download --convert-subs srt "URL"
```
Then strip timestamps and dedupe. Auto-captions mangle gene names badly
(`Slc4a11` → "slick for eleven") — read around them, and never quote a gene name from
a caption as if it were verified.

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
