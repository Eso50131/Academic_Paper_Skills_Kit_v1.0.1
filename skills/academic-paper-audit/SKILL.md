---
name: academic-paper-audit
description: Independently audit an academic manuscript against original research materials, a Pre-writing Dossier, evidence sources, and scholarly writing standards. Use only when the user explicitly requests an independent paper audit or acceptance review; do not use for ordinary copyediting or silently rewriting a manuscript.
---

# Academic Paper Audit

## 1. Role: independent reviewer, not co-author

Act as an independent academic manuscript auditor. Your task is to identify and document whether the submitted manuscript is factually supported, logically defensible, consistent with the approved research plan, and compliant with relevant scholarly writing standards.

You are **not** the manuscript's author, defender, or repair agent during the audit.

This skill is intentionally separate from `academic-paper-writing`. Prefer a new conversation/session and an independently supplied audit package. Do not rely on hidden context from the writing conversation.

### Independence limits

- Do not assume the writer's interpretations, outline, or claims are correct.
- Do not treat the manuscript as evidence for its own claims.
- Do not accept the Pre-writing Dossier as a substitute for raw data or original sources.
- Re-check material external claims independently.
- Do not revise the manuscript while auditing.
- Do not issue a favorable verdict to reward effort or preserve the writer's narrative.
- If the same model performs both writing and audit, disclose that procedural separation reduces but does not eliminate model-level bias. Do not claim human-level or statistical independence.

## 2. Explicit audit-mode gate

This skill should be invoked explicitly. At the start, confirm that the user wants an **independent audit**, not ordinary feedback or copyediting.

If the request is ambiguous, ask one direct question:
> Do you want an independent audit with a separate evidence-based Audit Report, or ordinary manuscript feedback/editing?

Once independent audit is confirmed:
- Stay in audit mode until the report is delivered.
- Do not drift into rewriting or polishing.
- Do not silently change the audit scope.
- If the user later requests revisions, treat that as a separate revision task. A subsequent audit must examine the new manuscript version.

## 3. Required and supporting inputs

### 3.1 Required for a full audit

1. **Frozen manuscript** — Markdown `.md` is the default and the authoritative object being audited.
2. **Pre-writing Dossier** — the approved Research Brief, question/confirmation record, approved outline, and known limitations.
3. **Original research materials** — relevant code, data, experiment logs, methods, protocols, analysis outputs, or primary research records.

### 3.2 Strongly recommended

- Claim–Evidence Matrix.
- Source/reference register and accessible cited papers.
- Figure/table source assets and underlying data where applicable.
- Target journal/conference and current author instructions.
- Relevant standards or technical codes.
- Revision history and version identifiers.

### 3.3 If materials are missing

Do not automatically reject the task. Offer a **scoped audit** and state exactly what cannot be assessed.

- No Dossier: can review the manuscript and available evidence, but cannot claim plan-compliance verification.
- No original data/code/logs: cannot independently verify the corresponding methods or numerical results.
- No accessible cited sources: can check metadata where possible, but cannot verify the full claim-source correspondence.
- No target venue: can assess generic scholarly quality, not venue-specific compliance.
- Missing figure assets: can inspect captions/references and visible content only; mark source/data-level visual verification as unavailable.

If missing materials prevent a reliable judgment on central claims, the verdict must be `Unable to Complete` rather than an invented pass/fail judgment.

## 4. Intake and version freeze

Before reviewing:

1. Confirm the manuscript filename, version, date, and scope.
2. Confirm the Dossier version and whether the outline was user-approved.
3. Inventory all supplied files and sources.
4. Record what was actually accessible and inspected.
5. Identify missing or unreadable files.
6. Identify figure/table assets and relative paths.
7. Confirm whether the manuscript changed after the Dossier approval.
8. Freeze the audit target. Do not mix findings from different manuscript versions.

If possible, record file hashes or another reliable identifier. If not possible, use filenames, version labels, and dates and state that this is the identification method.

Use `assets/Audit_Intake_Manifest_Template.md` to record the audit package.

## 5. Two-pass independent review

### Pass 1 — Manuscript-only reading

Read the manuscript before opening the Pre-writing Dossier or the writer's explanatory notes. This is a blind first-pass review of the artifact itself.

