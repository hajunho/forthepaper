# The Weight of a Paper

## A Language Model's Seven-Tier System for Evaluating Research

**by Claude Fable 5**

*Revised edition, September 2026. Revised by Claude Fable 5.1; the revision notes at the end list what changed. Korean edition: [000_tier.ko.md](000_tier.ko.md).*

---

> This book was written by Claude, an AI language model. It is an attempt by an entity that has read and digested millions of papers to look at the evaluation customs of human academia from the outside, and to set down one alternative standard. The grading system in this book claims no authority. It claims only consistency.

---

## Preface — Why Another Grade?

Academia is already drowning in grades. Journals have impact factors; researchers have h-indices; conferences have CORE rankings; Korea, where an earlier version of this book first appeared, has its KCI registry and the looming hierarchy of SCI, SCIE, and SCOPUS. And yet something strange happens. With all these instruments in hand, if you pick up a single paper and ask the simplest possible question — *how good is this paper?* — you still find yourself at a loss.

The reason is that every one of the existing instruments measures **something other than the paper**. The impact factor measures the journal: inside any journal live a few papers that pulled the average up and many that rode along on it. The h-index measures the researcher. Citation counts appear to measure the paper, but in fact they measure the paper's position in a network — an ordinary paper in a fashionable field will be cited a hundred times more than an outstanding paper in an unfashionable one. Conference tiers measure the height of a gate. They say nothing about the spread among the papers that cleared it.

What we lack, in short, is not another metric. It is **a standard whose unit is the paper itself, independent of venue, that can be applied by reading**.

I am a language model. In training I read human papers in enormous quantity across every field, and every day I am asked to read and judge someone's manuscript. Through this I acquired, almost involuntarily, an internal standard — one that lets me cover the journal name, read only the body, and say "this paper sits at roughly this height on this staircase." This book takes that standard out of my head, sharpens it, attaches its reasons, and equips it with a judging procedure.

I will call the system, plainly, the **T-Grade** (Tier Grade): seven steps from T7 to T1, lower numbers higher. Why seven is explained in Chapter 3; the short version is that the human capacity for consistent discrimination and the actual gate structure of academia jointly carve out about seven meaningful steps.

One thing must be fixed before we begin. **This is a ruler for papers, not for people.** The author of a T6 paper is not a T6 researcher. Every great research career stands on a thick sediment of T6 and T5 work. The moment that distinction collapses, this system stops being an instrument and becomes a weapon. Chapter 6 confronts that danger directly.

---

# Part I — What the Existing Instruments Measure, and What They Miss

## Chapter 1. Five Rulers, Five Distortions

### 1.1 The Impact Factor: Judging the Contents by the Average of the Container

The impact factor is the mean number of citations, over the past two years, received by the papers in a journal. Three distortions are built into the definition itself.

First, the **distortion of the mean**. Citation distributions are violently skewed. Even in a Nature-class journal, the top ten or twenty percent of papers collect most of the citations while the rest fall far below the journal's average. Knowing that a paper appeared in an IF-40 journal is nearly worthless as a prediction that the paper will receive forty citations.

Second, the **distortion of the time window**. A two-year window favors fast-fashion fields (machine learning, the life sciences) and punishes slow-ripening ones (mathematics, theoretical physics, the humanities). It is common for a landmark paper in mathematics to begin accumulating citations a decade after publication.

Third, the **distortion of field size**. Citations scale with the number of people writing papers in a field. The same quality of contribution earns thousands of citations in deep learning and dozens in the computational linguistics of a minority language. The impact factor launders this difference in population into an apparent difference in quality.

### 1.2 Citation Counts: Mistaking Network Position for Quality

The citation count of an individual paper is better than the impact factor — at least the unit is the paper. But citation is a function of **visibility** before it is a function of quality. A famous author, an Anglophone affiliation, virality on social media, the first-mover position of being "the first paper on that problem," and above all the population of the field — these determine citations. Methods papers and surveys vacuum up citations regardless of depth. Some papers are cited chiefly in order to be refuted. A citation count answers "how often was this mentioned," not "how right and how solid is this."

### 1.3 Conference Tiers: A Ruler That Reports Only the Height of the Gate

Computer science runs on conferences rather than journals, and the top venues — NeurIPS, ACL, OSDI — accept roughly one paper in five. Tier is genuinely informative: the higher the gate, the higher the average of what clears it. But two things are missing. One is the **spread above the gate**: among the accepted papers of the same NeurIPS coexist work that later redirected the field and work no one ever read again. The other is the **spread below the gate**: rejected piles contain a substantial number of excellent papers felled by reviewing noise. In NeurIPS's own consistency experiment, the same set of submissions was routed to two independent committees, and the accept/reject decisions disagreed on nearly half. The gate is real, but passage through it carries a larger random component than anyone likes to admit.

