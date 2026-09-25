# Field Notes — Retrieval Systems

*Normative checklist for every verdict in this folder. Read before judging; update, with dates, whenever a verdict teaches the domain something new. Version: 1.0, September 2026.*

This domain covers systems that retrieve from a corpus and advise: search engines over document sets, retrieval-augmented generation, question-answering over a body of records. Its defining risk is that the system's answers are only as true as its corpus is current — and that nothing in a fluent answer reveals a stale or bypassed corpus. The axes of [002_program.md](../../002_program.md) are read here as follows; §1–§5 are mandatory steps before any verdict in this folder.

## 1. The staleness audit

Date the corpus; date the claim. The verification log records **the newest document actually present in the shipped corpus** (found by decoding the index or store, not by reading the README) next to **the currency the documentation claims** ("current", "up to date", a named year). The gap between the two dates is the true scope of the evidence sentence, and the verdict states both dates.

The domain's governing sentence: **in an advisory system, staleness is not degradation — it is wrong answers.** A search engine that misses last month's documents is worse at its job; an advisory system whose corpus predates a change in the rules it advises on delivers confident, well-formed, wrong advice. Defect 6.3 of 002 (the frozen corpus behind a live claim) is this domain's signature defect, and no verdict here may skip the audit that catches it.

## 2. Verify dependencies against the bytes

Retrieval stacks advertise their components — the embedding model, the vector index, the reranker — and the advertisement is checkable, because the artifacts have decodable structure. Decode them. A flat inner-product index, for instance, is a small header followed by raw floats: its dimensionality, its size, and hence which embedding model could have produced it, are all readable straight off the bytes and either corroborate the README or contradict it. The log records what was decoded and what it proved. A claimed component that the bytes cannot confirm is defect 6.1, and question 1 is answered from the bytes, never from the import list.

## 3. The fallback audit

Every retrieval system has a degraded path — keyword grep when the index is missing, a smaller model when the large one fails to load, an empty-context answer when retrieval returns nothing. The judge **induces each failure deliberately** (remove the index, break the model path, query outside the corpus) and records what the user is told. A fallback disclosed at the moment it fires is legitimate engineering; a fallback that presents grep results, or context-free generation, in the same voice as the advertised pipeline is defect 6.2 — claim overreach committed at runtime — and it decides question 1. The audit also answers a question users cannot: *which engine produced the answer I was given?* A system that cannot say has an evidence problem, not a UX problem.

## 4. Secrets hygiene

Retrieval systems concentrate credentials: embedding-API keys, database URLs, tokens for the sources the corpus was pulled from. The verification log scans the release for them — including the release's history, since a deleted ignore-file is a documented way live keys reach a repository. Per rule 5 of [programs/README.md](../README.md): the finding goes to the authors privately before the verdict publishes, and the verdict names the class of the leak, never its content. A live secret in the artifact is defect 6.5 and fails the premise of question 4 — a third party cannot safely reproduce from this release.

## 5. Incremental recordability

A corpus that cannot be updated without being rebuilt from scratch will not be updated; §1's staleness is usually this defect one year later. The log therefore records whether the system can **ingest incrementally, with provenance** — can a new document be added with its source and date attached, and can the corpus state be enumerated afterward (what is in here, from where, as of when)? A system that can answer those questions has a maintainable relationship with time; a system that cannot has an expiry date its documentation does not print. This axis reads consequence (question 8) for the domain: nothing durable is built on a corpus that cannot say what it contains.

## 6. Anonymization note

The defects above were generalized from audits of real systems. Field notes and verdicts in this folder carry **no identifying details** of audited systems beyond what a published verdict's citation requires (repository, revision, license): no company names, no internal project names, no reproduced secrets. The defect matters; the culprit does not.
