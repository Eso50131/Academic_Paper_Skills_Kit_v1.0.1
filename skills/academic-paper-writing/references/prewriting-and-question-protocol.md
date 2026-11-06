# Pre-writing and Question Protocol

## 1. Purpose

Pre-writing establishes a reliable shared understanding of the actual research before a full manuscript is drafted. It is not a generic intake form and not an excuse to interrogate the user about information already present in files.

## 2. Material-first sequence

1. Identify the requested writing mode and paper genre.
2. Inventory the available files and connected sources relevant to the task.
3. Read relevant materials before asking questions.
4. Extract facts, methods, results, citations, figures, and unresolved issues.
5. Compare versions and detect contradictions.
6. Create a short uncertainty ledger.
7. Ask only questions whose answers materially affect the research description, paper structure, evidence, or conclusions.

For a broad file set, begin with semantic/topic search or document navigation and then inspect the specific primary sources. For code/data claims, inspect the relevant code, data, logs, or result files when available. Do not treat filenames or file summaries as proof of unseen contents.

## 3. Research Brief schema

The Research Brief should cover:

| Field | What to capture |
|---|---|
| Paper identity | Working title, genre, discipline, language, target venue |
| Research object | What is studied and at what scale |
| Context | Only background necessary to understand the problem |
| Core question | The precise question the paper answers |
| Objective | What the study aims to achieve |
| Scope | Included conditions and explicit exclusions |
| Prior work | Relevant methods, evidence, debates, and source status |
| Gap/problem | What remains unresolved and why it matters |
| Actual method | What was implemented/performed, not what was planned |
| Data/experiments | Data source, sample, conditions, controls, metrics |
| Results | Actual results and their provenance |
| Contribution | New capability, finding, method, evidence, or interpretation |
| Boundaries | Assumptions, applicability, limitations, known failures |
| Unknowns | Missing or conflicting facts and required follow-up |

## 4. Question Round 1 — Research discovery

Normally ask 5–10 consolidated questions, but do not force the number. Questions should be grouped and concise. Avoid asking what the source material already answers.

Suggested domains:

1. **Paper positioning:** What kind of academic paper is intended? What field, language, target venue, and audience?
2. **Research object/context:** What exactly is being studied? Which conditions or population/system are in scope?
3. **Core problem:** What specific scientific or technical problem motivates the study?
4. **Objective/scope:** What does the research aim to establish or demonstrate? What is outside scope?
5. **Actual route/method:** What methods, models, algorithms, theories, or procedures were actually used?
6. **Data/experiments:** What data, samples, experimental conditions, baselines, controls, and metrics were used?
7. **Actual findings:** What results have been obtained? Include negative, null, mixed, or unexpected outcomes.
8. **Contribution:** What does the user believe is new, and what evidence supports that view?

Use follow-up prompts only where they clarify the main question. Let the user answer “unknown”, “not yet performed”, or “not applicable”. Do not imply that planned work has already happened.

## 5. Question Round 2 — Targeted validation

After Round 1, compare the user's answers with source materials and the emerging claim/evidence map. Ask only high-impact questions that remain.

Possible domains:
- Exact model architecture, components, inputs, outputs, losses, assumptions, and parameter settings.
- Method-selection rationale and whether alternatives were actually tested.
- Experimental design, baselines, fairness, controls, repetitions, and statistical analysis.
- Result provenance, calculations, denominators, thresholds, and failure cases.
- Whether proposed mechanisms are measured, theoretically derived, or speculative.
- Prior-work comparison and novelty boundaries.
- Generalization scope and untested conditions.
- Which contribution should be foregrounded and which should be omitted.
- Contradictions between the manuscript, code, logs, tables, and user statements.

Usually ask 5–10 grouped questions only if that many consequential uncertainties remain. Do not repeat Round 1. If only one or two critical issues remain, ask only those.

## 6. When two rounds are not enough

Two rounds are a normal discovery design, not a guarantee that all research facts become known. If critical information remains missing:
- Request the exact source file or a precise user confirmation.
- Mark the item as unresolved.
- Narrow or qualify the manuscript claim.
- Use a visible placeholder if the user wants a draft before the fact is available.
- Do not silently infer the missing information.

For highly complex work, a later focused clarification may be necessary. Explain why it is needed rather than hiding uncertainty.

## 7. Claim–Evidence Matrix

Create a matrix before drafting. Each major claim should have:
- A unique ID.
- Exact or concise claim wording.
- Claim category (background, prior-work, method, data, result, interpretation, novelty, conclusion).
- Evidence source and exact location.
- Verification state.
- Scope/qualification.
- Planned manuscript section.

A claim may be:
- User-confirmed but not independently verified.
- Supported by inspected primary evidence.
- Supported only within a limited scope.
- Pending verification.
- Unsupported or contradicted.

The matrix is an internal control and a handoff artifact, not necessarily part of the published manuscript.

## 8. Outline and approval gate

Before full drafting, present:
1. Paper profile and primary genre.
2. One-paragraph central thesis.
3. Narrative arc: problem → prior work → gap → method/argument → evidence → interpretation → conclusion.
4. Detailed section/subsection outline.
5. Each section's purpose, key claims, evidence, and transition.
6. Claim–Evidence Matrix.
7. Unresolved facts and proposed handling.

Ask the user to confirm or revise the Research Brief and outline. A clear affirmative approval is required for full drafting. If the user requests a waiver, record it and do not upgrade uncertain facts to confirmed facts.

## 9. Dossier handoff

Complete `assets/Prewriting_Dossier_Template.md`. Include:
- A structured summary.
- The approved outline and its version.
- A record of Round 1 and Round 2 questions and the user's answers for material facts.
- Exact user wording or faithful quoted excerpts for key confirmations when possible.
- Corrections the user made to the AI's earlier interpretation.
- Unresolved items and excluded claims.
- Source register and evidence matrix.
- Approval status and date/version.

Do not dump the entire chat transcript by default. A concise structured record is easier to audit. Preserve relevant original user statements for material claims; do not erase ambiguity during summarization.

## 10. Scope-sensitive shortcuts

- **Copyedit only:** no full interview; preserve meaning and flag suspected factual issues separately.
- **Single-section drafting:** inspect the relevant evidence and ask only section-critical questions.
- **Outline-only task:** stop after outline and approval; do not draft the manuscript.
- **Full manuscript:** complete the full process unless the user explicitly waives a gate.
