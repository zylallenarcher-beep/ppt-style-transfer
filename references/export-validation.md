# Export and Rendering Validation

Read the sections relevant to the selected production route. HTML, PowerPoint COM, and composited backgrounds are not mandatory for every task.

## Match the required editing capabilities first

- Native objects: Suitable for layout changes, adding or removing table rows, and updating charts linked to data. Verify the actual object types and editing behavior.
- Hybrid: Render photographs, complex gradients, glass effects, and decoration into a background, while retaining body text and numbers as native text. Suitable for presentations that need stable visuals and mainly text edits. Bars and timelines within the background do not update automatically when numbers change.
- Full-slide images: Use only when the user accepts this delivery format. Describe the text as non-editable.

## HTML to PPTX

Use fixed dimensions and explicit slide boundaries. Preview over HTTP. Multi-slide components may generate thumbnails or clones; capture only the actual slides. For deck-stage, selecting direct child slides can avoid counting internal clones. Check the slide count, slide uniqueness, asset loading, and font readiness.

If the exporter cannot reliably reproduce glass effects, filters, or gradients, you may composite the visual layer, provided this meets the editing requirements. Hide text and any native brand objects that must be retained before capturing the visual layer. After overlaying native text, check for duplication, omissions, and backgrounds covering content. Preserve the geometry of hidden layout placeholders so text does not reflow when background elements disappear.

Validate a representative slide in the actual PPTX before expanding to the full deck. Find the runtimes and exporters available in the current environment. Avoid hard-coded tool paths from another project, and do not install a new tool merely because a previous project used it.

## Windows PowerPoint

Test inserting slides across different dimensions in a copy first, then check the target dimensions and object scaling. If the original first slide must be retained, you may keep it in a copy of the source deck and import the redesigned inner slides. Preserve the original file and leave the user's other presentations open.

Browsers and PowerPoint may calculate Chinese fonts, punctuation, and text boxes differently. If Chinese punctuation appears at the beginning of a line, a full stop is stranded, or line wrapping is incorrect, check the East Asian font and language settings first. In a PowerPoint COM environment that supports them, LanguageID=2052 and FarEastLineBreakControl are repair options that must be verified. Apply them only to the relevant Chinese text, without globally overriding other languages. Re-render affected slides after local text-box expansion or spacing adjustments.

The actual text bounds of TextRange can help detect overflow and intersections. Also visually inspect tables, hierarchy, image subjects, and masks. Programmatic bounds checks do not replace visual judgment, and decorative overlaps are not necessarily errors.

## Pre-delivery checks

- Read content back from the final PPTX, rather than comparing only generation code or HTML.
- Render the final version with the target presentation software. If using an alternative renderer, state the limits of what it verifies.
- Check slide count and order, missing or cropped text, image clarity, font weight, Chinese line breaking, table rows and columns, and chart relationships.
- Run file-structure validation appropriate to the production route. Confirm that opening and exporting produce no repair warnings.
- After fixing a specific issue, recheck the affected scope. Deliver once all checks pass; avoid repeated runs that add no verification value.
- Save the final renders, source mapping, and known limitations. A local HTTP preview is not long-term hosting.
