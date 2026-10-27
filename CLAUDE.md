# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A collection of standalone illustrations drawn with plain HTML and CSS only. There's no JavaScript, build step, package manager, linter, or test suite. To view a drawing, open its `index.html` in a browser (e.g. `open Homer/index.html`).

## Structure

Each drawing has its own top-level folder (`FERB-FACE/`, `SHANAB/`, `Pokemon/`, `Homer/`, `cartoon-face/`) with three files:
- `index.html`: markup made of empty `<div>`s, one per shape (head, eyes, mouth, collar, etc.)
- `style.css`: all the drawing logic
- a `.png` screenshot of the finished result, which `README.md` embeds

When you add a new drawing, follow the same layout: a new folder with `index.html`, `style.css`, and a screenshot. Then add a `## [<Name>](<folder>)` section with the screenshot to `README.md`, using relative paths (`![<Name>](<folder>/<file>.png)`).

## CSS drawing conventions

- Colors live in CSS custom properties on `:root` (e.g. `--skin`, `--hair`, `--color-yellow`) and are used via `var(...)`.
- Shapes are placed with `position: absolute` inside a centered `.container`. Size and position come from `border-radius`, borders, and transforms.
- Units differ between drawings. Some use `vmin`/percentages so they scale with the viewport (e.g. `cartoon-face`), others use fixed `px`. Stay consistent with the drawing you're editing.
- `index.html` order matters: later elements stack on top of earlier ones unless `z-index` is set.
- `cartoon-face` uses shared utility classes (`befor-element`, `after-element`, `custom-border`, `custom-radius`) that turn on `::before`/`::after` pseudo-elements or a common border/radius. Keep the existing `befor` spelling, because the CSS selectors depend on it.
