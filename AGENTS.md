# AGENTS.md

Guidance for AI coding agents working in this Shopify theme.

## Scope

- This repository is a Shopify Online Store theme (Liquid/CSS/JS, no app backend).
- Make minimal, targeted edits; do not refactor broadly unless requested.

## First Checks

1. Review the project layout in [README.md](README.md).
2. Validate quality gates before finishing changes:
    - CI lint reference: [.github/workflows/ci.yml](.github/workflows/ci.yml)
    - Theme Check config: [.theme-check.yml](.theme-check.yml)
    - Formatting rules: [.prettierrc.json](.prettierrc.json)

## Repository Map

- [layout/](layout/) for theme shell files.
- [templates/](templates/) for page templates.
- [sections/](sections/) for section markup + schema.
- [snippets/](snippets/) for reusable Liquid fragments.
- [assets/](assets/) for CSS and JS behavior.
- [config/](config/) for theme settings schema/data.
- [locales/](locales/) for translation keys used by `t:` lookups.

## Required Style Preferences

1. Do not introduce new BEM class names (`__` / `--`) in new CSS, Liquid, or JS hooks.
2. When modifying existing BEM-based markup/selectors, keep current selectors compatible unless the task explicitly requests a naming migration.
3. Use minimal Shopify section settings:
    - Add only settings that are required for the requested feature.
    - Prefer sensible defaults over many toggles.
    - Avoid decorative/redundant settings that do not materially change behavior.
    - Add blocks only when repeatable content is required.
