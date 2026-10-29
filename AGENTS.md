# Repository Guidelines

## Project Structure & Module Organization

This repository contains standalone drawings made with HTML and CSS. Each top-level drawing directory (`FERB-FACE/`, `SHANAB/`, `Pokemon/`, `Homer/`, `cartoon-face/`, `apple/`, and `rolex/`) contains an `index.html`, a `style.css`, and a PNG preview. Drawing shapes must use HTML/CSS; screenshots belong in documentation, not in the rendered artwork. Do not introduce JavaScript, SVG, or image-based drawing elements.

`README.md` displays the gallery. For a new drawing, create a separate directory with the same three-file layout and add a gallery cell using relative paths. Keep three cells per row, use a 250px-wide thumbnail linked to the full-size PNG, and link the drawing name to its directory.

## Build, Test, and Development Commands

- `open Homer/index.html`: preview a drawing in the default browser on macOS. Elsewhere, open the HTML file directly in a browser.
- `git diff --check`: check changes for whitespace errors before submitting.

There is no build step, package manager, development server, automated test suite, linter, or formatter configured.

## Coding Style & Naming Conventions

Match the file being edited: HTML generally uses four spaces, while CSS indentation varies between tabs and spaces. Avoid unrelated reformatting.

Use descriptive shape classes such as `.face`, `.eye`, or `.prong`. Define reusable colors as `:root` custom properties where appropriate. Preserve each drawing's unit choices (`px`, percentages, or `vmin`), positioning, and DOM stacking order. Keep existing selector spellings, including `befor-element` in `cartoon-face/`, unless updating every matching reference.

## Testing Guidelines

Validate changes visually in a browser. Compare the drawing with its PNG preview, inspect overlapping shapes and alignment, and resize the viewport to check scaling or clipping. Update the screenshot when the intended appearance changes. For gallery edits, verify thumbnail, full-size image, and directory links. No automated coverage threshold is configured.

## Commit & Pull Request Guidelines

Recent commits use short descriptive subjects, such as `Replace Citizen logo with Rolex crown` and `Show README drawings as a thumbnail gallery`; no enforced prefix format is evident. Keep commits focused on one drawing or documentation change.

Pull requests should describe the affected drawing and intended visual change, list manual checks, and include before/after screenshots for artwork changes. Link an issue when relevant.
