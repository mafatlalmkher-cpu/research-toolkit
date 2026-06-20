# Research Toolkit

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20773499.svg)](https://doi.org/10.5281/zenodo.20773499)

A small family of free, single-file, browser-based tools for the research workflow,
built as companions to [QueryBee](../index.html). Every tool is one self-contained
HTML file with no build step, no account, no API key, and no server. Open the file in
any modern browser and it works, including offline.

Open `index.html` for the hub that links everything.

## The tools

| File | What it does | Network |
|------|--------------|---------|
| `index.html` | Hub / landing page linking the whole suite | offline |
| `review-tools.html` | Stage-by-stage guide to free tools for the whole review (protocol, references, full text, screening, risk of bias, meta-analysis, reporting) | offline |
| `prisma-flow.html` | PRISMA 2020 flow diagram maker; download as SVG or PNG | offline |
| `dedupe.html` | Citation de-duplicator for combined RIS / BibTeX / CSV exports (DOI + fuzzy title) | offline |
| `cite.html` | Reference formatter: DOI / PMID → APA, Vancouver, Harvard, BibTeX, RIS | Crossref + PubMed lookups |
| `screen.html` | Guide to the best free screening tools (Catchii, ASReview, Rayyan) and how to choose | offline |
| `molbio.html` | Molecular biology toolkit: reverse complement, %GC, Tm, translation, A260 quantification, ng↔pmol, oligo MW | offline |
| `qpcr.html` | qPCR/RT-qPCR: 2^−ΔΔCt and Pfaffl relative expression, primer efficiency from a standard curve | offline |
| `solutions.html` | C₁V₁=C₂V₂ dilutions, molarity↔mass, percent solutions, serial-dilution planner | offline |
| `tissue-culture.html` | Plant tissue culture: PGR stock volumes, mg·L⁻¹↔µM, stock prep, recipe scaling | offline |

## Design

Single-file by design: no dependencies beyond Google Fonts (which degrade gracefully
to system fonts when offline). The visual language matches QueryBee (warm paper palette,
Fraunces / Hanken Grotesk / JetBrains Mono). The bench calculators do all maths locally;
the reference formatter and QueryBee use only free public services (Crossref, PubMed,
OpenAlex) for metadata lookups and store nothing.

## Verification

The qPCR and dilution maths were checked against independent re-derivations (e.g. 100 ng
of 1 kb dsDNA = 0.154 pmol; a −3.32 standard-curve slope = 100% efficiency). Always
confirm critical results before relying on them for published or clinical work.

## Website / blog

This folder is also a small static website (a blog with a downloads page) so the tools
can be published and downloaded from one place:

- `index.html` — home, with the tools grid and an articles list
- `review-tools.html`, a guide to the best free tools for every stage of a review
- `downloads.html` — use-online and download links, plus a single ZIP of all tools
- `about.html` — mission, citation, and how to host your own copy
- `posts/` — a short page for each tool, plus how-to guides
- `assets/blog.css` — shared styles for the blog pages (the tools stay self-contained)
- `research-toolkit-tools.zip` — all tools bundled for offline use

See `DEPLOY.md` for free GitHub Pages publishing steps.

## Licence

MIT, the same as QueryBee. Copy it, host it, adapt it, translate it.
