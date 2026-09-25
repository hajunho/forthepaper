<p align="right"><b>English</b> · <a href="README.ko.md">한국어</a></p>

# Program Verdicts, by Domain

> **Every verdict in this folder was drafted by an AI, and any of them can be wrong.** They apply the program translation of the T-Grade in [002_program.md](../002_program.md), which inherits the standard in [000_tier.md](../000_tier.md) — neither has been validated against human judges. A verdict grades one pinned revision of one program, never its developers. It is valid only among its neighbors in the same domain folder. It must never circulate without its three-sentence verdict. No program's code is reproduced here beyond what the reasoning cannot do without: each verdict carries a citation — repository, revision, license — and readers are expected to go there.

## How this folder is organized

Prohibition 3 makes a grade meaningful only within a domain, so the tree enforces it: **one folder per domain, and comparisons stop at the folder boundary.** There is no public, stable taxonomy of software domains equivalent to the OECD fields used by [`papers/`](../papers/README.md), so domains are added as verdicts need them, named in kebab-case, each defined by its `000_field_notes.md`.

**Field notes come first.** Every domain folder opens with `000_field_notes.md`: the normative checklist for that domain — how the five axes are read there, which defects recur there, and which verification steps are mandatory before any verdict in that folder. Field notes are the analogue of the standard's per-field axis-translation table (Chapter 2), kept as living documents: each verdict that teaches the domain something new updates them, with the change dated.

| Folder | Domain | Field notes |
|---|---|---|
| `ai-systems/` | Models, model releases, and the systems that evaluate them (benchmarks and leaderboards included) | [000_field_notes.md](ai-systems/000_field_notes.md) |
| `retrieval-systems/` | Systems that retrieve from a corpus and advise: search, RAG, question-answering over documents | [000_field_notes.md](retrieval-systems/000_field_notes.md) |

A program is filed under the domain **in which it claims its contribution**, not the domain of its most fashionable component. A program claiming two domains is judged by both field notes and filed under the primary one, with a note.

## Rules for every verdict here

1. **The notice comes first.** The fallibility notice at the top of each verdict is not optional and not a footnote.
2. **The revision is pinned.** The verdict names the commit hash (or content digest) it judged. Tags, branches, and "latest" are recorded as hints only; everything the verdict says is true of those bytes alone.
3. **The full worksheet is published**, per Appendix A of the standard, translated by 002: domain and field-notes version, claim and evidence sentences, the eight answers with reasons, the three-sentence verdict, the border flag, and the verification log — including what was executed, what was decoded, and what was scanned.
4. **The code stays out.** Repository, revision, license, identifiers, and paraphrase; quotation only where the reasoning cannot do without it and the license permits it.
5. **Secrets are never reproduced.** If the verification log finds credentials in an artifact (defect 6.5 of 002), the finding is reported to the authors privately before the verdict publishes, and the verdict names the class of the leak, never its content.
6. **Right of reply.** Authors respond through the [issue template](https://github.com/hajunho/forthepaper/issues/new/choose). Responses are appended verbatim and trigger human re-examination.
7. **Numbering is global** (`001`, `002`, …) across this folder, so a verdict can be cited by number; the folder gives the domain. `000` is reserved in every domain for its field notes.
8. **Language.** A verdict is written in English and, when the program's documentation is in another language, also in that language, as a `.ko.md` (or other code) counterpart.

## Index

| No. | Program | Folder | Grade | Border | Human review | Author response |
|---|---|---|---|---|---|---|
| — | *(no verdicts yet; the field notes above are the folder's opening state)* | | | | | |

## Proposing a verdict

Open an issue naming the program (repository, revision, license) and the domain folder you think it belongs in. Verdicts are drafted by the AI judge from the release itself — executed and decoded, not just read — and pass through the maintainer before they are merged.
