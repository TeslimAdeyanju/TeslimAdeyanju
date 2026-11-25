# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

The GitHub profile README for `TeslimAdeyanju` (the repo name matches the username, so GitHub shows `README.md` on the profile page). There is no build, lint or test step. The deliverable is `README.md` as GitHub renders it. Check changes by reading the rendered Markdown/HTML, or by pushing and looking at the profile.

## Structure and conventions

- `README.md` is mostly inline HTML (`<table>`, `<details>`, `<picture>`, `<p align="center">`), because GitHub-flavoured Markdown can't control layout. Keep new content in the same HTML patterns rather than mixing in Markdown tables.
- The header title is an SVG pair, `assets/title-light.svg` and `assets/title-dark.svg`, switched with `<picture>` / `prefers-color-scheme`. Edit both together when you change the name or styling.
- **Selected Portfolio Work** is a 3-column card table. Images are hot-linked from each project repo's `main` branch via `raw.githubusercontent.com`, so renaming a project repo or moving its image breaks the card.
- **Projects by Skill** has one `<details>` block per skill area. Each holds a 4-column table (Project / Tech Stack / Impact / Link) with fixed `width` attributes. Projects that aren't published use `<em>Coming soon</em>` or `<em>In progress</em>` in the Link column instead of a URL. Per recent commits, the planned builds are listed on purpose so the module counts match the owner's Notion tracker. Don't remove them as clutter.
- Rows for the same project can appear in several sections (cards, skill tables, Core Expertise). When you rename a repo or project, update every occurrence.
- `image.png` (root) is the FDA Toolkit overview image used in the README. `assets/fda_toolkit_architecture.png` isn't currently referenced.
- Write in British English (organisation, optimisation, visualisation). Use `&amp;` inside HTML headings and cells.

## Automation

- There are no workflows. The GitHub Activity section is made only of live images: `github-readme-stats.vercel.app` cards and a public WakaTime share chart (`wakatime.com/share/@TeslimAdeyanju/<id>.svg`).
- Don't reintroduce `athul/waka-readme` or any other workflow that calls the WakaTime API with an API key. WakaTime now refuses API keys outside editor plugins (403: "API Keys are only for plugins"), so those workflows fail.
- GitHub doesn't render `<embed>`. Use `<img>` for SVG charts.

## Commits

Commit messages are short, imperative, sentence-case summaries of the content change (for example "Fix ACA wording in About Me" or "Remove status notes from skill section headings"), with no prefixes. Content facts (qualifications, CV link, project stats) are owned by the author. Don't invent or "improve" figures.
