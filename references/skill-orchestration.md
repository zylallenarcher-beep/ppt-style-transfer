# Supporting Skill Orchestration

Read this reference when choosing or combining supporting capabilities. Keep `ppt-style-transfer` responsible for the source, structure, slide-count, editability, and final-delivery contract.

## Select by task and availability

Inspect the current host's skill catalog and actual tool availability. The names below are optional examples, not bundled dependencies or a requirement to install the entire list. Provider prefixes and names may vary. Read the instructions for the selected skills through the host's supported mechanism.

| Current task | Optional supporting skill | Selection boundary |
| --- | --- | --- |
| Read, edit, or rebuild a PPTX; inspect native objects and file structure | `pptx` | Use its supported PPTX workflow and verify the objects actually delivered. |
| Author through a host presentation session or artifact workflow | `presentations` | Follow that skill's current tools and runtime; keep other authoring recipes optional. |
| Produce a PPTX headlessly with a compatible Python route | `pptx-author` | Use for file-based authoring, not editing an open live presentation. |
| Explore layouts or build slide-structured HTML before export | `baoyu-design` | Use when the HTML route is selected. Its export applies to its own structured HTML, not arbitrary existing PPTX files. Validate the exported PPTX and its editability. |
| Produce illustrated slides as raster images | `baoyu-slide-deck` | Use when the user chooses or accepts an image-based deck; its text, tables, and charts are not fully editable native objects. |
| Generate or edit imagery | `imagegen` | Use an available image-generation route within the user's tool, model, and data authorization. |
| Use an explicitly chosen GPT Image API or CLI workflow | `gpt-image` | Verify the requested model, credentials, and authorized cost scope; preserve the user's provider choice. |
| Write or diagnose prompts for an explicitly chosen Image 2.5 model | `image25-prompting` | Prompt work alone does not start generation. |
| Derive a reproducible image prompt from a visual reference | `get-prompt-from-image` | Use for the image's appearance; it does not replace whole-deck style analysis or authorize generation. |
| Read or render a PDF source, reference, or review export | `pdf` | Inspect rendered pages; extracted text alone does not validate the layout. |
| Read or verify Excel/CSV source tables or chart data | `spreadsheets` | Use when spreadsheet files are involved; retain worksheet/cell provenance and the approved business values. |
| Perform a requested investment-banking or client-readiness deck review | `ib-check-deck` | Review and report. Apply any corrections through the production workflow within the authorized scope. |

If a named skill is missing, use a compatible available tool or equivalent skill. Identify the real capability gap when none exists, and continue independent authorized work. A list of skill names is not evidence that they were invoked or that the required service works.

## Compose compatible stages

- Choose one compatible primary presentation-authoring route. For example, use `pptx`, the host's `presentations` workflow, or `pptx-author` as appropriate. Their toolchains can differ; do not impose incompatible runtimes or recipes as simultaneous requirements.
- Add design, imagery, source-data, or review helpers only for the stages that need them. A possible chain is source inspection, HTML design with `baoyu-design` when selected, imagery with `imagegen` when needed, compatible PPTX production, then final-file and rendered-page checks.
- Carry source locators, exact text and values, units, approved assets, style rules, target slides, and editing requirements across handoffs. A helper's default advice to shorten text, change slide count, or wait for a new sample approval does not override the established task contract.
- Preserve exact tool/model requests. If the requested route is unavailable, explain the gap instead of silently switching providers, models, or delivery formats. Use only controls actually exposed by the selected tool; a model, size, or quality named in a prompt does not prove that the tool provides that control. Keep prompt-only work separate from generation and native objects separate from raster content.

## Authorization and project data

Reuse the user's existing authorization. Selecting a supporting skill does not itself authorize new installations, credentials, paid API calls, external uploads, publishing, or broader business-fact revisions. Obtain only genuinely missing authorization for an action that requires it; continue work already covered by the task.

Send sensitive source text, images, or embedded data only to approved services within the authorized data scope. Keep task-specific mappings, notes, prompts, assets, and renders in approved private project locations, and exclude them from public Skill packages and their Git history. Public distribution of workflow instructions does not authorize publication of a user's source presentation.

## Verify the composed result

Record the selected helpers, their actual availability and use, the outputs handed off, and any limitations in the private task record. Validate the final files for source coverage, numbers in context, permitted slide-count changes, actual editability, and real rendering. A successful helper call or intermediate preview does not establish that the finished deck passes these checks.
