---
name: architecture
description: Create or update an ARCHITECTURE.md file for a software repository using a consistent architecture template and system diagram. Use when users ask for architecture documentation, architecture overview, system design summary, high-level component mapping, system context outline, data flow boundaries, infrastructure/deployment overview, or an ARCHITECTURE.md starter document.
---

# Architecture Skill

Create or refresh a root-level `ARCHITECTURE.md` that gives agents and developers a fast, accurate architectural understanding of the codebase.

## Workflow

1. Inspect the repository structure before drafting content.
2. Read `references/ARCHITECTURE_TEMPLATE.md` and use it as the baseline structure.
3. Create or update `ARCHITECTURE.md` at repository root.
4. Preserve all section headings from the template unless the user requests a different structure.
5. Populate placeholders with repository-specific details; keep unknown fields as explicit placeholders rather than inventing values.
6. Ensure section **2. High-Level System Diagram** includes a clear architecture diagram (Mermaid is acceptable, ASCII is also acceptable if requested).
7. Set **Date of Last Update** to the current date in `YYYY-MM-DD` format.

## Output Rules

- Keep architecture information concrete and repository-specific.
- Prefer concise statements over long prose.
- Reflect real technologies found in the repo (frameworks, services, stores, CI/CD, security controls).
- If information is missing, write `Unknown` or a bracketed placeholder.
- Do not remove the diagram requirement from section 2.

## Required Template

Always base the output on:

- `references/ARCHITECTURE_TEMPLATE.md`

Copy that structure into root `ARCHITECTURE.md`, then tailor content to the repository.