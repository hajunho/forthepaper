# Verdict 001 — "One Movie, Two Different Perspectives"

*A worked application of the T-Grade procedure in [000_tier.md](000_tier.md), Chapter 4 and the Appendix worksheet.*

---

## The Paper

| | |
|---|---|
| **Title** | 하나의 영화, 서로 다른 두 시선 (One Movie, Two Different Perspectives) |
| **Authors** | 김자미 (Kim Jamee), 정재림 (Jeong Jairim) — Korea University |
| **Venue** | 한국어문교육 (Korean Language and Literature Education) No. 45, pp. 167–190, 2023. KCI-registered journal. |
| **DOI / ID** | https://doi.org/10.24008/klle.2023..45.006 · KCI FI003019539 |
| **History** | Presented at the 한국어문교육연구소 conference (7 Jan 2023); submitted 7 Oct 2023; accepted 9 Nov 2023. |
| **Field for grading** | Education research (convergence / teacher education). Axis 3 is translated into *systematicity of evidence* as Chapter 2 prescribes. |
| **Judge** | Claude Fable 5.1 (Anthropic) |
| **Date** | 25 September 2026 |

Read backwards, per §4.1: conclusion and abstract first, then Chapter 4 (results), then Chapter 3 (method), and only then the introduction and theoretical background.

---

## Step 1. Record the Ranges

**Claim** (what the conclusion asserts to be true, one sentence):
Pre-service Korean-language teachers approach the AI film *Her* as a literary text, pre-service informatics teachers approach it through AI technology and its practical risks, and this difference in perspective yields four implications for how AI convergence education should be designed and how pre-service teachers should be supported.

**Evidence** (what was actually shown, one sentence):
Forty graduate students in one teacher-education program (25 Korean-education, 15 computer-education, fall 2022) each wrote three or more questions after watching *Her*; nouns extracted from the questions with KoNLPy/Okt were rendered as one word cloud per group, and about ten questions were quoted and interpreted by the authors.

**Claim overreach:** ☐ none ☑ **minor** ☐ severe

The descriptive core of the claim (the two groups emphasized different things) is supported at the level the evidence allows. The overreach is in three places:

1. The abstract states the difference as a finding ("It was found that…") on the strength of two word clouds with no reported frequencies, no question counts, and no coding scheme applied to both groups. The comparison is illustrated, not measured.
2. The four implications (clear goals, teacher baseline knowledge, co-design/team teaching, recognizing difference) are presented as derived from the analysis. They are reasonable positions, but nothing in the data tests them; they would read identically if the word clouds had come out the other way.
3. The final sentence claims the study "showed that effective convergence education can be sought based on differences in perspective." That is the grammar of possibility, which is honest for this grade, but "showed" is doing more work than the evidence supports.

---

## Step 2. The Eight Questions