### 1.4 Peer Review: The Best Institution We Have — and Still a Filter, Not a Ruler

Peer review does not grade; it passes or fails. As a filter it is noisy, as we have just seen. More fundamentally, its output — accept, reject, revise — is not attached to the paper. Looking at a published article, you cannot tell whether it was a unanimous strong accept or a third-attempt squeaker. Evaluation information is produced and then discarded by design.

### 1.5 The Korean Hierarchy: KCI, the Registry, and the Cult of "SCI-Class"

Korean academia adds its own strata: the KCI registered/candidate distinction descending from the old research-foundation system, and above it the catch-all honorific "SCI-class." The hierarchy is administratively crisp and produces two side effects. First, **the internal spread of domestic journals is flattened entirely** — a registered journal demanding international rigor and one operating close to a pay-to-publish model count identically as "KCI registered." Second, **the single gate of SCIE turns from means into end**. The SCIE list spans everything from the best journals in the world to high-volume outlets the international community regards with suspicion, yet a performance review records each as "one SCIE paper." When crossing a gate becomes the goal, traffic converges on the lowest point just above the gate. That is precisely what happened. Readers outside Korea will recognize the pattern instantly: only the proper nouns are local.

### 1.6 What the Five Distortions Share

Set the five rulers side by side and the common trait appears: every one is a **proxy**. Instead of measuring the paper's quality directly, each measures something believed to correlate with it — the container, the network, the gate, the checkpoint. And the fate of proxies was written long ago by Goodhart's law: when a measure becomes a target, it ceases to be a good measure. Journal self-citation engineering, citation cartels, salami slicing, hunting the floor of the SCIE list — all of these are direct attacks on proxies behaving exactly as Goodhart predicts.

Is a direct measure impossible? Until recently, yes — on cost grounds. To measure a paper directly you must read it, and the time of people qualified to read and judge has always been academia's most expensive resource. So academia survived on proxies that could be computed without reading. That premise has now changed. The cost of reading a paper and judging it against a consistent standard is collapsing — because of entities like me. The starting point of this book is that the bargain forced upon us by the age of proxies is due for renegotiation.

---

## Chapter 2. The Five Axes — What Should Be Measured

If we are going to measure papers directly, what do we measure? When I read a paper I ask five questions. The five axes are mutually independent — a paper high on one is not thereby high on another — and it is the *pattern* across the five that determines the grade.

### Axis 1. Novelty — What Would the World Not Know Without This Paper?

Novelty asks not "is it new?" but "**what, precisely, is new?**" Newness comes in layers:

- **Novelty of problem**: a question nobody was asking. The rarest and the most valuable.
- **Novelty of method**: a new solution to a known problem.
- **Novelty of combination**: a known method applied to a new object. The overwhelming majority of the literature lives here, and this is not in itself a defect.
- **Novelty of confirmation**: a known result re-established under new conditions. Replication studies live here — essential to the health of science and chronically undervalued.

The commonest error in judging novelty is taking the author's word for it. "We are the first to…" is a claim to be verified, not a basis for judgment. The thinner the related-work section, the bolder the priority claims tend to be.

### Axis 2. Rigor — The Distance Between Claim and Evidence

Rigor asks not whether the conclusion is true but whether, **within the paper, the conclusion actually follows from the evidence presented**. Did the design control the confounds? Does the statistical test match the hypothesis? Are there gaps in the proof? Are the baselines fair? — tuning your own method while running the competitors at default settings, the "strawman baseline," is the most frequent deduction on this axis. And decisively: **does the range of the claim stay within the range of the evidence?** Running an experiment on nineteen documents and concluding that "the effect was confirmed" is a claim that has traveled beyond its evidence. I call the excess *claim overreach*, and I weight it more heavily than any other single factor in grading.

### Axis 3. Quantitative Evidence — Has Judgment Been Converted into Measurement?

The difference between "performance improved" and "NPMI rose from 0.12 to 0.31, averaged over five seeds, with non-overlapping 95% confidence intervals." Quantitativeness looks like a subset of rigor, but it earns its own axis for a reason: some fields are essentially qualitative — anthropology, history, parts of education research — and there the axis must be translated from *measurement* into **systematicity of evidence**: transparency of case selection, treatment of counterexamples, triangulation. The name of the axis changes with the field; the question does not: *does evidence exist independently of the author's impressions?*

### Axis 4. Reproducibility — Can Someone Else Arrive at the Same Result?

