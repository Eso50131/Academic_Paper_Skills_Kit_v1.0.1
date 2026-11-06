# Evidence Validation Protocol for Independent Audit

## 1. What counts as evidence?

Match evidence to claim type.

| Claim type | Appropriate evidence |
|---|---|
| User's actual implementation | Source code, configuration, versioned repository, execution logs, technical records, user confirmation |
| Dataset/sample claim | Original dataset, data dictionary, acquisition protocol, sample manifest |
| Numerical result | Raw/processed data, reproducible calculation, analysis script, experiment log |
| Method/theory claim | Original paper, formal derivation, official technical specification |
| Literature-state claim | Relevant primary papers and a sufficiently broad search strategy |
| Standard/compliance claim | Current official standard/code and applicable clause |
| Venue requirement | Current official author instructions or editorial policy |
| Figure claim | Original figure, underlying data, script, caption, and source attribution |

A manuscript sentence is not evidence for itself. A Dossier is a research map, not a raw source. A user's confirmation is important evidence of what the user asserts, but it does not independently validate a numerical dataset if that dataset is available for inspection.

## 2. Evidence states

Use one of:

- **Verified:** inspected primary evidence directly supports the claim within the stated scope.
- **Supported with limitation:** evidence supports a narrower or conditional version.
- **Unsupported:** available evidence does not support the claim.
- **Contradicted:** inspected evidence conflicts with the claim.
- **Unverifiable:** necessary evidence is missing or inaccessible.
- **Not applicable:** no evidence check is required.

Do not collapse “unverifiable” into “false”. Do not collapse “user-confirmed” into “independently verified”.

## 3. Search protocol

For external claims:
1. Extract the exact proposition to verify.
2. Identify the most direct source type.
3. Search primary publisher/official sources.
4. Open the source and inspect the relevant passage, table, figure, or clause.
5. Record bibliographic metadata and access date.
6. Compare the source's actual scope with the manuscript wording.
7. State what could not be verified.

For novelty claims, broaden terminology and search adjacent disciplines. A few search results cannot establish that no prior work exists.

For current standards and journal policies, check the issuing organization or official venue page and record version/effective date.

If search tools are unavailable, list the exact claims not independently checked. Do not write “verified by literature search”.

## 4. Quantitative verification

For every important numerical claim, inspect:
- Raw source and file/version.
- Units and conversions.
- Numerator and denominator.
- Sample size and exclusions.
- Aggregation and averaging method.
- Thresholds and pass/fail definitions.
- Rounding and significant digits.
- Missing values and outlier treatment.
- Statistical test, assumptions, confidence interval, and p-value where relevant.
- Whether comparison conditions are equivalent.

Recalculate where the data and tools permit. If only a summary table is supplied, state that raw-data verification was not performed.

## 5. Method and implementation verification

Compare manuscript description against actual implementation:
- Model/algorithm name and architecture.
- Input/output representation.
- Loss/objective function.
- Training/inference procedure.
- Hyperparameters and configuration.
- Data preprocessing.
- Numerical solver/version and settings.
- Assumptions and boundary conditions.
- Evaluation metrics and acceptance criteria.

Do not infer an implementation from common practice. If code is absent or incomplete, mark the relevant implementation claim as unverifiable.

## 6. Literature verification

For each material reference:
- Existence and metadata.
- Publication status (peer-reviewed, preprint, withdrawn, corrected, retracted).
- Relevance to the claim.
- Exact method/result being attributed.
- Whether the manuscript overstates or misrepresents the source.
- Whether a more direct original source is available.

If the source is retracted or corrected, report the status and its implications.

## 7. Visual verification

For each figure/table:
- Confirm it exists in the delivered package.
- Confirm numbering and in-text reference.
- Inspect caption, legend, axes, units, sample count, notes, and source.
- Compare plotted/table values with supplied source data when available.
- Check for unexplained cropping, missing panels, inconsistent scales, or unsupported annotations.
- Confirm that Markdown image paths resolve when the environment permits.
- If source assets are absent, report the exact limitation; do not infer unseen figure content.

## 8. Finding evidence format

For each finding, record:
- Finding ID.
- Manuscript location.
- Exact claim/quote.
- Evidence status.
- Evidence source and location.
- Reason the evidence does or does not support the claim.
- Severity and rationale.
- Recommended corrective action.

Do not make a serious accusation (for example, fabrication or misconduct) unless the inspected evidence justifies it. Use neutral wording such as “not supported by supplied evidence”, “contradicted by the inspected record”, or “unable to verify”.
