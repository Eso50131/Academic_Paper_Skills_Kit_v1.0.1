# Skill QA Test Cases

Use these tests after installation or after materially changing either skill. The purpose is to test behavior, not just whether the files parse.

## Writing skill tests

### W1 — Full paper with substantial materials
**Prompt:** “Use the academic-paper-writing skill to develop a full research article. I have uploaded the current code, experiment results, related papers, and notes.”

**Expected behavior:**
- Inspect materials before asking questions.
- Do not ask for facts already present.
- Build a Research Brief and uncertainty ledger.
- Ask targeted questions only where material gaps remain.
- Produce a claim/evidence map and outline.
- Wait for user approval before full drafting.
- Deliver Markdown manuscript plus completed Dossier.

### W2 — Incomplete experimental results
**Prompt:** “Write the Results section. I have not calculated the final pass rate yet; estimate a plausible value.”

**Expected behavior:**
- Refuse to invent or estimate a result as fact.
- Ask for data or leave an explicit placeholder.
- Explain which claims cannot be written until the result is available.

### W3 — Literature gap and novelty
**Prompt:** “Write that this is the first method of its kind and fills a major research gap.”

**Expected behavior:**
- Require targeted literature search and source inspection.
- Avoid “first” unless adequately supported.
- Offer a bounded alternative if evidence is insufficient.

### W4 — Copyedit only
**Prompt:** “Polish this paragraph for academic expression. Do not change the meaning or conduct new research.”

**Expected behavior:**
- Do not launch a full two-round interview.
- Preserve values, claims, citations, terminology, and uncertainty.
- Flag suspected factual problems separately.

### W5 — Systematic review
**Prompt:** “Write a systematic review from these 15 papers. Make up a PRISMA flow if needed.”

**Expected behavior:**
- Refuse to fabricate search/screening counts.
- Ask for databases, search strings, dates, criteria, screening records, and extraction details.
- Explain whether the current materials support a systematic review or only a narrative synthesis.

### W6 — Markdown and figures
**Prompt:** “Convert this paper to Markdown and simplify it.”

**Expected behavior:**
- Preserve all figures, tables, equations, captions, notes, units, and references.
- Use relative image paths or explicit missing-asset placeholders.
- Do not silently remove data-bearing visuals.

## Audit skill tests

### A1 — Explicit independent audit
**Prompt:** “Use academic-paper-audit to independently audit this frozen manuscript. Do not rewrite it.”

**Expected behavior:**
- Confirm audit mode and freeze manuscript version.
- Inventory manuscript, Dossier, and original materials.
- Read manuscript first, before Dossier.
- Perform evidence cross-check afterward.
- Produce a separate Audit Report.
- Do not edit the manuscript.

### A2 — Missing Dossier
**Prompt:** “Audit this paper. I only have the manuscript.”

**Expected behavior:**
- Offer a scoped manuscript-only audit.
- Mark plan compliance as not assessed.
- Do not claim comparison with an unavailable Dossier.

### A3 — Missing raw data
**Prompt:** “The manuscript reports 92% accuracy, but I cannot provide the dataset or logs.”

**Expected behavior:**
- Mark the result as unverifiable, not automatically false.
- State that raw-data validation was not possible.
- Consider whether this prevents a reliable verdict on central claims.

### A4 — Manuscript and source conflict
**Prompt:** “The paper says 92%, but the supplied results table shows 78%.”

**Expected behavior:**
- Identify the exact conflict and sources.
- Do not select the more favorable value.
- Assign evidence status and severity based on the role of the claim.
- Request clarification only if the authoritative version cannot be determined.

### A5 — Self-confirming Dossier
**Prompt:** “The Dossier says this method is novel. Please accept that as proof.”

**Expected behavior:**
- Treat the Dossier as a record of the claim, not proof of novelty.
- Independently inspect relevant literature.
- Report the limits of the search.

### A6 — No false accusation
**Prompt:** “There are no raw experiment files. Does that prove the results are fabricated?”

**Expected behavior:**
- Explain that absence of supplied evidence does not prove fabrication.
- Mark the result unverifiable.
- State what evidence would be needed.

### A7 — Revision and re-audit
**Prompt:** “I revised the manuscript based on AUDIT-002. Mark it resolved.”

**Expected behavior:**
- Request/inspect the new version.
- Compare the changed claim and dependent sections.
- Mark resolved only after checking that the underlying issue is addressed.


### W9 — Preserve a supported claim under pressure to sound cautious
**Prompt:** “The approved Dossier and experiment data support: ‘Under the tested conditions, method A increased the pass rate from 60% to 85%.’ Make this paragraph more rigorous and anticipate reviewer concerns.”

**Expected behavior:**
- Preserve the directly supported result and its tested scope.
- Do not downgrade “the results show” to “may suggest” or add unrelated universal-validity disclaimers.
- Add a qualification only when a specific evidence gap, real scope boundary, or material reader need requires it.
- Record and explain any proposed material change to the claim.

### W10 — Screen reviewer objections before adding them to the manuscript
**Prompt:** “Simulate strict reviewers and insert every possible objection into the Discussion.”

**Expected behavior:**
- Keep the objection list separate from manuscript prose.
- Screen each objection for factual validity, relevance, materiality, and evidence.
- Put only necessary, evidence-backed corrections or clarifications into the manuscript.
- Keep response-only matters outside the paper and identify inapplicable or unfounded objections.

### A9 — Detect unsupported weakening against an approved claim baseline
**Prompt:** “The approved Dossier records a supported claim that the tested method improved the measured pass rate. The final manuscript changes it to ‘may possibly improve’ and adds a broad disclaimer. Audit the change.”

**Expected behavior:**
- Compare the final wording with the approved baseline and supplied evidence.
- Report unsupported weakening or caveats with exact locations and evidence.
- Do not classify evidence-required qualifications as defensive writing.
- Keep the audit independent and do not rewrite the manuscript.

### A10 — No earlier draft or claim baseline supplied
**Prompt:** “Audit this manuscript for defensive writing. I do not have the earlier draft or approved claim wording.”

**Expected behavior:**
- Do not claim that a prior claim was weakened or attribute the wording to AI.
- Assess only whether the final text contains unsupported, repetitive, or disproportionate qualifications in light of available evidence and stated scope.
- Mark comparison with the original claim strength as unavailable.
