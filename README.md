# PPT Style Transfer

Redesign an existing presentation to match a reference deck, slide screenshots, or an approved visual style while preserving the content and numbers required for the task. Use it for visual refreshes, slide layout changes, representative samples, complete deck redesigns, or revisions to an existing deliverable.

Public repository: [ppt-style-transfer](https://github.com/zylallenarcher-beep/ppt-style-transfer).

## Capabilities

- Extract the reference's colors, typography hierarchy, image style, brand elements, and spacing.
- Rearrange text, images, tables, and charts, reducing slide density within the authorized scope.
- Map source content to output slides and verify numbers, units, qualifiers, and relationships.
- Check content in the final files and inspect actual renders for missing text, clipping, overlap, and line wrapping.
- Deliver the requested PPTX, PDF, or previews, with a clear account of editability and known limitations.
- Coordinate available presentation, design, image, spreadsheet, and review skills as the task requires.

Writing a presentation from scratch, updating numbers alone, and auditing business facts are outside the default scope.

## Structure and slide count

| Mode | Approach |
| --- | --- |
| Preserve structure and slide count | Keep the sections, slide order, content assigned to each slide, and total slide count. Improve layouts within each slide. |
| Restructure and add slides with authorization | Rearrange or split slides after explicit authorization, choose a slide count within the approved bounds, and provide a source-to-output slide map. |
| Propose a slide count for approval | Submit the proposed total, net increase, split rationale, and content destinations before producing slides that depend on the increase. |

"The slides are too crowded" alone does not authorize adding slides. Sample approval and approval of the full deck's slide count are recorded separately. Existing authorization carries forward without repeated confirmation.

## Installation

Place the complete repository root at `~/.codex/skills/ppt-style-transfer`, with `SKILL.md` directly inside that folder. Keep `agents/` and `references/` together with it. If you use a custom `CODEX_HOME`, install under its `skills/ppt-style-transfer` directory.

Alternatively, clone the repository:

```sh
git clone https://github.com/zylallenarcher-beep/ppt-style-transfer.git ~/.codex/skills/ppt-style-transfer
```

If the destination already exists, save the existing version separately before replacing it.

## Environment and dependencies

This repository contains workflow instructions. It does not bundle presentation software, exporters, renderers, or image generation services. The host environment must provide the ability to read, author, and inspect presentation files; tools are selected for the task.

Supporting skills are selected from the host's current capabilities. Examples include `pptx`, `presentations`, or `pptx-author` for a compatible authoring route; `baoyu-design` for HTML design; `imagegen` or an explicitly chosen `gpt-image` route for imagery; and `pdf`, `spreadsheets`, or requested specialist review for the relevant checks. These Skills are not bundled with this repository. See [Supporting Skill Orchestration](references/skill-orchestration.md) for the task map, prompting helpers, image-based deck option, and handoff rules.

Only the needed skills are loaded. Existing content, slide-count, editability, tool/model, and authorization requirements carry through each stage. Optional integrations do not automatically install tools, start paid generation, or upload private source material. HTML authoring and image generation are used only when needed; Windows PowerPoint COM requires a compatible environment.

Editability depends on the production route. Data-driven charts and tables with editable rows require suitable native objects. Elements inside composited backgrounds or full-slide images cannot be described as fully editable. If actual rendering is unavailable, identify the unverified parts and leave rendering validation marked as incomplete.

## Usage examples

Provide the source presentation and visual references, then specify the scope you need.

### Preserve every slide

```text
Use $ppt-style-transfer to redesign the source deck in the reference style.
Preserve the wording, numbers, structure, slide order, and total slide count.
Keep text, tables, and charts editable. Deliver PPTX and PDF files.
```

### Allow restructuring and additional slides

```text
Use $ppt-style-transfer to redesign the complete deck in the reference style.
You may rearrange and split slides, and choose the slide count.
Preserve all business content, provide a source-to-output slide map,
and inspect the final renders.
```

### Approve the slide count first

```text
Use $ppt-style-transfer to analyze crowded slides and propose a new total,
the net increase, which slides to split and why, and where their content will go.
Report the proposed count first. Wait for approval before producing slides
that depend on the increase.
```

Read the full workflow in [SKILL.md](SKILL.md), [Content Mapping and Fidelity Checks](references/content-fidelity.md), and [Export and Rendering Validation](references/export-validation.md).

### Combine available skills

```text
Use $ppt-style-transfer to redesign this deck in the reference style.
Choose compatible available skills for source inspection, layout, imagery,
data checks, and final validation. Preserve the content, slide-count,
editability, and tool requirements already agreed for this task.
```

## License

No license has been specified for this package. Public availability does not grant a particular open-source license.