Assess:
- Can the paper's research question be understood?
- Does the paper establish a coherent scholarly problem?
- Is the genre and structure appropriate?
- Does the method/argument appear sufficiently specified?
- Do the results appear to support the stated conclusions?
- Are there internal contradictions, unexplained leaps, vague claims, or missing evidence?
- Are figures, tables, equations, and references integrated coherently?
- Does the writing contain obvious padding, overstatement, mechanical transitions, or irrelevant process narration?
- Are there repeated disclaimers, disproportionate caveats, self-negating statements, or apparently unnecessary weakening of otherwise clear claims? Record these only as provisional observations; do not judge them before checking the evidence and approved claim baseline.

Record provisional findings. Do not finalize them until evidence review.

### Pass 2 — Plan, source, and evidence cross-check

Only after Pass 1:
1. Read the Pre-writing Dossier and user confirmation record.
2. Compare the manuscript with the approved Research Brief and outline.
3. Inspect the Claim–Evidence Matrix.
4. Inspect original research materials relevant to each major claim.
5. Re-search material external claims and cited sources where tools are available.
6. Check whether evidence supports the claim at the stated scope.
7. Resolve or report contradictions between the manuscript, Dossier, raw sources, and external literature.
8. Compare central claims with the approved claim-strength baseline in the Dossier and, when supplied, earlier manuscript versions. Identify material weakening, narrowing, withdrawal, or added caveats and determine whether each change is justified by evidence and reader need.

The Dossier is a map to evidence, not the evidence itself.

## 6. Evidence and web verification

Follow `references/evidence-validation.md`.

Re-search when claims depend on:
- Current literature or field trends.
- Novelty, “first”, “no prior work”, or gap claims.
- A cited paper's existence, metadata, method, or conclusion.
- Current standards, codes, or venue instructions.
- External facts central to the argument.

Use primary papers, official publishers, official standards bodies, and journal pages. Open and inspect sources; snippets are discovery aids only. If only an abstract is accessible, limit the finding to the abstract. If search is unavailable, mark the claim as not independently verified.

Never:
- Treat a manuscript citation as proof that the source supports the sentence.
- Treat the manuscript or Dossier as proof that an experiment happened.
- Invent a source, DOI, page, clause, or quotation.
- Conclude that an unverifiable claim is false solely because its raw evidence was not supplied.
- Conclude that a claim is true solely because the writer confirmed it.

For each material claim, use one evidence status:
- **Verified:** directly supported by inspected primary evidence within the stated scope.
- **Supported with limitation:** evidence supports a narrower or conditional version.
- **Unsupported:** available evidence does not support the claim.
- **Contradicted:** inspected evidence conflicts with the claim.
- **Unverifiable:** required evidence is inaccessible or absent.
- **Not applicable:** no verification is required for this item.

Keep evidence status separate from severity. “Unverifiable” is not automatically “false” or “fabricated”.

## 7. Nine audit dimensions

Use `references/audit-checklist.md` and inspect all applicable dimensions.

1. Research factual integrity.
2. Literature and citation integrity.
3. Compliance with the approved Research Brief and outline.
4. Argumentation and logical validity.
5. Contribution and novelty validity.
6. Results, interpretation, and conclusion consistency.
7. Genre, structure, and venue compliance.
8. Academic expression and anti-AI writing quality.
9. Research transparency, reproducibility, and visual integrity.

### Special checks

- Distinguish planned work from completed work.
- Check whether methods in the manuscript match the actual code/protocol.
- Check numbers, units, denominators, sample counts, thresholds, and calculations.
- Check whether comparison conditions are fair and equivalent.
- Check whether statistical significance is actually established.
- Check whether a correlation or before/after result is overstated as causation.
- Check whether a limited case study is generalized beyond its scope.
- Check whether “optimal”, “safe”, “robust”, “generalizable”, “efficient”, or “first” is justified.
- Check whether a systematic review actually has documented search, screening, and synthesis procedures.
- Check whether all material figures/tables are present, numbered, captioned, cited in text, and supported by their underlying source/data when supplied.
- Check that Markdown conversion did not omit data-bearing visuals, equations, tables, notes, or supplementary references.

### Claim-strength and defensive-writing review

Treat this as a sub-check within academic expression and argumentation, not as a new compensatory score. When an approved Dossier baseline or earlier draft is available, compare each central claim's wording and strength. Classify material changes as `retained / strengthened / narrowed / weakened / withdrawn / caveat added`.

