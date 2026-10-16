# ppt-style-transfer

## Package source and status

- Type: A complete package of a user-installed Skill, including `SKILL.md`, `agents/openai.yaml`, and three documents under `references/`.
- Source: The user supplied the `ppt-style-transfer` package and authorized its inclusion and public distribution at [ppt-style-transfer](https://github.com/zylallenarcher-beep/ppt-style-transfer).
- Language: The public edition is in English. It preserves the original workflow's scope, authorization rules, and validation requirements.
- This package documents the workflow. Its presence in a catalog does not establish actual invocation, presentation production, successful testing, or production use.
- No third-party code, fonts, images, or other assets are bundled. No license has been specified.

## Scope and trigger

Use this Skill to redesign, rearrange, sample, and validate an existing presentation against a reference deck, slide screenshots, or an approved visual style. It supports three modes: preserve structure and slide count, restructure and add slides with explicit authorization, or propose a slide count for approval first.

The current request determines content fidelity, editability, output formats, and permission to change structure. Updating numbers alone, writing from scratch, and auditing business facts are outside the default scope.

## Capabilities and limits

Extract visual rules, map source content to output locations, verify numbers in context, check the final file's content, and inspect actual renders for missing text, clipping, overlap, and line wrapping. Elements within full-slide images or composited backgrounds cannot be described as fully editable. Report any parts that could not be verified through actual rendering.

## Dependencies and installation

The host environment supplies presentation reading, authoring, export, and rendering capabilities. This package includes no runtime or service. It coordinates optional available skills for authoring, HTML design, imagery and prompting, spreadsheet source data, PDF review, and requested deck QC. Choose compatible tools for each stage using [Supporting Skill Orchestration](references/skill-orchestration.md); the named skills are not bundled or assumed to be installed. HTML authoring, image generation, and Windows PowerPoint COM are used only when needed and available. The existing source, editing, authorization, and project-data boundaries remain authoritative across handoffs.

Install the complete directory at `~/.codex/skills/ppt-style-transfer`, or under `skills/ppt-style-transfer` in a custom `CODEX_HOME`. See [README.md](README.md) for usage and [SKILL.md](SKILL.md) for the execution rules.