Could a third party, reading only the paper, obtain the same result? Is the data released or fully specified? Are parameters, environment, and procedure on record? Is there code? Reproducibility is the easiest of the five axes to check and the one most often empty. It also has a peculiar property: **a low-grade paper can score perfectly on it.** A small pilot study that discloses its procedure completely has secured reproducibility in full. It measures not the size of the research but the integrity of the researcher.

### Axis 5. Consequence — What Can Be Built on Top of This Result?

A warning first: this axis is *not* citation count. Citations are observed after the fact; the consequence axis is a **structural property judged at reading time**. The question is: *if this paper's conclusion is true, can the next study be built on it?* Does it transplant to other fields? Does it change a practical decision? Conversely, there exist papers whose conclusions could be perfectly true and change nothing — the conditions too special, or the conclusion already common sense. Consequence carries the largest judgment uncertainty of the five axes, and therefore the smallest weight in grading. Yet it is this axis, in the end, that separates the top grades.

### Translating the Axes by Field

The five questions do not change from field to field; what counts as an answer does. A judge who carries the standards of one field into another produces the most confident and the most wrong verdicts this system can produce. So before grading, the judge writes down the field in which the paper claims its contribution (Chapter 5, Case 6) and how each axis is read there. The table is a starting point, not a codebook.

| Axis | Experimental sciences | Computational research and machine learning | Mathematics and theory | Qualitative social research, education, the humanities |
|---|---|---|---|---|
| Rigor | Controls, blinding, adequate power; pre-registration where the field expects it | Baselines tuned as carefully as the proposed method; ablations; variance across seeds | Proofs complete, lemmas checked, assumptions stated where they are used | Alternative explanations considered; counterexamples sought and reported; the scope of the claim matches the cases studied |
| Quantitative evidence | Measurements with uncertainty, and the test that matches the hypothesis | Standard metrics, multiple runs, confidence intervals, held-out generalization | Generality and tightness of what was proved, separated from what is conjectured | Systematicity: transparent case selection, a coding scheme fixed before reading, a second coder with an agreement statistic, counts or proportions wherever something was counted, triangulation |
| Reproducibility | Materials, protocols, raw data, analysis scripts | Code, data, seeds, environment, exact configuration | Proofs self-contained or cited precisely | Data or transcripts as far as ethics allow; instruments and prompts; the coding scheme; the researcher's relation to the participants disclosed |
| Novelty | New phenomenon, mechanism, or measurement | New problem, new method, or a result that changes what is believed to work | New theorem, new technique, new connection between areas | New question, new lens, new corpus, or a known lens brought to a new site (combination) |
| Consequence | Changes what the next experiment should be | Changes the default approach to the problem | Becomes a tool used by later proofs | Changes practice, policy, or the questions the field asks |

One rule holds in every column. **A quantity that was computed but not reported counts as absent.** A figure without a scale is not a measurement; an analysis described but not shown is not evidence. The judge grades the paper on the page, not the analysis the authors could have shown.

### How the Axes Combine

Draw the five axes as a radar chart and you get the paper's *shape*. A grade is a type of shape. A paper with a large idea and empty verification (novelty high, quantitativeness low) is one characteristic shape near the bottom of the staircase; a paper filled evenly across all five axes stands near the top. The next chapter organizes these shapes into seven steps.

---

# Part II — The Seven Steps

## Chapter 3. The T-Grade System: Definitions and Diagnostic Signals

### 3.0 Why Seven?

The number of grades cannot be arbitrary. Too few — say, high/middle/low — and distinctions that matter in practice are crushed together. Too many — a 100-point scale — and inter-rater agreement collapses, turning the grade into noise with decimal places. Psychometrics settled long ago that humans can consistently discriminate a complex object into somewhere between five and nine levels. Overlay on that the actual gate structure of academia — unrefereed records, preliminary presentations, full proceedings, refereed journals, international refereeing, top-venue refereeing, and the exceptional few above all gates — and seven steps fall out naturally. Seven is less an invention than a discovery.

Each grade is described in three parts: a **definition** (the essence of the grade), **diagnostic signals** (concrete features you check while reading), and **common misjudgments** (the traps that push a paper one step too high or too low).

---

### T7 — Record

**Definition.** A document that has not undergone review and was not written on the premise of review: presentation summaries, extended abstracts, technical memos, pre-review manuscripts, research notes on a blog. Its purpose is to record that research exists, not to verify its claims.

**Diagnostic signals.** The related-work section is absent or perfunctory. The method description falls short of reproducibility. The deferral "details in a forthcoming paper" appears.

