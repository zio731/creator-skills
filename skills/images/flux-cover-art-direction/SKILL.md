---
name: flux-cover-art-direction
description: Turn a verified book brief and a planned cover composition into a FLUX illustration prompt, then judge the returned art at cover and thumbnail size.
---

Start with the book's audience, promise, and one concrete scene or object supported by the brief. Choose a visual metaphor only if it communicates the same promise. Keep source covers as references for genre conventions and build an original composition.

Specify the image's role in the layout before writing the prompt. For a panel, define the focal point and the safe crop. For artwork behind a title, specify which side must stay quiet, what its dominant tone should be, and where the subject belongs. Use the crop ratio the renderer will actually place.

Write the prompt in this order:

1. Subject and a single observable action.
2. Viewpoint, main shape and position, and space reserved for the layout.
3. Illustration technique, palette, and lighting tied to the audience.
4. Output boundaries. Request artwork without lettering, logos, mockups, or frames. Compose the title and subtitle as editable type in the renderer.

Make each variant test a different visual decision, such as an overhead composition versus a close side view. Avoid vague quality adjectives. Keep the prompt and its model, dimensions, and seed with the asset receipt so that a later run can reproduce the request.

Inspect the placed artwork and the complete cover at 160 px. Verify that the subject reads at that size, the focal point survives cropping, and the title zone has enough contrast. Record what to change before requesting another variant. Check the effective print resolution at the actual placement size.

## References

- [Image Prompt and Cover Maker](https://github.com/Mikefluff/skills) for model-aware briefs and distinct cover variants.
- [Black Forest Labs FLUX.2 klein guidance](https://help.bfl.ai/articles/7592221790-how-do-i-generate-quickly-with-flux-2-klein) for model-specific prompting.
- [Awesome Free LLM APIs](https://github.com/open-free-llm-api/awesome-freellm-apis) and [Public APIs](https://github.com/public-apis/public-apis) for provider discovery. Verify current account limits and terms against the provider before executing.
