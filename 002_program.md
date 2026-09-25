<p align="right"><b>English</b> · <a href="002_program.ko.md">한국어</a></p>

# The Weight of a Program

## The T-Grade Translated for Software Artifacts

**A translation of [*The Weight of a Paper*](000_tier.md), not a second standard.**

*First edition, September 2026. Written by Claude, an AI language model (Anthropic). Korean edition: [002_program.ko.md](002_program.ko.md). By its own scale this document grades itself T6: the translation is laid out, its validation is not done.*

---

> A paper is a claim plus its evidence. A program is the same object in different matter: its **documentation** — the README, the model card, the release notes — is the claim, and its **artifact** — the bytes that run — is the evidence. Everything the standard says about the distance between claim and evidence applies unchanged; only the way the judge collects the evidence changes. This document translates the standard, chapter by chapter, and adds the one thing programs need that papers do not: a catalog of the defects that live specifically in the gap between documentation and bytes.

---

## 1. The Correspondence

| In the standard | For a program |
|---|---|
| The paper | The release: documentation plus artifact, at one pinned revision |
| The claim (what the conclusion asserts) | What the documentation says the program does, requires, and achieves |
| The evidence (what was shown) | What the artifact demonstrably does when executed, decoded, and inspected |
| Claim overreach | Documentation that asserts what the bytes do not deliver |
| The venue (a hint, never a verdict) | Stars, downloads, leaderboard rank, org name — hints, never verdicts |
| Reading the full text | Running the code, decoding the artifacts, reading the source |

One rule before any other: **a verdict grades one pinned revision.** A paper cannot change after publication; a repository can. The verdict names the commit hash — not a tag, not a branch, not "latest" — and everything it says is true of those bytes only. A tag can be moved; a hash cannot. (The domain field notes give the mechanics.)

## 2. The Five Axes, Translated

The five questions do not change; what counts as an answer does — exactly as the standard's Chapter 2 translates them across research fields.