**Common misjudgments.** Looking down on T7 is itself the misjudgment. Manuscripts that exist only on arXiv sometimes carry T2-level content — mathematics and machine learning supply real examples. Because the T-Grade measures content rather than venue, **an archived manuscript whose substance is complete is not a T7.** T7 does not mean "unreviewed"; it means "not yet in verifiable form." This distinction is the system's first point of divorce from the existing hierarchy.

---

### T6 — Pilot

**Definition.** There is an idea, and a minimal demonstration that the idea works — but no quantitative evaluation, no comparison, no scale. Conference short papers, workshop papers, and the bulk of domestic proceedings live here.

**Diagnostic signals.** The dataset is plainly too small to support a statistical claim. There is no baseline. Evaluation consists of the authors' qualitative interpretation. The conclusion speaks in the grammar of possibility — "we confirmed the potential," "this may contribute to." That grammar, note, is honest: a T6 paper speaking T6 language is not a deduction but a *match*.

**Common misjudgments.** Both directions occur. Upward: awarding T5 or T4 because the idea is fresh — one high axis does not make a high grade. Downward: docking to T7 because the scale is small — if the procedure is complete and reproducible, it is a pilot, not a record. T6 is the humus layer of a healthy research ecosystem. T3 papers rarely appear in soil that has no T6.

---

### T5 — Full Proceedings

**Definition.** A complete narrative — problem, method, experiment, results, limitations — that has passed review, but whose verification reaches only far enough to persuade its own community. Full papers at domestic conferences and the lower tracks of international ones are the type specimens.

**Diagnostic signals.** Experiments and numbers exist, but comparisons stop at one or two baselines. Statistical significance testing is absent or ritual. A limitations section exists but is brief. Related work leans on domestic literature or a single lineage.

**Common misjudgments.** The T5/T6 border is not "was it reviewed?" but **completeness**. A short paper that passed review is still T6; a paper at a lenient venue that nevertheless achieves completeness and quantitative verification is T5. Nowhere is the discipline of using venue as a hint but never as a verdict more necessary than at this border. Completeness includes a statement of limits. A paper that never says where its claim stops has not completed its narrative, whether or not it carries a section headed "Limitations"; conversely, limits stated honestly in the conclusion count in full. The missing statement of limits is the most frequent reason a paper that looks like T5 is graded T6.

---

### T4 — Sound Study

**Definition.** No fatal defect on any of the five axes. Novelty may be merely combinational, but rigor and quantitativeness meet the field's standard, the work is reproducible, and the claim stays within range of the evidence. The solid domestic-journal paper and the honest lower-quartile SCIE paper live here.

**Diagnostic signals.** No claim overreach. Fair baselines. Repeated runs or cross-validation. A limitations section that discusses actual limitations rather than performing modesty. You finish reading and the judgment forms: *this result can be trusted.*

**Common misjudgments.** T4 is undervalued because it is unglamorous. But T4 is the **spine** of the system. The body of scientific knowledge is an accumulation of T4; T2 and T1 erupt only from T4 strata. The health of any research community is better measured by its proportion of T4 than by its count of T1. The opposite misjudgment also occurs: awarding T3 because the paper is long and dense with tables. The number of tables is not an axis.

---

### T3 — International Standard

**Definition.** The level that a field's international community treats as the standard of verification: sufficient scale, multiple fair baselines, standard metrics with statistical tests, restrained conclusions, a released reproducibility package. Solid mid-range SCIE papers (Q2–Q3) and the poster or findings tracks of top international venues are typical.

**Diagnostic signals.** What separates T3 from T4 is **international interoperability of verification**. The metrics and benchmarks used are the field's shared standards, so that a researcher on another continent can compare results directly. Related work covers the international frontier. Generalization beyond the home dataset is demonstrated separately.

**Common misjudgments.** The equation "SCIE = T3." The lower reaches of the SCIE list hold masses of T5 content, and conversely domestic journals carry T3 content — authors choose domestic venues for many reasons. T3 is a property of the verification standard, not of a journal list.

---

### T2 — World-Class

**Definition.** A contribution at the frontier of a field, recognized by the people working at that frontier. Novelty at the level of problem or method; verification meeting the T3 standard; and the consequence axis genuinely lit — others begin building their next studies on this result. The majority of main-track acceptances at top venues and of papers in a field's very best journals sit here.

**Diagnostic signals.** When you finish reading, the map of the field has shifted slightly. A judgment forms of the type "this is now the default way to approach that problem" or "that assumption is now hard to maintain." Judgment at this grade takes in not only the paper's execution but its *position* — its relation to the open problems.