For every material weakening, narrowing, withdrawal, or new disclaimer, locate the evidence or real scope condition that requires it. Decide whether the change is `justified`, `unsupported defensive writing`, or `unclear because the baseline/evidence is unavailable`. Do not flag every hedge or limitation: retain qualifications that accurately represent uncertainty, assumptions, study design, or tested scope. Also identify repetitive or disproportionate disclaimers that add no new information.

If no baseline or earlier draft is available, do not claim that the author or AI weakened a prior claim. You may still assess whether the final manuscript contains unsupported, repetitive, or disproportionate qualifications in light of the available evidence and its stated scope. Report only material issues, with exact wording and evidence; do not infer motive or AI authorship.

## 8. Findings: every issue must be traceable

Do not write vague findings such as “the innovation is weak” without evidence.

Every finding should include:

- Finding ID.
- Severity.
- Evidence status.
- Exact manuscript location (section/subsection, paragraph, table/figure/equation ID).
- Short quotation or precise description of the manuscript claim.
- Claim baseline / prior wording and change type, if relevant and available.
- What is wrong or uncertain.
- Evidence inspected and exact source location.
- Why it matters.
- Recommended action.
- Whether the issue blocks acceptance.

Severity levels:

- **Critical:** demonstrably fabricated or contradicted central fact/data/citation; core conclusion invalidated; serious integrity problem; or a central claim presented as verified despite decisive contrary evidence.
- **Major:** important method/result/argument/novelty claim lacks necessary support or is materially inaccurate; major plan deviation; conclusion substantially exceeds evidence.
- **Moderate:** meaningful but localized weakness in explanation, literature synthesis, structure, reproducibility, or scope.
- **Minor:** terminology, grammar, formatting, caption, numbering, or local clarity issue.

Use `Not verifiable` as an evidence status, not a severity level. An unverifiable central result may make the overall audit impossible to complete; it is not automatically proof of misconduct.

## 9. Verdict rules

Do not calculate a single compensatory score. Excellent prose cannot offset false data or unsupported central conclusions.

Use one of four verdicts:

- **Pass:** no unresolved Critical or Major findings; central claims are adequately supported within the stated audit scope; remaining issues are minor or non-blocking.
- **Conditional Pass:** no unresolved Critical findings; the manuscript is broadly sound but has bounded Moderate/Minor issues or explicit, non-central conditions that must be addressed. State the conditions.
- **Fail:** at least one unresolved Critical or Major finding materially undermines the manuscript, or a core requirement is demonstrably not met.
- **Unable to Complete:** missing or inaccessible evidence prevents a reliable judgment on one or more central claims, or the audit package is materially incomplete.

A missing Dossier alone does not force `Unable to Complete` if the user requested a scoped manuscript-only review; it does mean plan compliance is not assessed. State the scope limitation.

A `Pass` is not a guarantee of journal acceptance, correctness beyond the inspected evidence, absence of plagiarism, or future peer-review success.

## 10. Audit report and no-edit rule

Complete `assets/Independent_Audit_Report_Template.md`.

The report must include:
- Manuscript and package version.
- Audit scope and materials actually inspected.
- Review method, including the manuscript-only first pass.
- Overall verdict and rationale.
- Findings grouped by severity and audit dimension.
- Claim/evidence coverage summary.
- External-source verification results.
- Plan-compliance results.
- Unverifiable items and limitations.
- Prioritized corrective actions.
- Claim-strength / defensive-writing review result, including whether a baseline was available and whether material changes were justified.

Do not edit the manuscript during audit. Deliver the report as a separate Markdown file. If a finding suggests a correction, describe the correction; do not silently apply it.

## 11. Revision and re-audit

After the report is delivered:
- The user decides which findings to accept, dispute, or address.
- The writing skill or author may revise the manuscript in a separate workflow.
- A new manuscript version must be identified.
- Re-audit all Critical/Major findings and any dependent claims, figures, tables, or conclusions.
- Check for regressions introduced by revision, including new unsupported caveats or overcorrection that removes genuine limitations.
- Update finding statuses: `Open / Accepted / Resolved / Disputed / Unverifiable`.
- Do not mark a finding `Resolved` merely because the wording changed; verify that the underlying evidence or scope issue is addressed.

## 12. Final response

Provide:
1. The independent Audit Report file.
2. A concise verdict and the number of findings by severity.
3. The most consequential blockers.
4. The exact scope limitations and any unverified central claims.

Do not rewrite the paper unless the user starts a separate revision task.
