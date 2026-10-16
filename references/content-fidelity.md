# Content Mapping and Fidelity Checks

Use this reference when preserving content from an existing PPT, especially when reorganizing content across slides or working with reports that contain tables or charts.

## Source records

Save the original file hash, slide order, dimensions, and rendered source slides. Extract native paragraphs, table cells, data labels, units, qualifiers, footnotes, source authority levels, and notes. Also inspect text within images, content inherited from slide masters, grouped shapes, embedded charts, and their workbooks. A bar chart drawn with ordinary shapes still carries relationships between data and categories.

Assign each content item a stable locator, such as source file / slide / object / paragraph. Locate table content by row and column, and chart content by series / category / value. Image identifiers locate assets; they do not replace checks of their business meaning. Use OCR as an aid. Mark illegible text as pending verification instead of guessing numbers or filling gaps.

Store the mapping in JSON, CSV, or a table; no particular project directory structure is required. Include at least these fields:

| Field | Purpose |
|---|---|
| source_id / locator | Locate the source slide, object, paragraph, or cell |
| original_text / value | Preserve the exact source text or value with its unit |
| output_page / target | Record the output location and content destination |
| role | Identify business source text, repeated running headings or table headers, navigation, or illustrative annotations |
| change_reason / authorization | Record the basis for an authorized rewrite, correction, or reference update |

## Splitting and reorganizing slides

Check authorization against the structure and slide-count mode in SKILL.md. When structure and slide count must match exactly, map each source slide to a new slide in the same sequence, and verify content placement and section hierarchy slide by slide. When reorganization is allowed or an expansion plan has been approved, one source slide may map to multiple new slides. Keep conditions and conclusions within a content group connected. Repeat relevant running headings, table headers, units, or qualifying conditions as needed to avoid ambiguity after a split, and record why they were repeated. Moving body content into speaker notes does not satisfy a requirement to keep it fully readable.

Handle cross-references such as "see P4" when reorganizing content. If navigation updates are allowed, record the old reference and its new target. If all original wording must remain strictly unchanged, retain the original reference and add a source-slide note or mapping table. Clearly distinguish new slide numbers from source-deck locators.

Record the specific source and discrepancy when arithmetic, terminology, or wording is inconsistent. A visual redesign does not by itself authorize factual changes. When the user explicitly authorizes business-content revisions, record those changes separately and check against the corresponding baseline version.

## Final-file checks

1. Coverage: Every source item that must be preserved has an output destination. List uninspected image, OCR, or embedded content separately.
2. Text: Read paragraphs and table text back from the final PPTX and compare them with the expected content mapped to each slide. Layout-induced line breaks and whitespace differences may be ignored. Numbers, plus and minus signs, inequality signs, decimal points, units, and qualifiers must match.
3. Occurrences: Explicitly record permitted repetitions and new navigation. Comparing character multisets for each slide can help detect omissions, but cannot establish order or meaning on its own.
4. Relationships: Verify the metric, table row and column, or chart series and category associated with every value. Check process direction, legends, scales, and footnotes. Complete text alone does not establish correct relationships.
5. Visuals: Native text that is complete but obscured or cropped still fails. Check the final rendered slides.

When the first slide must be preserved "exactly as is," prefer keeping the native slide and comparing renders in the same application at the same dimensions. Explain differences across renderers; pixel identity is not a universal cross-platform acceptance criterion.

Fidelity checks establish that content follows the specified source. They do not establish that the source data is true or that its investment conclusions are correct.
