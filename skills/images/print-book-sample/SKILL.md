---
name: print-book-sample
description: Use when turning a verified book brief into a reviewable print sample, especially a practical guide or educator guide with grayscale interiors. Covers sample scope, local layout and PDF preflight.
version: 1.0.0
---

# Print book sample

Start from the verified editorial brief. Carry the source digest, selected audience and evidence references into the sample receipt. Treat market observations as evidence for the opportunity. Support teaching methods, learner outcomes and other substantive claims with relevant primary education sources before presenting them as established.

## Choose representative pages

For an educator guide, make the cover recognizable to the intended educator. In the sample, show a teacher-facing explanation, a worked classroom example and a reusable activity or planning page. Mark proposed age range, lesson duration and learning objectives as editorial decisions until reviewed. Write examples from scratch. Use fictional or anonymous learners.

Define the page role, title, content blocks, diagrams and continuation rules in structured layout data. Keep exercises and diagrams editable. Set the interior ink mode from the brief. For grayscale, ensure different states stay distinguishable through labels, line styles or patterns. Check workspace for writing or marking on activity pages.

## Make the cover and check the PDF

Use the [cover direction worksheet](../../../references/cover-art-direction/ORDIVANE_WORKFLOW.md) for composition. Route to [Agnes](../agnes-book-cover/SKILL.md) when the brief calls for generated cover artwork and an authorized route is available. Use original local vectors where they explain the concept clearly. Add lettering in layout. Inspect the front at page size and 160 px.

Render every sample page at the actual trim. Review font embedding, clipping, margins, text overflow, contrast and the effective resolution of placed raster assets. Check the exported interior color spaces when grayscale is required. Compare the PDF to the layout data and verify representative exercise or diagram values against their source. Save the render checks, source and output digests and scope of review. Label the sample as ready for review only after the checks pass.

## Automation handoff

Keep art direction and technical preflight as separate checks. Bind the direction to the dossier and the artwork receipt to the exact direction and asset digest. Put a technical cover used to test the renderer in a separate review state. If the artwork is missing, rejected or mismatched, return a waiting state before rendering the editorial sample. Pass that state back to the calling workflow so it can preserve the dossier and resume from the same direction.
