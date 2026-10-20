---
description: Create a reusable project brain starter in the current project
---

# Create a project brain starter

Create a barebone `project-brain/` folder in the current project. It must be reusable for any kind of project and must contain no product-specific names, requirements, sample credentials, or assumed technology stack. Inspect the existing files first and preserve any existing user content. If `project-brain/` already exists, add only missing starter files and report any conflicts instead of overwriting them.

Build this structure:

```text
project-brain/
  .gitignore
  README.md
  private-knowledgebase/
    README.md
  internal-knowledgebase/
    README.md
    decisions.md
    transcripts/
      README.md
  project-knowledgebase/
    README.md
    specs/
      README.md
    scenarios/
      README.md
    adrs/
      README.md
    transcripts/
      README.md
```

Write concise, practical Markdown instructions in each README:

- `private-knowledgebase/` is for personal notes and drafts. Shared specs must never cite it.
- `internal-knowledgebase/` is team-visible raw input and dated decisions. Use one input per file under `transcripts/`, named `YYYY-MM-DD-<source>-<topic>.md`. Keep later corrections as new entries.
- `project-knowledgebase/` is material stakeholders may review. Its `specs/` hold current agreed behavior by area; `scenarios/` hold observable acceptance checks matched by filename to specs; `adrs/` explain significant technical decisions; `transcripts/` hold stakeholder input.
- Explain the flow from raw input or decision to a sourced spec rule, then a scenario when applicable. Keep unanswered questions explicit. Never fabricate a project fact.
- In `specs/README.md`, include an initially empty index and a simple format: Context, Glossary, Use Cases, Domain Rules, Open Questions. Rule IDs use `R-<AREA>-001`, remain stable, have status `[planned]`, `[partial]`, or `[built]`, and cite a shared source relative to the `project-brain/` root. An optional `[from code - unconfirmed]` status is for existing behavior awaiting confirmation.
- In `scenarios/README.md`, show a generic scenario with `SC-<AREA>-001`, `Covers`, use case, status, priority, setup, steps, and observable expected results. Explain that built rules need scenario coverage or a documented reason for exemption.
- In `adrs/README.md`, show the `NNNN-short-title.md` naming convention and a small template with status, date, context, decision, and consequences.
- In `decisions.md`, include only a title and guidance for dated entries; include no invented decisions.
- In `project-brain/.gitignore`, ignore `/private-knowledgebase/*` and re-include `/private-knowledgebase/README.md`. Explain that Git ignore does not untrack previously committed files or prevent cloud sync.

Do not create example specs, scenarios, ADRs, or transcripts that could be mistaken for real project facts. At the end, show the created tree and state whether any existing files were left untouched or any conflicts need review.
