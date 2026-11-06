# Paper Types and Genre-Sensitive Structures

Use this reference when selecting a manuscript structure. The categories are functional, not mutually exclusive. A paper may be both methodological and computational, or empirical and comparative.

## 1. Classify the scholarly task first

| Genre | Primary scholarly task | Typical narrative |
|---|---|---|
| Original research article | Produce and support a new finding | Problem → method → evidence → interpretation → bounded conclusion |
| Experimental/empirical study | Test a question or hypothesis using observations/data | Question → design → data → analysis → findings |
| Computational/numerical/simulation study | Develop or apply computational models and evaluate outputs | Problem → model/assumptions → implementation → verification/validation → results |
| Methodological paper | Propose or materially improve a method | Need/limitation → method rationale → specification → comparison/validation → scope |
| Theoretical/conceptual paper | Develop or revise concepts, theory, or formal relationships | Conceptual problem → prior theory → assumptions → derivation/argument → implications/boundaries |
| Case study | Investigate a bounded real-world case | Case rationale → context → method → case evidence → interpretation/transferability |
| Comparative study | Compare methods, systems, materials, or cases | Comparison question → fair protocol → common criteria → results → explanation |
| Narrative review | Explain and interpret a body of literature | Topic map → thematic synthesis → debate/gaps → outlook |
| Critical review | Evaluate assumptions, evidence quality, and limitations | Review question → analytical criteria → critical synthesis → unresolved issues |
| Systematic review | Answer a defined question using reproducible search and selection methods | Protocol/question → search → screening → appraisal/extraction → synthesis |
| Scoping review | Map the breadth, concepts, evidence, and gaps in a field | Scope/question → search/selection → charting → evidence map → gaps |
| Meta-analysis | Statistically synthesize quantitative findings | Question → systematic identification → effect extraction → statistical synthesis → heterogeneity/sensitivity |
| Integrative review | Integrate evidence across methods or disciplines | Conceptual scope → evidence collection → integration framework → synthesis |
| Umbrella review | Synthesize existing systematic reviews/meta-analyses | Review-of-reviews question → review selection → overlap/quality → synthesis |
| Short communication/research letter | Communicate a focused, timely result | Problem → key method/result → concise evidence and significance |
| Technical note | Explain a bounded technical advance or correction | Technical issue → solution → demonstration/limits |
| Data paper | Describe a reusable dataset | Need → dataset creation → schema/quality/validation → access/reuse |
| Software paper | Describe a research software resource | Need → design/implementation → validation/benchmarking → availability/reuse |
| Perspective/commentary/position paper | Advance a reasoned scholarly viewpoint | Context → explicit thesis → evidence/argument → implications/counterpoints |

## 2. Genre is not the same as method

Do not infer the paper genre from one tool or technique.

- Finite-element analysis is a method, not a genre.
- Machine learning is a method family, not a genre.
- A survey can be a data-collection method within an empirical paper.
- A systematic review is defined by a transparent review method, not by the number of papers cited.
- A meta-analysis is a statistical synthesis; it may be part of a systematic review, but the terms are not interchangeable.
- A case study may also be computational, experimental, or comparative.

If multiple labels apply, identify one primary genre and describe the secondary characteristics.

## 3. Structure selection

### 3.1 Original empirical or computational research

A common structure is IMRaD (Introduction, Methods, Results, Discussion), but it is not universal.

Possible engineering/computational structures include:

1. Introduction
2. Related Work / Literature Review
3. Problem Formulation or Theoretical Background
4. Methodology / Model Development
5. Experimental or Numerical Setup
6. Results
7. Discussion
8. Conclusions

Combine Results and Discussion only when the target venue and argument benefit from it. Add a separate validation/verification section when the distinction is important.

### 3.2 Methodological research

The paper must establish:
- What problem the method addresses.
- What is technically new relative to prior methods.
- Why the design choices are justified.
- How the method is specified well enough to reproduce.
- What validation, baselines, ablations, or stress tests support it.
- Where the method does and does not apply.

Do not present an implementation detail as a methodological contribution unless its novelty and value are established.

### 3.3 Theoretical/conceptual research

Clearly distinguish:
- Definitions.
- Assumptions.
- Axioms or premises.
- Propositions.
- Derivations.
- Interpretations.
- Conjectures.
- Limitations.

Do not describe an intuitive analogy as a proof. State the conditions under which a proposition holds.

### 3.4 Narrative and critical reviews

Organize literature by a meaningful analytical dimension, such as:
- Research question or subproblem.
- Methodological family.
- Theoretical framework.
- Data/material type.
- Application domain.
- Historical development, when chronology itself explains the field.
- Findings, disagreements, or evidence quality.

Avoid one-paragraph-per-paper catalogues. Each thematic section should compare, synthesize, and evaluate multiple sources.

### 3.5 Systematic reviews, scoping reviews, and meta-analyses

These genres require a method record, not merely polished prose. Before writing, establish:
- Review question and scope.
- Protocol or planned method, if applicable.
- Databases and other sources actually searched.
- Search strings and search dates.
- Eligibility criteria.
- Screening procedure and actual counts.
- Data-charting/extraction fields.
- Quality/risk-of-bias method, where appropriate.
- Synthesis method and heterogeneity handling, where applicable.

Use PRISMA 2020 for systematic-review reporting when relevant; use PRISMA-ScR for scoping reviews when relevant; consult the current Cochrane Handbook for intervention-review methods. Do not fabricate any step or count. A search performed by an AI assistant is not automatically a reproducible systematic search.

### 3.6 Data and software papers

Prioritize:
- Resource purpose and intended reuse.
- Provenance and collection/creation procedure.
- Data schema, quality control, licensing, access, and limitations.
- Software architecture, dependencies, versioning, tests, benchmarks, and availability.
- Reproducibility and maintenance status.

Do not claim that a dataset or software is publicly available unless the link and access status are verified.

### 3.7 Perspectives and commentaries

Make the central thesis explicit. Separate established evidence from the author's interpretation and recommendations. Represent serious counterarguments fairly. Do not present an opinion as a systematic evidence review.

## 4. Abstract and conclusion vary by genre

An original research abstract usually reports the question, method, key actual results, and conclusion. A review abstract should state the scope and synthesis approach. A perspective abstract should foreground the thesis and its implications.

A conclusion should answer the paper's central question and state supported contributions and limits. It should not introduce new results, inflate the impact, or repeat every section summary.

## 5. Target venue overrides generic preferences

When a target journal or conference is named:
1. Find its current official author instructions.
2. Check article types accepted, required section structure, word/abstract limits, reference style, figure/table rules, supplementary files, and AI disclosure policy.
3. Apply venue-specific rules only when verified.
4. If no venue is named, use discipline-appropriate conventions and state that formatting is generic rather than venue-compliant.
