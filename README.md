# Academic Paper Writing & Audit Skills

**Version:** 1.0.1  
**Language:** Chinese-first instructions; supports Chinese and English academic manuscripts  
**Package type:** Open Agent Skills-compatible folders

This package contains two independent skills:

1. **`academic-paper-writing`** — research understanding, pre-writing, evidence-aware planning, academic manuscript drafting and revision.
2. **`academic-paper-audit`** — independent, evidence-based manuscript acceptance review. It is intentionally separate from the writing skill.

The handoff artifacts are:

- `Prewriting_Dossier.md` — the approved research understanding, user-confirmed facts, outline, and claim/evidence plan.
- `Manuscript.md` — the manuscript itself, delivered in Markdown.
- `Independent_Audit_Report.md` — the independent audit findings and verdict.

## Important format decision

The manuscript deliverable is **Markdown (`.md`)**, not DOCX. This avoids unnecessary Word layout work and makes the text directly inspectable by models.

Markdown delivery must **not omit research visuals or structured content**:

- Preserve all tables, equations, figure numbers, captions, notes, units, axes, legends, and source attributions.
- Preserve supplied image assets and reference them with relative Markdown image paths, for example `![Figure 2. Workflow](figures/figure-2.png)`.
- If an image cannot be embedded or extracted, retain an explicit placeholder with the figure number, intended content, and missing asset requirement. Never silently drop it.
- Do not replace a data-bearing figure with vague prose. If the original data are available, preserve the figure or provide the underlying table/data as appropriate.

## Package contents

```text
Academic_Paper_Skills_Kit/
├── README.md
├── QA_Test_Cases.md
└── skills/
    ├── academic-paper-writing/
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   ├── references/
    │   └── assets/
    └── academic-paper-audit/
        ├── SKILL.md
        ├── agents/openai.yaml
        ├── references/
        └── assets/
```

## Compatibility and installation

The skills use the open Agent Skills folder convention: each skill is a directory containing exactly one `SKILL.md` entrypoint with YAML frontmatter (`name`, `description`), plus optional `references/`, `assets/`, and `agents/openai.yaml`.

- **Codex CLI / IDE:** copy each skill folder into a discovered skills directory, such as `$HOME/.agents/skills/` for user-wide use or `<repo>/.agents/skills/` for repository-specific use. Keep the folder name identical to the skill name.
- **ChatGPT desktop:** standalone skills are supported in eligible/current desktop experiences; use the Skills area and follow the import/install flow exposed by your version.
- **ChatGPT web/mobile:** current OpenAI documentation distinguishes standalone skills from skills distributed through plugins. Standalone skills are not universally available on every ChatGPT surface. For web/mobile distribution, package the skills through the supported plugin workflow if your workspace/product offers it.
- **OpenAI Skills API:** upload the two individual ZIPs supplied with this package separately. Each individual ZIP contains one top-level skill folder and exactly one `SKILL.md`. Do not upload the all-in-one archive as a single skill bundle.

The `agents/openai.yaml` files provide optional OpenAI UI metadata. They do not add external tool dependencies.

## Included archives

The delivery set contains:

- `Academic_Paper_Skills_Kit_v1.0.1.zip` — the complete source package with both skills, templates, references, and QA tests.
- `academic-paper-writing_v1.0.1.zip` — upload-ready single-skill archive.
- `academic-paper-audit_v1.0.1.zip` — upload-ready single-skill archive.

## Recommended use

1. Start a **new writing conversation** and invoke `academic-paper-writing`.
2. Provide available research materials. Let the skill inspect them before asking questions.
3. Complete the research-discovery and targeted-clarification steps. Confirm the proposed outline.
4. Ask the writing skill to produce both the Markdown manuscript and the completed Pre-writing Dossier.
5. Start a **separate conversation** and explicitly invoke `academic-paper-audit`.
6. Supply the frozen manuscript version, Pre-writing Dossier, original research materials, evidence matrix, and source materials.
7. Review the independent audit report. Revise through the writing workflow, then re-audit the new manuscript version.

The audit skill is deliberately configured for explicit invocation. This reduces accidental mixing of authoring and judging roles.

## Claim-strength protection and anti-defensive writing

Version 1.0.1 adds a focused safeguard to both skills. The writing skill records approved, evidence-supported core claims and their scope, avoids unsupported weakening or hypothetical reviewer disclaimers, and requires evidence for material claim changes. The audit skill checks claim-strength changes and defensive wording against the approved baseline when available. Appropriate uncertainty and genuine limitations remain required; the goal is neither overstatement nor unnecessary retreat.

## No MCP required

These are instruction-and-reference skills. They do not require a custom MCP server, API, or script. They instruct the agent to use web search, file reading, or other tools only when those capabilities are available in the current environment. If a required capability is unavailable, the agent must disclose the limitation rather than pretend that verification occurred.

## Scope

These skills are for **scholarly academic papers**. They do not define workflows for project reports, business reports, grant applications, theses/dissertations as a separate genre, or general business writing. A thesis chapter may be handled only when the user explicitly asks to apply the academic-paper rules to that chapter.

## Design references

The package follows the current OpenAI/ChatGPT and Codex skill-folder conventions and the open Agent Skills approach. See the official documentation:

- [Build skills — ChatGPT Learn](https://learn.chatgpt.com/docs/build-skills)
- [Skills — OpenAI API](https://developers.openai.com/api/docs/guides/tools-skills)
- [OpenAI skill-creator guidance](https://github.com/openai/skills/blob/main/skills/.system/skill-creator/SKILL.md)

The academic-writing references also point to established resources such as the University of Manchester Academic Phrasebank, Gopen & Swan's *The Science of Scientific Writing*, PRISMA 2020, Cochrane guidance, and journal/publisher instructions. Always verify the latest edition and target-journal policy when a task depends on them.
