# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Quarto book project for "Masterclass AI" - a Dutch-language educational workbook about strategic AI implementation for organizations. The book covers AI strategy, governance, workforce impact, and implementation roadmaps.

## Build Commands

```bash
# Render the book (HTML and PDF output)
quarto render source/

# Preview with live reload
quarto preview source/

# Render specific format only
quarto render source/ --to html
quarto render source/ --to pdf
```

## Project Structure

- `source/` - Quarto source files (.qmd), images, bibliography, and supporting data
- `source/_quarto.yml` - Book configuration (chapters, title, formats)
- `source/references.bib` - Bibliography in BibTeX format
- `book/` - Rendered output (HTML + PDF), auto-generated from `source/`
- `data/use-cases.json` - AI use case examples with company, sector, and value factors

## Chapter Order

Defined in `source/_quarto.yml`:
1. index.qmd - Foreword (Voorwoord)
2. intro.qmd - Strategic significance of AI
3. work.qmd - AI impact on work
4. governance.qmd - Regulation and governance
5. strategy.qmd - Strategic positioning
6. implementation.qmd - Implementation success factors
7. references.qmd - Bibliography

## Content Guidelines

- All content is in Dutch
- The book uses `jupyter: python3` for executable code cells
- Images are stored in `source/images/`
- Supporting documents are in `source/docs/`

## Technical Notes

### Raw HTML in Quarto
For custom HTML diagrams that need to render properly (not as code), use the raw HTML block syntax:

````markdown
```{=html}
<div class="my-diagram">
  <style>/* CSS here */</style>
  <!-- HTML content -->
</div>
```
````

Example: The AI Portfolio Matrix in `implementation.qmd` uses this approach for the interactive 4-quadrant diagram with central "Transfer" circle.
