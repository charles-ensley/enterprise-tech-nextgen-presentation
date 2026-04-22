# AI assistant instructions (Cursor / Claude)

Use these as **user messages** or **Project Rules** when you want an assistant to **generate or extend** a single-file HTML deliverable that matches the scroll-deck style in this repository.

## System-style preamble (paste once)

You are building a static **scroll-snap presentation** (one HTML file, no framework). Follow `PRESENTATION-FRAMEWORK.md` in this repository for structure, tokens, and accessibility. Reuse patterns from `starter-deck.html`: fixed nav, `.deck-slide` sections, `.sparkle-field` per slide, optional particle canvas, Mermaid for architecture, `prefers-reduced-motion` support. Do not invent confidential customer details; use placeholders. Reserve **one** accent color for the primary CTA. Keep all CSS in a single `<style>` and non-module JS at the end unless Mermaid ESM is required in `<head>`.

## Content request template

> Generate a new HTML file named `YOUR_PROJECT-agentforce-presentation.html` (or a path I specify).  
> - **Industry / segment:** (e.g. B2B financial infrastructure — generic)  
> - **Solution story:** (e.g. Agentforce seller copilot — 3 use cases)  
> - **Required sections:** Intro, Account context (SWOT in four cards, no real company unless I paste approved copy), gap & shift, sales motion stepper, value, architecture principles, **Mermaid** system map, data/specs (tables or tabs), 4-week implementation stepper, closing.  
> - **Do not** use real company names or non-public financials unless I supply them.  
> - **Apply** the dark-navy + electric-blue glass aesthetic from the framework.  
> - **Include** sparkle fields and the grain filter; **omit** the particle canvas if the file is for print/PDF.  
> - **Wire** nav `href`s to every `section id`.

## Iteration template

> Update the Mermaid `graph TD` in the architecture section: reorder Data Model nodes so edges that share a target do not create long crossing lines; merge redundant subgraphs; cap diagram height with `.mermaid-wrap` CSS.  
> Or: **Condense** vertical space: smaller `flowchart.rankSpacing`, shorter node labels, `max-height: 60vh` on the SVG.

## What to load (for humans)

- [starter-deck.html](starter-deck.html) — copy-paste base  
- [PRESENTATION-FRAMEWORK.md](PRESENTATION-FRAMEWORK.md) — full technical contract  
- [README.md](README.md) — overview and quick start  

## Optional narrative skills (Salesforce EHT)

For **storyline** (not code), teams sometimes pair this HTML with `sf-ent-hitech-landing-page` and `sf-ent-hitech-agentforce-solution-blueprint` in a separate Cursor skills bundle—see [PRESENTATION-FRAMEWORK.md §11](PRESENTATION-FRAMEWORK.md#11-optional-cursor--salesforce-eht-narrative-skills).