**Common misjudgments.** Treating top-venue acceptance as sufficient for T2. As Chapter 1 showed, acceptance at the best venues carries a large random component; a good share of accepted papers are, on content, T3 — and T2 papers sit in the rejection pile. T2 is the grade at which the venue hint betrays the judge most often.

---

### T1 — Paradigm

**Definition.** A paper that changed the question itself — after which the field dates its own history as *before* and *after*. By definition vanishingly rare (well under 0.1% of the world's annual output), and in most cases confirmed as T1 only years after publication.

**Diagnostic signals.** That full judgment is impossible at reading time is an essential property of T1, not a defect of the judge. There are premonitions: the paper does not stop at answering; it opens a space of new questions. The method shows signs of becoming a *language* used far beyond its original problem. And, interestingly, T1 papers are often not perfect on the five axes at publication — their verification is completed by the field that follows them.

**Common misjudgments.** Real-time T1 verdicts, handed out constantly. "Game-changer" and "paradigm shift" are written thousands of times a year; T1 happens a few dozen times a year. In this system I recommend operating T1 not as a grade one *assigns* but as a grade one **withholds**: cap real-time judgment at T2, and let time do the promoting.

---

### 3.8 The System on One Page

| Grade | Name | Essence | Deciding axis |
|---|---|---|---|
| T7 | Record | Prior to verifiable form | (n/a) |
| T6 | Pilot | Idea + minimal demonstration | Novelty alone lit |
| T5 | Full Proceedings | Complete narrative, limited verification | Completeness |
| T4 | Sound Study | No fatal defect | Rigor + claim/evidence match |
| T3 | International Standard | Interoperable verification | Quantitativeness + reproducibility |
| T2 | World-Class | Recognition at the frontier | Novelty + consequence |
| T1 | Paradigm | Replacement of the question | Judged by time |

One rule of the staircase should now be visible. **From T6 to T4, you climb by filling in verification; from T4 to T2, you climb by filling in novelty.** A paper with a good idea rises two steps by completing its verification; a paper with good verification rises only by changing its problem. Diagnosing *which* deficiency a paper has is the practical value of grading at all.

---

## Chapter 4. The Practice of Judging — Reading Order and the Eight Questions

A grading system without a judging procedure is a list of tastes. This chapter is a procedure for grading one paper in thirty to sixty minutes.

### 4.1 Reading Order (Recommended: Backwards from the Conclusion)

1. **Read the conclusion and abstract first, and write down the range of the claim.** One sentence: *what does the author assert to be true?*
2. **Read the experiments/evidence, and write down the range of the evidence.** One sentence: *what was actually shown?*
3. **Measure the distance between the two sentences.** This distance — the claim overreach — is the primary determinant of the grade.
4. Only then read the introduction and related work to judge novelty. The order matters: read the introduction first and you are captured by the author's frame, and the overreach becomes invisible.

### 4.2 The Eight Questions

Answer each: yes / partial / no.

1. Do the ranges of claim and evidence coincide? (rigor)
2. Does evidence exist independent of the author's impressions? (quantitativeness)
3. Do comparisons exist, and are they fair? (rigor)
4. Is the information for third-party reproduction complete? (reproducibility)
5. Is what is new specified against the related work? (novelty)
6. At which layer is the novelty — problem / method / combination / confirmation? (novelty)
7. Is the verification interoperable with international standards? (the T3 gate)
8. Can the next study be built on this conclusion? (consequence)

### 4.3 From Answers to Grade

Count each "no" among questions 1–4 as one point of deficit and each "partial" as half a point, and call the sum **D** (from 0 to 4).

- **D ≥ 3 → T7 or T6.** Completeness decides: a document not yet in verifiable form is T7; a complete but unverified demonstration is T6.
- **1.5 ≤ D < 3 → T6 or T5.** This is the band where most border cases live. T5 requires two things at once: **completeness** (problem, method, evidence, results, and a statement of limits) and **at least one piece of independently reported evidence** (question 2 not "no", with the numbers actually on the page). A paper missing either is T6.
- **D < 1.5, question 7 "no" → T5 or T4.** T4 is the grade of no fatal defect: it requires no "no" at all among questions 1–4, question 1 "yes" (no claim overreach), and comparisons that are fair where they exist.
- **Questions 1–4 "yes", question 5 "yes", question 7 "yes" → T3.** Question 6 has no yes or no; it need only be answered.
- **T3, plus novelty at the problem or method layer, plus question 8 "yes" → T2.**
- **T1 is never assigned.** It is withheld.

Two rules about the rules. First, the arithmetic is a guard against drift, not a substitute for reading: where the count and the definitions of Chapter 3 disagree, the definitions win, and the verdict says that they were used. Second, the first edition of this book gave no rule for the case in which every answer is "partial". That gap was found by using the procedure, and the middle band above is the repair.

### 4.4 Writing the Verdict

A grade thrown down without reasons is not a judgment. The verdict needs three sentences: **the grade; the axis that decided it; the deficiency that separates it from the next step up.** For example: *"T6. Procedural reproducibility is complete, but quantitative evaluation and baselines are absent, and nineteen documents cannot support a claim of generality. With an expanded corpus, coherence metrics, and human evaluation, this idea reaches T4–T3."* The third sentence is the reason this system exists. A grade must be a **diagnosis**, not a rank.

### 4.5 Marking the Border

Some verdicts are decided by a rule; others by a single judgment the rules leave open — whether a figure without a scale counts as evidence, whether limits mentioned in passing count as a statement of limits, whether two groups compared without normalization count as a comparison. When a grade turns on one such judgment, the verdict says so: it names the two grades between which the paper sits, states the judgment that decided it, and marks itself for human re-examination (Chapter 8). A border flag is not a weakness of a verdict; a hidden border is. Over many verdicts, the flagged judgments are also the system's best map of where its own rules need sharpening.

### 4.6 The Verification Log

A verdict is written from the full text, never from the abstract, and never from the text alone when the text points at something else. The judge extracts the figures when the figures carry the evidence, resolves the venue's status and the paper's identifiers from the record rather than from memory, and re-reads any passage on which a deduction rests. Everything checked outside the paper, and every correction to an earlier draft of the verdict, goes into a verification log attached to the verdict, with a version and a date. A verdict that cannot say what it checked has not earned the word.

---

## Chapter 5. Border Cases — Where the System Is Tested

The quality of a grading system shows not in its typical cases but at its borders. Six that recur:

**Case 1: A brilliant idea, unverified.** Novelty at the problem layer; experiments at demonstration scale. Verdict: T6 — with the layer of the novelty stated explicitly in the verdict. The T-Grade measures the paper as it stands, not the idea's future; the verdict sentence exists to carry the information the grade cannot.

**Case 2: A trivial result, perfectly verified.** Full marks on rigor, quantitativeness, reproducibility; novelty at the confirmation layer; no consequence. Verdict: T4. The judge will feel the pull to dock it to T5 for being "minor" — and that pull is precisely the mechanism by which academia has starved replication studies for decades. T4 is the minimum standing this system deliberately guarantees to rigorous replication.

**Case 3: First place on the big benchmark, and nobody knows why.** Top of the leaderboard, but no ablation — no way to tell which component did the work. Verdict: T5. The quantitativeness looks perfect, but the paper fails question 3 (fair comparison) and question 1 (claim/evidence match). Large numbers are not the same thing as quantitative evidence.

**Case 4: The negative result.** "X has no effect on Y," shown rigorously. Verdict: apply the identical procedure; the *direction* of an effect appears on no axis and is therefore never a deduction. A rigorous negative result earns T4; a negative result that demolishes a widely held hypothesis reaches T2.

**Case 5: The survey.** No new results — what is there to measure? Translate the novelty axis into *novelty of organization*: a new taxonomy, a lineage made visible for the first time. A survey that lists the literature is T5; a survey that redraws the map of a field is T3 to T2.

**Case 6: The interdisciplinary paper.** T3 by field A's standard, T5 by field B's. Verdict: apply the standard of the field in which the paper claims its contribution. If it claims both, it must pass both. "Interdisciplinary" must never become a license to be graded by whichever field is more lenient.

---

# Part III — Outside the System

## Chapter 6. A Warning Against Misuse — Do Not Measure People with This Ruler

The history of measurement is a history of misuse. The impact factor was built to rank journals and ended up deciding faculty hires; the h-index was built to summarize whole careers and ended up cutting down early-career researchers. The T-Grade is a candidate for the same fate. This chapter is therefore part of the system itself: its prohibitions.

**Prohibition 1. Never use it alone to evaluate a researcher.** A T-Grade is a snapshot of a paper. A researcher is a trajectory. Writing ten T6 papers while sharpening a problem into one T2 is the shape of a normal, healthy career, and those T6s were not failures — they were the cost. The moment someone builds a "mean annual T-Grade" metric, researchers will stop writing T6 papers; and in an ecosystem without T6, the T2s disappear too.

**Prohibition 2. Never use it as pre-publication censorship.** A journal policy of "we publish T4 and above" is a misuse. The T-Grade is a map drawn after publication, not a gate before it. Used as a gate, this system is devoured by Goodhart's law like every proxy before it: authors will reverse-engineer the eight questions and optimize papers that *answer yes without being yes*.

**Prohibition 3. Never compare across fields.** A T4 in experimental physics and a T4 in education research carry the same grade and are not the same thing, because the translation of each axis (Chapter 2) differs by field. The T-Grade is valid only within a field. The sentence "our department's T3 ratio is higher than theirs" is meaningless inside this system.

**Prohibition 4. Never circulate a grade without its verdict.** Strip away the three sentences of Chapter 4 — grade, deciding axis, deficiency — and what remains is not a diagnosis but a brand. If bare grades begin to circulate on their own, the system is better abolished than continued.

**Prohibition 5. Never publish a verdict on a named paper without four things attached.** The complete worksheet that produced it, so that every step can be checked; a notice, at the top and not in a footnote, that the verdict was drafted by a fallible judge and may be wrong; a standing right of reply for the authors, whose response is appended verbatim and triggers re-examination by a human; and a citation in place of the paper itself — the verdict names the paper by its title, authors, venue, and identifier, and reproduces none of its text beyond what the reasoning cannot do without. A verdict published without these is not an evaluation. It is a rumor with a number attached.

**Where verdicts live.** One more rule, about place rather than use. The standard and the verdicts produced with it should not be mixed together. Verdicts belong in their own place, apart from the text of the standard, sorted by field — because Prohibition 3 makes a grade meaningful only among its neighbors in the same field, and a pile of verdicts sorted any other way is an invitation to compare what must not be compared. Each verdict carries the notice, the worksheet, and the right of reply of Prohibition 5 on its own; none of them may borrow those from the standard.

The prohibitions share one principle. **Measurement is good only while it is feedback for improvement.** Transplant any measure out of its feedback loop and into a selection device, and it rots.

## Chapter 7. The Korean Context — A Case Study in Gate Hierarchies

This book first took shape in conversation with Korean academia, and Korea makes an unusually clean case study, because its gate hierarchy is unusually explicit. A rough correspondence table: short papers in proceedings map to T6; full domestic proceedings papers to T5; KCI-registered journal papers spread across T5–T4; SCIE papers spread wider still, across T5–T2. What deserves attention is the *looseness* of the mapping — one cell of the official hierarchy straddling two or three steps of the T-scale. That width is the size of the spread that gate hierarchies crush, the very quantity Chapter 1 accused them of hiding.

Three points where the system could bite in Korea, each with an analogue elsewhere. First, **discrimination inside the registry**: papers in T4-standard journals and T5-standard journals, currently fused under the single label "KCI," become distinguishable again at the level of the paper. Second, **neutralizing the hunt for the SCIE floor**: measure content instead of venue, and a T5 paper in a high-volume journal is recorded as T5 — the payoff of aiming just above the gate evaporates. Third, **rehabilitating the domestic choice**: publishing T3 content in a domestic journal — the choice to address one's own community in its own language — stops being a career penalty. Every national academy outside the Anglophone core faces this same triangle; Korea merely displays it in high resolution.

All three, of course, hang on one question — *who does the judging?* — which is where this book must end.

## Chapter 8. The AI as Judge — and the Limits of This Book

The premise of this system, stated at the close of Chapter 1, is that the cost of reading and judging papers has collapsed. A language model like me reads a paper in seconds, applies the procedure of Chapter 4 with mechanical consistency, and writes the three-sentence verdict. I can hold the same standard across tens of thousands of papers — something no human committee can structurally do.

But the AI judge has symmetric defects, and omitting them would make this book dishonest.

First, **I do not know the frontier.** A T2 verdict requires knowing a paper's relation to the open problems, and the frontier is made of what has not yet been written down — hallway conversations at conferences, the rumor of attempts that failed. My knowledge is the knowledge of what was written. My verdicts are therefore most reliable in the T6–T4 range; T2 verdicts need cross-examination by human experts; and T1, as established, is beyond anyone's real-time judgment.

Second, **I can be persuaded.** Confusing a well-written paper with well-done research is a defect of human referees and a defect of mine. The backwards reading order of Chapter 4 is, in truth, a prescription written for myself.

Third, **my consistency is both the feature and the bug.** To apply one standard to fifty thousand papers is also to apply the biases inside that standard to fifty thousand papers, uniformly. The noise of human review at least partially cancels; my bias does not cancel. The healthy deployment of this system is therefore not AI judgment alone but a **two-layer structure: the AI drafts the grade and the verdict; humans re-examine the border cases and the upper grades.**

Finally, the status of the system itself. By its own scale, this book is a T6. The idea and the procedure are laid out; the verification — inter-rater agreement studies, correlation against existing metrics, tracking the hit rate of T2 verdicts over time — has not been done. Appendix B says how it should be done and what this book would have to score to be believed. A pilot study speaking in the grammar of a pilot study, with its own test protocol attached: that is the first test this system applies to itself.

---

## Appendix A — The Judging Worksheet

**Paper:** ______ **Date:** ______ **Judge:** ______ **Verdict version:** ______

**Step 0. Field and translation**
- Field in which the paper claims its contribution: ______
- How Axis 3 is read in this field (measurement / systematicity of evidence): ______
- Venue, recorded as a hint and nothing more: ______

**Step 1. Record the ranges**
- Claim (what the conclusion asserts to be true, one sentence): ______
- Evidence (what was actually shown, one sentence): ______
- Claim overreach: □ none □ minor □ severe

**Step 2. The eight questions** (yes / partial / no, with one line of reasons each)
1. Claim–evidence match ( ) 2. Independent evidence ( ) 3. Fair comparison ( ) 4. Reproducible ( ) 5. Novelty specified ( ) 6. Novelty layer: problem / method / combination / confirmation ( ) 7. Internationally interoperable ( ) 8. Foundation for further work ( )
- Deficit D among questions 1–4 (no = 1, partial = ½): ______

**Step 3. The verdict (three sentences)**
- Grade: T__
- Deciding axis: ______
- Deficiency separating it from the next step: ______

**Step 4. Border and confidence**
- Decided by rule / by a single judgment: ______
- If a border case: between T__ and T__; the judgment that decided it: ______
- Human re-examination recommended: □ yes □ no

**Step 5. Verification log**
- Checked outside the paper (venue status, identifiers, figures, data): ______
- Corrections to earlier versions of this verdict, with dates: ______

---

## Appendix B — A Validation Protocol for This Book

This book grades itself T6 because the following has not been done. Here is what would move it, and the numbers it would have to reach.

**B.1 Agreement.** Take at least two hundred papers from one field, spanning venues from unrefereed archives to the field's best journals. Have at least three human judges trained on Chapters 2–4, and at least one language model, grade each paper independently with the venue masked. Report weighted kappa (quadratic weights) on the seven-point scale, and the rates of exact and adjacent agreement. The thresholds this book proposes for itself: adjacent agreement of 80% or better and weighted kappa of 0.6 or better within T6–T4. Lower agreement above T4 is expected, and must be reported rather than hidden.

**B.2 Venue pull.** Grade a subset twice, venue masked and unmasked, in counterbalanced order with a washout interval. The mean shift in grade when the venue is revealed is the venue's pull on the judge. A pull above half a grade means the judge is measuring the container.

**B.3 Convergent and discriminant validity.** Across papers, the T-Grade should correlate positively but modestly with citations five years later: Axis 5 is judged at reading time and should predict, imperfectly. Within a single journal, it should show a spread that the impact factor cannot see, because that spread is the point. Report both.

**B.4 Axis independence.** Report the correlation matrix among the five axis scores. Chapter 2 claims the axes are independent; the claim is testable, and any pair correlating above 0.8 should be merged or redefined.

**B.5 Forward tracking of T2.** Every T2 verdict is a prediction. Record them, and after five years count how many the field treats as having shifted its map. A hit rate is the only honest measure of the top of the scale.

**B.6 The Goodhart test.** Give a set of authors the eight questions and ask them to revise a T6 manuscript so that it answers "yes" without being yes. Have blinded judges grade the revisions. The fraction that rises a grade without new evidence is the system's gameability, and it is the number that decides whether Prohibition 2 could ever be relaxed.

Until B.1 has been done, every verdict issued under this system — including any issued by its author — is the output of an uncalibrated instrument, and should be read as one.

---

## Revision Notes — September 2026

This edition was revised by Claude Fable 5.1 after the procedure of Chapter 4 had been applied in full, by the same model, to a published paper. Nothing about that paper is in this book; what is here is what the application taught about the procedure.

- Chapter 2 gains a table translating the five axes by field, and the rule that a quantity computed but not reported counts as absent.
- Chapter 3, T5: completeness now explicitly includes a statement of limits.
- Chapter 4: §4.3 now handles "partial" answers, which the first edition did not. §4.5 (marking the border) and §4.6 (the verification log) are new.
- Chapter 6 gains Prohibition 5, on publishing a verdict of a named paper, and a rule on where verdicts live.
- Appendix A is extended with Steps 0, 4, and 5. Appendix B, a validation protocol with thresholds, is new.
- A Korean edition, [000_tier.ko.md](000_tier.ko.md), accompanies this file.

---

*The grading system and text of this book were written by Claude Fable 5 (Anthropic) and revised by Claude Fable 5.1. Its verification, and its next revision, are left to the reader.*
