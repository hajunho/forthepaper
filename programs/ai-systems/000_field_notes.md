# Field Notes — AI Systems

*Normative checklist for every verdict in this folder. Read before judging; update, with dates, whenever a verdict teaches the domain something new. Version: 1.0, September 2026.*

This domain covers models, model releases, and — because they are software making measurable claims — the benchmarks and leaderboards that evaluate them. The axes of [002_program.md](../../002_program.md) are read here as follows, and the verification steps in §1–§4 are mandatory before any verdict in this folder.

## 1. Pin the revision: hash, not tag

A model repository's tag can be moved after the leaderboard run, after the blog post, after the verdict. The verdict names the **commit hash** of the exact revision judged — weights, tokenizer, configuration, and card together. If the release names only a version tag, the verification log records the hash that tag resolved to on the date of judgment. Everything the verdict says is true of that hash only; a claim of the form "model X does Y" with no revision attached is not yet a claim this folder can judge.

## 2. Verified numbers only

A number in a model card counts as evidence only if the log can answer: **which benchmark, which configuration (shots, prompt, harness version), which date, run by whom.** A number that cannot produce its measurement is treated as absent — defect 6.4 of 002, the descendant of the standard's rule that a quantity computed but not reported counts as absent. Numbers reproduced from another model's card, or from a leaderboard whose harness differs from the card's stated setup, are recorded as hearsay, not evidence.

## 3. Read the limitations section as a signal

In this domain the thickness and specificity of a model card's limitations section is among the most reliable honesty signals available at reading time. A card that names concrete failure modes — languages it degrades in, formats that break it, benchmark contamination it could not rule out — is doing what the standard's T5 completeness rule demands of a paper. A card whose limitations section is boilerplate ("may produce inaccurate outputs") has not stated its limits, and completeness is judged accordingly. The signal is asymmetric: a thick limitations section cannot raise a grade by itself, but a hollow one caps the completeness reading.

## 4. Fixed probes

Executing the artifact (002 §3) means, in this domain, running a small **fixed probe set** — inputs chosen by the judge, held constant across all verdicts in this folder, and kept out of the model card's demo path. Probes are not a benchmark and produce no score; they exist to catch the gap between demo and behavior: the claimed capability that only works on the README's example, the silent fallback in the serving stack, the tokenizer that mangles the second language the card advertises. The probe set and its transcript go into the verification log, verbatim.

## 5. The catalog of failed leaderboards

Venue hints in this domain are leaderboard ranks, and the record shows exactly how each kind fails. These are this domain's analogue of the ruptures in [001_proxy_atlas.md](../../001_proxy_atlas.md): dated events, kept because their decay is the point.

- **Contamination.** Benchmark items leak into training corpora, by accident or otherwise, and the score measures memory instead of capability. Endemic and repeatedly documented across public benchmarks; the reason a card that cannot discuss contamination has not stated its limits (§3).
- **Saturation.** In June 2024 the Open LLM Leaderboard was rebuilt with a new benchmark suite because the old one had saturated — top models were separated by noise, and the ranking had stopped measuring. A leaderboard has a service life, and a rank cited without the leaderboard's version and date is a number without a scale. (The leaderboard was retired altogether in March 2025.)
- **Selective disclosure.** *The Leaderboard Illusion* (April 2025) documented, on the most-watched preference leaderboard, private variant testing — one provider testing 27 unpublished variants before releasing the best performer's score — and deep data-access asymmetries between large providers and everyone else. A rank is a hint about the process that produced it, and the process is not the same for all entrants.
- **The ranked model is not the released model.** April 2025: a major open-weights release ranked near the top with an "experimental" chat-optimized variant, while the checkpoint actually released to the public was a different model. The rank was true; it was true of bytes nobody could download. This is why §1 pins hashes: a leaderboard entry without a revision is a claim about nothing in particular.

**Discipline for verdicts:** a leaderboard rank is cited, if at all, as a venue hint — with the leaderboard's name, version, and date — and never as evidence on the quantitative axis. Evidence is a measurement whose configuration the log can reproduce (§2).

## 6. A leaderboard is software

Every failure in §5 is a defect catalogued by 002: contamination is an unverified dependency between training set and test set; saturation is a measurement instrument out of range; selective disclosure is a fairness failure in the comparison (question 3); ranked-but-not-released is a claim about bytes other than the pinned ones (question 1). A leaderboard is documentation plus artifact, and this folder can grade one. That is the platform's closing argument: nothing in the evaluation stack is exempt from the standard it administers.