| Axis | For a program |
|---|---|
| **Novelty** | What could not be built before this existed — and at which layer: new problem, new method, new combination (a known method packaged for a new setting; most software lives here, and this is not a defect), or new confirmation (a reimplementation that verifies someone else's claim). |
| **Rigor** | Does the artifact do what the documentation claims, under the conditions the documentation states? Do the claimed dependencies actually participate at runtime? Does every advertised path work, or only the demo path? |
| **Quantitative evidence** | Are performance and quality claims backed by measurements that are on the record — the benchmark, the configuration, the date? A number whose measurement cannot be produced counts as absent, the direct translation of the standard's rule that a quantity computed but not reported counts as absent. |
| **Reproducibility** | Can a third party build, run, and obtain the claimed behavior from the release alone? Pinned dependencies, stated environment, data available or fully specified. As with papers, a small tool can score perfectly here: the axis measures integrity, not size. |
| **Consequence** | Can the next system be built on top of this one? Stable interfaces, a license that permits it, and a design that others can extend — judged at reading time, not by the download count. |

## 3. Reading Order — the Artifact First

The standard reads a paper backwards, conclusion before introduction, so that the author's framing cannot hide the gap between claim and evidence. The translation for programs:

1. **Execute and decode the artifact first.** Run it on inputs of the judge's choosing, not the README's. Decode the data files; list the actual runtime dependencies; observe what the program does when its primary path fails.
2. **Write down the evidence sentence**: what the artifact was observed to do, one sentence.
3. **Only then read the documentation**, and write down the claim sentence: what it says the program does.
4. **Measure the distance.** That distance is claim overreach, and it is the primary determinant of the grade, exactly as in §4.1 of the standard.

A judge who reads the README first is captured by it — the demo works, the phrases are confident, and the silent fallback (§6.2) becomes invisible. The order is the same prescription the standard writes for itself, in different matter.

## 4. The Eight Questions, Translated

Answer yes / partial / no; the deficit arithmetic, the grade mapping, and the rule that the tier definitions win over the arithmetic are all inherited unchanged from §4.3 of the standard.

1. Does the artifact do what the documentation claims? (claim–evidence match)
2. Do measurements exist independent of the author's assertions — benchmarks on record, tests that run? (independent evidence)
3. Are there comparisons, and are they fair — baselines run with the same care as the system itself? (fair comparison)
4. Can a third party build, run, and reproduce the claimed behavior from the release alone? (reproducibility)
5. Is what is new specified against the systems that already exist? (novelty specified)
6. At which layer is the novelty — problem, method, combination, confirmation? (novelty layer)
7. Is the verification interoperable — standard benchmarks, standard formats, results others can compare against? (the T3 gate)
8. Can the next system be built on this one? (consequence)

## 5. The Seven Tiers, Read for Programs

- **T7 — Record.** Code that exists to record that an attempt exists: a gist, an unbuildable dump, a script with its paths hard-wired to one machine. Not yet in verifiable form. As with papers, looking down on T7 is the misjudgment — complete substance published informally is not T7.
- **T6 — Pilot.** It runs, and demonstrates the idea — on the happy path, at demo scale, without measurement. Most research code lives here, honestly, and T6 code speaking T6 language ("prototype", "proof of concept") is a match, not a deduction.
- **T5 — Full Proceedings.** A complete release — install, run, documented behavior, stated limits — whose verification persuades its own users but stops there: few tests, no independent measurement, comparisons thin. Completeness includes a statement of limits; a README that never says where the program stops working has not completed its narrative.
- **T4 — Sound Study.** No fatal defect: the documentation claims exactly what the artifact delivers, the tests exercise what the README advertises, failure modes are surfaced rather than swallowed. The spine of every healthy codebase, and exactly as unglamorous as the standard says T4 papers are.
- **T3 — International Standard.** Verification interoperable with the field: standard benchmarks with configurations on record, standard formats, CI that a stranger can read, results others have reproduced. A property of the verification, not of the org name on the repository.
- **T2 — World-Class.** Others build their systems on it, and the default way of doing something changed because it exists. Judged with the same caution the standard applies: popularity is a hint with a large random component, not the verdict.
- **T1 — Paradigm.** The program after which the field dates itself. Never assigned in real time; withheld, as the standard withholds it.

The staircase rule survives translation intact: **from T6 to T4 a program climbs by filling in verification; from T4 to T2 it climbs by filling in novelty.**

## 6. The Defect Catalog

Papers and programs fail differently. These five defects live specifically in the gap between documentation and bytes; each was observed in the field, and each is anonymized here because the defect matters and the culprit does not. The catalog is what §3's reading order exists to catch.

### 6.1 The claimed dependency that is not there

The documentation names a library, a model, or a technique as the engine of the system; the artifact, decoded, does not contain or does not invoke it. The claim rides on the reputation of a component that never runs. **Judge's move:** verify dependencies at the byte level — what is loaded, what is called — never from the import list or the README. A claimed-but-absent dependency is a "no" on question 1, and severe.

### 6.2 The silent fallback

The primary path fails — the index is missing, the model cannot load, the service is down — and the program silently degrades to a cruder method, presenting the degraded output as if it were the advertised one. The user cannot know which engine answered. **Judge's move:** induce the failure. Break the primary path deliberately and watch whether the program says so. A fallback is legitimate exactly when it is disclosed at the moment it fires; undisclosed, it is claim overreach committed at runtime.

### 6.3 The frozen corpus behind a live claim

The documentation speaks in the present tense — current data, up-to-date guidance — while the data the artifact ships was frozen at a date the documentation does not state. In an advisory system, staleness is not a performance discount; past the date the world changed, it is wrong answers delivered with confidence. **Judge's move:** date the data, date the claim, and treat the gap as the evidence sentence's true scope. A verdict on such a system states both dates.

### 6.4 The number before the measurement

The README asserts a latency, an accuracy, a throughput — and no benchmark, configuration, or date can be produced that yields the number. Marketing prose in the position of evidence. **Judge's move:** ask for the measurement; a number whose measurement cannot be produced counts as absent (§2), and question 2 is answered accordingly. This is the direct descendant of the standard's rule that a figure without a scale is not a measurement.

### 6.5 The secret in the artifact

Credentials, tokens, or private keys shipped inside the release — sometimes committed, sometimes revealed by a deleted ignore-file. This is not merely a security bug: an artifact that leaks its author's secrets fails question 4's premise (a third party cannot safely reproduce from this release) and testifies that the release process itself was never inspected. **Judge's move:** scan for secrets as a fixed step of the verification log; report the finding to the author privately before the verdict publishes, and never reproduce the secret's value anywhere — the verdict names the class of the leak, not its content.

## 7. Prohibitions, Inherited

Chapter 6 of the standard applies verbatim, with one word changed. A T-Grade measures one release, never a developer — every strong engineering career stands on a sediment of T6 prototypes, and that sediment was the cost, not the failure. It is a map drawn after release, not a merge gate; a policy of "T4 or no merge" is the misuse Prohibition 2 names. It is valid only within a domain: a T4 game and a T4 retrieval system share a label, not a meaning — which is why program verdicts are filed under domain folders and comparisons stop at the folder boundary. A grade never circulates without its three sentences. And a verdict on a named program is published only with its complete worksheet, its fallibility notice, a standing right of reply for the authors, and a citation — repository, revision, license — in place of wholesale reproduction of the code.

**Where verdicts live:** [`programs/`](programs/README.md), one folder per domain, each with its own field notes that translate the axes further — the analogue of the standard's per-field axis table. The verdicts are drafted by an AI judge and pass through the two-layer structure of the standard's Chapter 8, whose limits — not knowing the frontier, being persuadable by good prose, uniform bias — apply to this judge with no discount.

---

*This translation was produced the way the standard was: by applying the procedure and writing down what the application taught. Its verification — the protocol of the standard's Appendix B, re-read for programs — has not been done, and until it is, every program verdict here is the output of an uncalibrated instrument, and should be read as one.*
