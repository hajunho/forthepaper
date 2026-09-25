<p align="right"><b>English</b> · <a href="README.ko.md">한국어</a></p>

# Verdicts, by Field

> **Every verdict in this folder was drafted by an AI, and any of them can be wrong.** They apply the T-Grade standard in [000_tier.md](../000_tier.md), which has not yet been validated against human judges (Appendix B of the standard). A verdict grades a paper, never its authors. It is valid only among its neighbors in the same field folder. It must never circulate without its three-sentence verdict. And the paper's own text is never reproduced here: each verdict carries a citation and identifiers, and readers are expected to read the paper itself.

## How this folder is organized

Prohibition 3 of the standard makes a grade meaningful only within a field. The folder tree enforces that: **one folder per field, and comparisons stop at the folder boundary.**

The taxonomy is the OECD *Fields of Research and Development* classification (Frascati Manual, 2015), because it is public, stable, and already used by national statistics offices. Top-level folders are the six major fields; sub-folders take the second-level names, in kebab-case.

| Folder | Major field | Sub-folder examples |
|---|---|---|
| `natural-sciences/` | Natural sciences | `mathematics`, `computer-and-information-sciences`, `physical-sciences`, `chemical-sciences`, `earth-and-environmental-sciences`, `biological-sciences` |
| `engineering-and-technology/` | Engineering and technology | `civil-engineering`, `electrical-electronic-and-information-engineering`, `mechanical-engineering`, `chemical-engineering`, `materials-engineering`, `medical-engineering`, `environmental-engineering`, `nano-technology` |
| `medical-and-health-sciences/` | Medical and health sciences | `basic-medicine`, `clinical-medicine`, `health-sciences`, `medical-biotechnology` |
| `agricultural-and-veterinary-sciences/` | Agricultural and veterinary sciences | `agriculture-forestry-and-fisheries`, `animal-and-dairy-science`, `veterinary-science`, `agricultural-biotechnology` |
| `social-sciences/` | Social sciences | `psychology-and-cognitive-sciences`, `economics-and-business`, `education`, `sociology`, `law`, `political-science`, `social-and-economic-geography`, `media-and-communications` |
| `humanities-and-the-arts/` | Humanities and the arts | `history-and-archaeology`, `languages-and-literature`, `philosophy-ethics-and-religion`, `arts` |

A paper is filed under the field **in which it claims its contribution** (Chapter 5, Case 6 of the standard), not under the field of the journal that published it. When the two differ, the verdict's Step 0 says so. A paper that claims contributions in two fields is graded by both standards and filed under the primary one, with a note.

## Rules for every verdict here

1. **The notice comes first.** The fallibility notice at the top of each verdict is not optional and not a footnote.
2. **The full worksheet is published**, per Appendix A of the standard: field and translation, claim and evidence sentences, the eight answers with reasons, the three-sentence verdict, the border flag, and the verification log.
3. **The paper's text stays out.** Title, authors, venue, identifiers, and paraphrase only. No PDFs, no extended quotation, no supplementary material belonging to the authors.
4. **Right of reply.** Authors respond through the [issue template](https://github.com/hajunho/forthepaper/issues/new/choose). Responses are appended verbatim and trigger human re-examination.
5. **Numbering is global** (`001`, `002`, …) so that a verdict can be cited by number; the folder gives the field.
6. **Language.** A verdict is written in English and, when the paper is in another language, also in that language, as a `.ko.md` (or other code) counterpart.

## Index

| No. | Paper | Folder | Grade | Border | Human review | Author response |
|---|---|---|---|---|---|---|
| [001](social-sciences/education/001_one_movie_two_perspectives.md) · [한국어](social-sciences/education/001_one_movie_two_perspectives.ko.md) | 김자미·정재림 (2023), 「하나의 영화, 서로 다른 두 시선」, *한국어문교육* 45, 167–190. [DOI](https://doi.org/10.24008/klle.2023..45.006) | `social-sciences/education` | **T6** | T6/T5 | pending | none yet |

## Proposing a verdict

Open an issue naming the paper (title, venue, DOI) and the field folder you think it belongs in. Do not attach the paper. Verdicts are drafted by the AI judge from the published full text and pass through the maintainer before they are merged.
