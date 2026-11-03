---
name: agnes-book-cover
description: Design self-publishing cover studies from a book brief and observed comparables, using an existing Agnes image connection in n8n and separate editable typography. Use when the user selects Agnes for cover artwork; supports fiction, nonfiction, workbooks and logbooks.
---

# Book Cover Design with Agnes

Adapted from Arcanea Book Cover in frankxai/creator-skills, source commit b87c6bdbfb3252dfec4a271309af31ae92226a04. The original remains in its own folder. Retain the repository MIT license and copyright notice when copying this derivative.

Agnes is an external API and may charge. Use this variant only with a currently verified zero-price model/account route and the user's authorized call allowance. Having a key or a credential named free does not establish eligibility. Do not subscribe, top up, use paid fallback models or generate again merely because a cover is imperfect.

This file supplies design and provider-routing instructions. It does not install a workflow, retrieve a key or connect an editorial controller by itself.

## 1. Understand the book and its buyer

Read the available dossier, outline or manuscript and distinguish verified book facts from proposed copy. Identify audience, purpose, emotional register and the central visual idea.

For fiction, examine tension, narrative stakes and an appropriate symbolic image. For nonfiction, workbooks, technical manuals and logbooks, examine reader use, promised outcome and subject; do not invent protagonists or narrative conflicts. A sample puzzle book is a study, not the universal target.

Use relevant competitor covers actually observed, preferably from the existing research dossier. Record what each example shows about category recognition, hierarchy, imagery and thumbnail readability. If none were observed, label the art direction a hypothesis. Do not claim to have inspected a competitor or know what sells without evidence. Avoid copying their artwork, distinctive compositions or branding.

## 2. Choose an art direction

State one visual idea, its connection to the book, the role of the illustration, the type hierarchy and a coherent palette. Treat designer-inspired principles as working heuristics, not verified quotations or guaranteed sales rules.

Choose illustration, photography, original vectors, patterns or diagrams according to the brief. Exact puzzle grids, counts, technical symbols and readable text belong in deterministic local layout. Do not ask an image model to establish their correctness.

If alternatives are requested, vary the underlying concept and composition, not only the background color. A brighter palette is a book-specific choice, not a requirement for every genre. Keep the genre signal explicit: an attractive abstract image may still fail to identify the category.

## 3. Write the image prompt and layout brief

Describe subject, composition, lighting, palette, material treatment, emotional register and exclusions. Describe visual properties instead of asking for imitation of an individual artist. Default to artwork without baked-in title text; add title, subtitle and publisher separately as editable layout content.

Derive cover geometry from the actual trim and intended output. Artwork aspect ratio and final cover aspect ratio may differ when the illustration occupies a panel. Neither 2:3 nor 4K is a universal print specification. Do not invent spine width, manuscript page count or promises such as a puzzle quantity.

Prepare a bounded request with explicit model, output count, dimensions/ratio and an immutable prompt. No competitor reference uploads or confidential manuscript transmission are implied by this skill. Free-tier data handling must be suitable for the actual input.

## 4. Route through the existing n8n credential

Use the reviewed existing Agnes credential reference in n8n; never read its secret from an n8n database, reveal it in chat, publish it, paste it into workflow code or put it in a URL. Preserve successful workflows and historical receipts. A test workflow must remain manual and unpublished.

The qualified request shape for an artwork study is:

```json
{
  "model": "agnes-image-2.5-flash",
  "prompt": "The original art-directed prompt prepared for this study",
  "size": "4K",
  "ratio": "3:2",
  "n": 1,
  "return_base64": true
}
```

Send JSON with the configured Header Auth credential to `POST https://apihub.agnes-ai.com/v1/images/generations`. This is not the Gemini generateContent endpoint or request schema. Check current supported parameters before selecting another size or ratio.

Verify current pricing and account eligibility at [Agnes pricing](https://agnes-ai.com/en/docs/pricing). Trial offers apply to eligible default accounts; plan pools can differ. The account billing record determines actual charges. Never convert the example into a permanent free-price guarantee.

Before dispatch, compare the prepared request and installed workflow, enforce the authorized call count and record the request hash and a consumed dispatch claim in the existing project bookkeeping. Reuse a completed matching result after verifying its receipt and asset hash. A timeout, transport error or started-but-uncertain call requires reconciliation, not an automatic retry. Do not release uncertain reservations or create a new job to bypass a cap. Disable HTTP-node retries and pagination.

For HTTP 200 require exactly one `data` image with `b64_json`; decode it with explicit byte limits and inspect its real file format and dimensions. Do not fetch arbitrary provider-returned URLs with the credential. Save the received original unchanged in the project's review area, its SHA-256, request provenance and execution ID. Keep billing observation separate from generation success.

## 5. Review the actual result

Inspect the received image and the final local layout, including a thumbnail. Check relevance to the brief and category, composition, readable title, focal point, palette, unwanted objects, malformed shapes and any image artifacts. Report missed prompt requirements rather than silently treating them as passed.

Render and visually inspect the PDF when producing a PDF study. Measure effective pixels per printed inch at the artwork's actual placement, verify page geometry and embedded fonts, and keep rights/source notes. Changing DPI metadata or interpolating pixels does not establish new image detail. Received pixel dimensions alone do not prove how the provider created them.

A successful connection does not establish professional design quality, a complete print wrap, complete interiors, commercial clearance or automation through the main controller. Keep failed creative studies available for comparison. Any further generation must fit a distinct authorized request and the cumulative limits.

Deliver the reasoning, exact prompt/request, observed artwork, editable layout sources, validation findings and billing evidence available. Identify which operations were provider generation, local layout, cached reuse or manual review. Do not claim that a newly written skill generated an earlier test.
