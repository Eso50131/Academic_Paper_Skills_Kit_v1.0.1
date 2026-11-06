# Package Manifest

- Package: Academic Paper Writing & Audit Skills
- Version: 1.0.1
- Created: 2026-11-06
- Standard: Open Agent Skills folder convention
- Skills:
  - `academic-paper-writing`
  - `academic-paper-audit`
- Primary output: Markdown manuscript and Markdown handoff/audit documents
- External dependencies: None
- MCP dependencies: None
- Scripts: None
- Templates: Included under each skill's `assets/`
- Optional UI metadata: Included under each skill's `agents/openai.yaml`

## Validation performed

- Each skill folder contains exactly one `SKILL.md`.
- Each `SKILL.md` starts with YAML frontmatter containing `name` and `description`.
- Folder name matches the skill `name`.
- All relative references from `SKILL.md` point to files in the skill package.
- Each individual skill archive contains one top-level skill folder.
- The combined archive contains both independent skill folders and the QA test cases.
- Version 1.0.1 adds evidence-based claim-strength protection to writing and a dedicated defensive-writing check to independent audit, without changing the established workflow.
