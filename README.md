# TIL Repository

This repository is my public knowledge base for short, self-contained TILs: practical things I learned while studying, building, deploying, and documenting software. Each note is written as a Quarto file (`.qmd`) so it can be rendered as a readable article while still keeping the source easy to edit and organize.

The repo is structured around topic folders under `records/`, with supporting media in `assets/` and contributor photos in `avatars/`. The rendered site output is written to `_output/` by Quarto and should be treated as generated content.

## TIL Index

| TIL ID | Title | Category | Relative Link |
| --- | --- | --- | --- |
| TIL-001 | Building an Automated, Manifest-Driven Portfolio Sync Engine | Architecture | [records/architecture/dev-os-manifest-engine.qmd](records/architecture/dev-os-manifest-engine.qmd) |
| TIL-002 | From $0 to Zero-Trust: Architecting a Secure, Serverless Competition on a College Budget | Architecture | [records/architecture/Zero-Trust-Secure-Serverless-Competition.qmd](records/architecture/Zero-Trust-Secure-Serverless-Competition.qmd) |
| TIL-003 | From PaaS to Bare Metal – My First Production Deployment | Deployment | [records/development/My-First-Production-Deployment.qmd](records/development/My-First-Production-Deployment.qmd) |
| TIL-004 | Software Engineering study in AI Era | General | [records/general/engineering-in-AI-era.qmd](records/general/engineering-in-AI-era.qmd) |
| TIL-005 | From PaaS to Bare Metal – Part 2: The "Day 2" Challenge: Updates and Blue-Green DB Sync | Deployment | [records/development/Production-Deployment-Part-2-The-Updation.qmd](records/development/Production-Deployment-Part-2-The-Updation.qmd) |
| TIL-006 | Mastering the Model Context Protocol (MCP) | AI | [records/ai/model-context-protocol.qmd](records/ai/model-context-protocol.qmd) |
| TIL-007 | From E-Waste to Private Cloud: The Triple-Threat Home Server Journey | Architecture | [records/architecture/personal-cloud-service.qmd](records/architecture/personal-cloud-service.qmd) |
| TIL-008 | System Design Patterns — Quick Patterns Reference | Architecture | [records/architecture/system_design_patterns.qmd](records/architecture/system_design_patterns.qmd) |

## How The Repo Works

Every TIL starts as a `.qmd` file under `records/`. The folder name indicates the broad category, while the file name identifies the note itself. The note begins with YAML front matter, which Quarto uses to render metadata and which this repo uses to store the TIL index fields.

The common front matter fields used across the repo are:

- `title`: Display title of the note.
- `date`: The publishing or learning date.
- `category`: The high-level bucket for the note.
- `tags`: Searchable topical tags.
- `read_time`: Estimated reading time.
- `id`: Stable TIL identifier such as `TIL-001`.
- `related_tils`: Linked TIL IDs for cross-references.
- `related_projects`: Any associated project names.
- `system_manifest`: Manifest or system name used by the site.
- `contributor_avatars`: Contributor names and avatar image paths.
- `external_links`: Supporting references, certificates, videos, or repo links.

In the body of a note, the repo typically uses:

- `##` for the main sections of the note.
- `###` for subsections.
- `####` for step-by-step details or deeper nesting.
- Standard Markdown lists, tables, quotes, code fences, and image links.

Images are generally linked with root-relative paths such as `/assets/diagrams/...` or `/assets/screenshots/...`, and contributor pictures are linked from `/avatars/...`.