| # | Question | Answer | Notes |
|---|---|---|---|
| 1 | Claim–evidence match (rigor) | **partial** | Descriptive difference is supported; the implications are not tested by the design. |
| 2 | Evidence independent of the author's impressions (quantitativeness / systematicity) | **partial** | The NLP pipeline produces evidence independent of impression, but the paper reports no numbers from it: no total question count, no per-group noun frequencies, no normalization for the 25 : 15 group-size imbalance. The word cloud is the only output. The reading of *why* "사만다" outranks "테오도르" in the CS group is authorial inference. |
| 3 | Comparisons exist and are fair (rigor) | **partial** | The two-group comparison is the design itself, and both groups saw the same film after the same lecture. But the analysis is asymmetric: Korean-education questions are sorted into fact / value / literary categories (§4.2.1), while computer-education questions are read one student at a time with no category scheme (§4.2.2). Whether the same categories occur in the CS group is never asked. No second coder, no agreement statistic. |
| 4 | Information for third-party reproduction complete (reproducibility) | **partial** | Procedure is well specified: Python 3.8, KoNLPy Okt, normalization rules with examples, dictionary additions with examples, five-step pipeline in [그림 1]. Missing: the question corpus, the stopword list, the full custom dictionary, and the number of questions collected. A third party could rerun the pipeline but not on these data. |
| 5 | Novelty specified against related work (novelty) | **partial** | The gap is stated (little research on pre-service, as opposed to in-service, teachers' convergence competence). Prior work on disciplinary differences in reading the same text, or on text-mining student-generated questions, is not surveyed, so the priority of the design is asserted rather than located. |
| 6 | Novelty layer | **combination** | A known method (noun extraction + word cloud) applied to a new object (questions from two majors on one AI film). The framing question, *what do different majors see in the same text before we ask them to converge*, has a problem-layer flavor, but the paper treats it as an exploratory comparison rather than developing it. |
| 7 | Verification interoperable with international standards (the T3 gate) | **no** | No shared metric, benchmark, or effect size. Literature is almost entirely domestic. Nothing here can be compared directly with a study run elsewhere. |
| 8 | Next study can be built on this conclusion (consequence) | **partial** | The protocol (shared film → student-generated questions → same analysis for both majors) is reusable and cheap, and the fact / value / literary typology is a usable coding scheme if applied to both groups. The conclusion itself, that different majors notice different things, is close to common sense; what could be built on is the instrument, not the finding. |

---

## Step 3. The Verdict

**Grade: T6 (Pilot)**, at the T6/T5 border.

**Deciding axis:** Quantitativeness, translated for the field as systematicity of evidence. An NLP pipeline was built and run, and then its output was reported only as a picture. No count, frequency, or proportion appears anywhere in the paper, the two groups differ in size by a factor of 1.7 without normalization, and the qualitative coding is applied to one group only. Chapter 3's diagnostic signals for T6 are all present: the sample is too small for a statistical claim, there is no baseline beyond the two groups themselves, the evaluation is the authors' interpretation, and the conclusion speaks in the grammar of possibility. What pulls toward T5 is completeness. The narrative is full (problem, theory, method, results, conclusion), the method section is unusually careful for the venue, and the paper passed journal review. What holds it at T6 is that T5 requires "experiments and numbers"; here the numbers were computed and withheld. There is also no limitations section at all, where T5 expects a brief one.

**Deficiency separating it from the next step up (T5):** Report the analysis that was already done. A table of total questions per group and the top-20 nouns per group as proportions, not raw counts, would move the word clouds from illustration to evidence. Apply the fact / value / literary coding to both groups, have a second coder rate a subset, and report agreement. Add a limitations paragraph that names the sample size, the single-site single-semester design, the instructor-as-researcher relationship to both cohorts, and the 25 : 15 imbalance. With those changes and no new data collection, this paper is T5. To reach T4 it would need a balanced sample, a coding scheme fixed before reading, and a conclusion that separates what the data show (the groups differ) from what the authors recommend (the four implications).

---

## Notes That Are Not Deductions

Recorded per Chapter 3: a T6 paper speaking T6 language is a match, not a fault.

- **The design is good.** Asking pre-service teachers of two majors to generate questions about one shared text *before* asking them to co-design a lesson is a sensible and inexpensive way to surface the perspective gap that convergence education tends to paper over. The finding that Korean-education students read *Her* as a literary text while computer-education students "never let go of the thread that the AI is a language model trained on large data" is vivid and plausible, and the quoted questions (1)–(10) make it concrete.
- **The method section is above the grade.** Normalization rules with examples, dictionary additions with examples, and the tool versions are more than most papers at this venue provide. The reproducibility gap is the data, not the procedure.
- **The existential / practical risk distinction** (from 이상욱 2020) gives the paper a usable lens, and the observation that Korean-education students' value questions covered both risk types while CS students' questions clustered on practical risk is the paper's most interesting specific result. It deserves a count.
- **Venue hint.** Chapter 7 maps KCI-registered journal papers to a T5–T4 spread. This paper falls one step below that spread. That is the system working as designed: venue is a hint, not a verdict, and the spread inside "KCI-registered" is exactly the quantity the T-Grade exists to make visible.

---

## 판정문 (Korean summary of the three sentences)

**등급: T6 (파일럿), T6/T5 경계.**

**결정 축:** 정량성(이 분야에서는 근거의 체계성). 자연어 처리 파이프라인을 구축·실행했으나 결과가 워드클라우드 그림으로만 제시되고, 질문 총수·명사 빈도·집단별 비율이 본문 어디에도 없다. 25명 대 15명의 집단 크기 차이가 보정되지 않았고, 사실·가치·문학 질문 분류는 국어교육전공에만 적용되었다. 서사의 완결성과 꼼꼼한 방법 기술은 T5를 향하지만, T5가 요구하는 "수치가 있는 검증"이 없고 한계 절도 없다.

**다음 단계(T5)와의 차이:** 이미 수행한 분석을 표로 보고하면 된다. 집단별 질문 수, 상위 명사 20개의 비율, 두 집단 모두에 동일한 질문 유형 분류 적용, 제2 코더와 일치도, 그리고 표본 크기·단일 기관·연구자=담당 교수 관계·집단 불균형을 명시한 한계 절. 새 데이터 없이 이 수정만으로 T5에 도달한다.

---

*This verdict was drafted by an AI judge and is subject to the two-layer structure described in Chapter 8 of the manuscript: the AI drafts, humans re-examine. Per Prohibition 4, this grade should not circulate without the three sentences above. Per Prohibition 1, it says nothing about the authors.*
