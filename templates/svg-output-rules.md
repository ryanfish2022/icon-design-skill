# SVG production rules

## Default UI icon
Use a 24×24 viewBox, 2-unit stroke, rounded caps and joins, no fill, and currentColor for monochrome icons. Example:

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
  <path d="M12 3v12m-5-5 5 5 5-5M5 16v4h14v-4"/>
</svg>
```

## Production requirements
- Use optical padding (often around 2 units) and inspect stroke extents to avoid clipping.
- Filled icons should use fill=currentColor without unnecessary strokes.
- Multicolor icons should use explicit approved hex values.
- Use stable unique IDs for gradients when needed; avoid expensive filters at small sizes.
- Use editable paths and simple primitives; keep geometry understandable.
- No scripts, event handlers, external resources, embedded bitmap images or foreignObject.
- Decorative inline SVG should use aria-hidden=true; meaningful standalone icons need an accessible name appropriate to integration.
- Validate XML and render with a trusted SVG renderer when possible.
- Inspect at 16, 20, 24 and 32 px for UI use.
- Render PNG previews at requested dimensions with explicit color and alpha settings.

A realistic clay/glass PNG may need a simplified vector companion. Explain the fidelity tradeoff. Never embed the raster image inside an SVG and describe it as vectorized.
