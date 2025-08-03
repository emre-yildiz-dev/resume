# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a LaTeX-based resume/CV project using the `res.cls` document class. The main document is `res9b.tex` which contains Emre YILDIZ's professional resume.

## Common Commands

### Building the Resume
```bash
# Build PDF from LaTeX source
pdflatex res9b.tex

# Build with latexmk (handles multiple passes automatically)
latexmk -pdf res9b.tex

# Clean auxiliary files
latexmk -c
```

### Viewing the Output
```bash
# Open the generated PDF
open res9b.pdf  # macOS
```

## Project Structure

- `res9b.tex` - Main resume document containing all content
- `res.cls` - Custom document class for resume formatting (style options: centered/line, overlapped/margin, 11pt/12pt)
- `helvetica.sty` - Optional Helvetica font style (currently commented out in the document)
- `linkedin.png` - LinkedIn logo image (not currently used in the document)
- `res9b.pdf` - Generated PDF output

## Key LaTeX Components

The resume uses custom commands from `res.cls`:
- `\name{}` - Sets the resume owner's name
- `\address{}` - Can be used multiple times for multiple address lines
- `\section{}` - Creates major resume sections
- `\subsection{}` - Creates subsections within sections
- `{\sl text}` - Creates slanted/italic text for emphasis

## Development Notes

- The document class supports style options: `line` (current), `margin`, `centered`, `overlapped`
- Font size options: 10pt (default), 11pt, 12pt
- The resume includes hyperlinks using the `hyperref` package
- Uses `\noindent\hrulefill` for horizontal section dividers