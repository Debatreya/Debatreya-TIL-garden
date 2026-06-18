# Contributing to This TIL Repo

This repository is a personal TIL journal built with Quarto. The goal is to keep each note small, focused, and easy to render into a readable article while preserving a clean source structure.

## What To Add

Add one `.qmd` file per TIL. A good TIL is:

- Narrow in scope.
- Written as a concrete lesson, not a full tutorial.
- Backed by an actual problem, project, or experiment.
- Easy to revisit later through the index table in `README.md`.

## Where Files Should Go

Place new notes under `records/` in the category folder that best matches the topic:

- `records/architecture/`
- `records/development/`
- `records/ai/`
- `records/general/`

If a new category is genuinely needed, create a new folder under `records/` and keep the name short and descriptive.

Use one file per note and keep the source filename meaningful. The current repo mixes PascalCase and kebab-case, so consistency with the local folder is more important than enforcing a single global style.

## Front Matter Convention

Every note should begin with YAML front matter. The repo currently uses these fields:

- `title`
- `date`
- `category`
- `tags`
- `read_time`
- `id`
- `related_tils`
- `related_projects`
- `system_manifest`
- `contributor_avatars`
- `external_links`

A minimal example:

```yaml
---
title: "My New TIL"
date: 2026-06-18
category: "Development"
tags: ["#example", "#notes"]
read_time: "4 min"
id: "TIL-009"
related_tils: []
related_projects: []
system_manifest: "debatreyadas.dev-v1"
contributor_avatars:
  - name: "Debatreya Das"
    avatar: "/avatars/debatreya.jpg"
---
```

## How To Write QMD Files

Use standard Markdown inside `.qmd` files. The repo already supports Quarto rendering with HTML output, KaTeX math, code copy buttons, and line numbers.

Recommended structure:

- `##` for the main sections.
- `###` for subsections.
- `####` for deeper technical breakdowns or step lists.
- Paragraph text for the explanation.
- Bullet lists for compact takeaways.
- Tables for comparisons or summary matrices.
- Code fences for commands, config, snippets, or pseudo-code.
- Math blocks when you need formulas.

Keep the note readable first and technical second. A strong TIL usually has:

- Context.
- The problem or insight.
- The solution or learning.
- A short takeaway or conclusion.

## Headers Available In Practice

The repo does not enforce a custom header system beyond Markdown and Quarto front matter. In practice, the content hierarchy used here is:

- YAML front matter at the top of the file.
- `#` only when a document needs an explicit top title in the body.
- `##` for primary sections.
- `###` for subsections.
- `####` for nested implementation details.

That pattern matches the existing notes and keeps the rendered output consistent.

## Assets Folder

Use `assets/` for media that belongs to the notes:

- `assets/diagrams/` for architecture drawings, Excalidraw exports, and conceptual diagrams.
- `assets/screenshots/` for screenshots and captures used in the notes.

Reference images with root-relative paths such as `/assets/diagrams/example.png` or `/assets/screenshots/example.png`.

Keep generated or exported visuals here if they are part of the source material for a TIL. Do not put rendered site output here.

## Avatars Folder

Use `avatars/` for contributor profile images referenced from front matter. The `contributor_avatars` field expects a name and an image path, such as:

```yaml
contributor_avatars:
  - name: "Debatreya Das"
    avatar: "/avatars/debatreya.jpg"
```

Keep avatar images small, reusable, and easy to identify.

## Generated Output

Quarto writes rendered site files to `_output/`.

- Do not edit `_output/` by hand.
- Treat it as build output.
- Make changes in the source `.qmd` files instead.

## Updating The Index

When you add a new TIL, update the table in `README.md` with:

- The new `TIL-xxx` identifier.
- The title.
- The category.
- A relative link to the `.qmd` file.

Keep the IDs sequential so the index stays easy to scan.

## Suggested Review Checklist

Before publishing a note, check that:

- The front matter is valid YAML.
- The `id` is unique.
- The note lives in the correct `records/` subfolder.
- Images point to existing files in `assets/` or `avatars/`.
- The `README.md` index is updated.
- The body uses consistent heading levels.
