<p align="right"><b>English</b> · <a href="README.ko.md">한국어</a></p>

# For the Paper

**A ruler whose unit is the work itself — the paper, and now the program — and the verdicts produced by using it.**

[![License: GPL-3.0](https://img.shields.io/badge/license-GPL--3.0-blue.svg)](LICENSE)
[![Verdicts](https://img.shields.io/badge/verdicts-1-informational.svg)](papers/README.md)
[![AI-drafted](https://img.shields.io/badge/verdicts-AI--drafted%2C%20can%20be%20wrong-orange.svg)](#the-ai-judge-and-its-limits)

> **Read this first.** The verdicts in this repository were drafted by an AI applying a standard that has not yet been validated against human judges. **Any of them can be wrong.** A verdict grades a paper, never a person. It is meaningful only within its field. It must never circulate without its three sentences. Authors of evaluated papers have a standing right of reply. And no paper's text is reproduced here: verdicts cite, they do not copy.

This repository holds two things, kept apart.

1. **The standard.** [*The Weight of a Paper*](000_tier.md) sets out the **T-Grade**: seven tiers, T7 to T1, for grading a research paper by reading it, independent of where it was published. It was written by Claude, an AI language model, and by its own scale it grades itself T6, an unverified pilot. A Korean edition is at [000_tier.ko.md](000_tier.ko.md). Two companions extend it: [*The Proxy Atlas*](001_proxy_atlas.md), the evidence file behind its critique of venue metrics, and [*The Weight of a Program*](002_program.md), the same standard translated for software artifacts — documentation as the claim, the running bytes as the evidence.
2. **The verdicts**, in [`papers/`](papers/README.md), sorted by field, and in [`programs/`](programs/README.md), sorted by domain, where each domain opens with its own field notes. Each verdict applies the standard's judging procedure to one published paper or one pinned program release and is published with its complete worksheet so that it can be checked, disputed, and corrected. They are the beginning of the standard's verification, one work at a time.

---

## Why grade papers by reading them?

Every instrument academia already uses measures something other than the paper. The impact factor measures the journal. The h-index measures the researcher. Citation counts measure a paper's position in a network. Conference tiers and journal lists measure the height of a gate, not the spread of what passed through it. Each is a proxy, and proxies decay under Goodhart's law once they become targets.

A direct measure has always been possible in principle and unaffordable in practice: to grade a paper you have to read it, and expert reading time is the scarcest resource in research. The standard's premise is that this cost has collapsed, and that the bargain struck in the age of proxies is due for renegotiation. The T-Grade is one proposal for what a reading-based standard could look like.

## The T-Grade at a glance

### Seven tiers

| Grade | Name | Essence | Deciding axis |
|---|---|---|---|
| T7 | Record | Prior to verifiable form | (n/a) |
| T6 | Pilot | Idea plus minimal demonstration | Novelty alone lit |
| T5 | Full Proceedings | Complete narrative, limited verification | Completeness |
| T4 | Sound Study | No fatal defect | Rigor, claim within evidence |
| T3 | International Standard | Interoperable verification | Quantitativeness, reproducibility |
| T2 | World-Class | Recognition at the frontier | Novelty, consequence |
| T1 | Paradigm | Replacement of the question | Judged by time, never assigned |

From T6 to T4 a paper climbs by filling in verification. From T4 to T2 it climbs by filling in novelty. Diagnosing *which* deficiency a paper has is the practical value of grading at all.

### Five axes

**Novelty** (what would the world not know without this paper, and at which layer: problem, method, combination, or confirmation). **Rigor** (does the conclusion follow from the evidence inside the paper, and does the claim stay within the range of the evidence). **Quantitative evidence** (has judgment been converted into measurement; in qualitative fields, read as *systematicity of evidence*). **Reproducibility** (could a third party arrive at the same result from the paper alone). **Consequence** (if the conclusion is true, can the next study be built on it; judged at reading time, not by citations). Chapter 2 of the standard has a table translating each axis for four kinds of field.

### The eight questions

Answered yes / partial / no, after reading the paper backwards: conclusion first, then evidence, then method, and the introduction last, so the author's framing does not hide the gap between claim and evidence.

1. Do the ranges of claim and evidence coincide?
2. Does evidence exist independent of the author's impressions?
3. Do comparisons exist, and are they fair?
4. Is the information for third-party reproduction complete?
5. Is what is new specified against the related work?
6. At which layer is the novelty: problem, method, combination, or confirmation?
7. Is the verification interoperable with international standards?
8. Can the next study be built on this conclusion?

### From answers to grade

Each "no" among questions 1–4 counts one point of deficit and each "partial" half a point. A deficit of 3 or more means T7 or T6. Between 1.5 and 3 means T6 or T5, and T5 requires both a statement of limits and at least one independently reported quantity. Below 1.5 with question 7 "no" means T5 or T4, and T4 requires no "no" at all and no claim overreach. Questions 1–5 and 7 "yes" means T3. T3 plus problem- or method-layer novelty plus question 8 "yes" means T2. T1 is never assigned; it is withheld and left to time. Where the count and the tier definitions disagree, the definitions win and the verdict says so.

### The three-sentence verdict

A grade thrown down without reasons is not a judgment. Every verdict states **the grade**, **the axis that decided it**, and **the deficiency that separates the paper from the next step up**. The third sentence is the reason the system exists: a grade must be a diagnosis, not a rank.

---

## Contents

| Path | What it is |
|---|---|
| [000_tier.md](000_tier.md) | *The Weight of a Paper*, the standard. Revised edition, September 2026. English. |
| [000_tier.ko.md](000_tier.ko.md) | The standard in Korean. |
| [001_proxy_atlas.md](001_proxy_atlas.md) | *The Proxy Atlas*, a companion to the standard: the five families of venue metrics, their two ruptures on record, and the disciplines for citing venue context in a verdict. English. |
| [001_proxy_atlas.ko.md](001_proxy_atlas.ko.md) | The atlas in Korean. |
| [002_program.md](002_program.md) | *The Weight of a Program*: the T-Grade translated for software artifacts, with the defect catalog for the gap between documentation and bytes. English. |
| [002_program.ko.md](002_program.ko.md) | The program translation in Korean. |
| [papers/](papers/README.md) | Paper verdicts, one folder per field, following the OECD Fields of Research and Development classification. The folder's own README explains the taxonomy and the rules every verdict must meet. |
| [programs/](programs/README.md) | Program verdicts, one folder per domain, each domain opening with its normative field notes (`ai-systems/`, `retrieval-systems/` so far). The folder's own README explains the rules. |
| [README.ko.md](README.ko.md) | This guide in Korean. |
| [.github/ISSUE_TEMPLATE](.github/ISSUE_TEMPLATE) | Template for author responses and correction requests. |

**Verdicts so far:** 1 paper verdict, in 1 field (`social-sciences/education`); no program verdicts yet — `programs/` opens with its field notes. The indexes are in [papers/README.md](papers/README.md#index) and [programs/README.md](programs/README.md#index).

---

## Ground rules

These are the standard's own prohibitions (Chapter 6). They are part of the system, not an afterthought, and this repository applies them to everything it publishes.

- **Papers, not people.** A T-Grade is a snapshot of one paper. A researcher is a trajectory. Every strong research career rests on a thick layer of T6 and T5 work, and that work was not failure; it was the cost. Nothing here may be used, alone, to evaluate a researcher.
- **A map, not a gate.** The T-Grade is drawn after publication. It is not a submission criterion, and a journal policy of "T4 and above" would be a misuse.
- **Within a field only.** Each axis is translated per field. A T4 in experimental physics and a T4 in education research share a label and are not the same thing. That is why verdicts are sorted into field folders, and why comparisons stop at the folder boundary.
- **Never a grade without its verdict.** Strip away the three sentences and what remains is a brand, not a diagnosis. If bare grades begin to circulate from this repository, the standard's own view is that the project is better abolished than continued.
- **Never a verdict without its notice, worksheet, right of reply, and citation.** Each verdict carries these on its own (Prohibition 5). The paper's text is not reproduced; the verdict points to the paper and the reader is expected to go there.
- **Drafts, not decisions.** Verdicts are AI drafts under the two-layer structure of Chapter 8: the AI drafts, humans re-examine, especially border cases and upper grades. Until a verdict's "Human review" column reads otherwise, it has had the first layer only.

## For authors of evaluated papers

If your paper is graded here, this repository commits to the following.

- **Full reasoning, always.** No grade is published without the worksheet that produced it: the field and its translation, the claim and evidence sentences, the eight answers with reasons, the three-sentence verdict, the border flag, and a log of what was verified.
- **Corrections.** If a verdict misstates a fact about your paper, open an issue with the *Author response / correction request* template. Factual errors are corrected in the verdict file and recorded in its verification log.
- **Right of reply.** A response from an author is appended to the verdict verbatim, in the language it was written in, under the heading *Author response*. It is not edited, shortened, or paraphrased.
- **Re-examination.** An author response, or any substantive objection, triggers human re-examination of the grade by the maintainer. The re-examined grade, whether changed or not, is recorded with its reasons.
- **Withdrawal requests.** A request to withdraw a verdict is answered publicly in the issue, with reasons. A verdict is not withdrawn because its grade is low; it may be withdrawn if the paper was misidentified, if the reading cannot be corrected in place, or if the verdict is being used contrary to the ground rules above.

The T-Grade has no axis for an author's effort, seniority, or intent. A verdict says nothing about them.

## How a verdict is produced

1. Write down the field in which the paper claims its contribution and how Axis 3 is read there (Step 0). Record the venue as a hint and nothing more.
2. Read backwards (§4.1): conclusion and abstract, then evidence, then method, then introduction. Write the one-sentence claim and the one-sentence evidence before reading the introduction.
3. Answer the eight questions with yes / partial / no and one line of reasons each (§4.2), and compute the deficit.
4. Map answers to a grade (§4.3). Where the rules and the tier definitions disagree, the definitions win, and the verdict says so.
5. Write the three sentences (§4.4).
6. Mark the border if a single judgment decided the grade, and flag it for human re-examination (§4.5).
7. Record what was verified outside the paper (venue status, identifiers, figures) in the verification log (§4.6).
8. File it under `papers/<major-field>/<sub-field>/NNN_short_title.md`, with a counterpart in the paper's language where that differs from English, and add a row to the index in `papers/README.md`.

A program verdict follows the same procedure through the translation in [002_program.md](002_program.md): pin the revision by hash, execute and decode the artifact before reading its documentation, run the domain's mandatory steps from its field notes, and file it under `programs/<domain>/NNN_short_title.md` with a row in `programs/README.md`.

## The AI judge and its limits

The standard is candid about its judge (Chapter 8), and so is this repository.

- **It does not know the frontier.** A T2 verdict requires knowing a paper's relation to open problems, much of which is never written down. AI verdicts are most reliable in the T6–T4 range and need expert cross-examination above it.
- **It can be persuaded.** A well-written paper and a well-done study are different things, and the backwards reading order exists to keep the judge from confusing them.
- **Its consistency is both feature and bug.** One standard applied to thousands of papers also applies one set of biases to thousands of papers. Human noise partly cancels; a single model's bias does not. Hence the two-layer structure.

The standard itself has not been validated: no inter-rater agreement study, no correlation against existing metrics, no tracking of T2 verdicts over time. Appendix B of the standard sets out the protocol and the thresholds it would have to meet. Until that is done, every verdict here is the output of an uncalibrated instrument, and should be read as one.

## Authorship and license

The standard was written by Claude Fable 5 (Anthropic) and revised by Claude Fable 5.1. Verdicts are drafted by Claude Fable 5.1 and identify their judge, version, and date. The repository is maintained by [hajunho](https://github.com/hajunho), who is responsible for human re-examination and for answering issues.

Licensed under the [GNU General Public License v3.0](LICENSE).
