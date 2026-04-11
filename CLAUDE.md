# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal academic portfolio site for Sohom Chatterjee, deployed via GitHub Pages at `sohomchatterjee.com`. It is a single-page site built on the [Miniport](https://html5up.net/miniport) template by HTML5 UP.

## Architecture

The entire site is a single HTML file: [index.html](index.html). All content edits happen there.

**Page sections** (navigated via anchor links in the nav bar):
- `#top` — Intro/bio with profile photo and social links
- `#publications` — Academic publications list
- `#projects` — Hackathon and course projects
- `#work` — Work experience
- `#teaching` — Teaching experience
- `#awards` — Awards and honors

**Assets:**
- [assets/sass/main.scss](assets/sass/main.scss) — SASS source for the theme. Compiled output is [assets/css/main.css](assets/css/main.css).
- [assets/js/main.js](assets/js/main.js) — Theme JS (scroll behavior, nav highlighting).
- [assets/css/fontawesome-all.min.css](assets/css/fontawesome-all.min.css) + [assets/webfonts/](assets/webfonts/) — FontAwesome icons.
- [files/](files/) — PDFs linked from the page (resume, course project papers).
- [images/](images/) — All images used on the page.

## Styling

There is **no build system**. The SASS files are pre-compiled; [assets/css/main.css](assets/css/main.css) is the live stylesheet read by the browser.

- To change theme-level styles, edit [assets/css/main.css](assets/css/main.css) directly (or compile the SASS manually with `sass assets/sass/main.scss assets/css/main.css` if Sass CLI is available).
- Section- and component-level overrides are written as inline `<style>` blocks at the top of [index.html](index.html) — this is the established pattern for this repo. Continue using inline styles for targeted tweaks rather than modifying main.css.

## Deployment

Pushing to `main` deploys automatically via GitHub Pages. The custom domain is configured in [CNAME](CNAME) (`sohomchatterjee.com`). There is no CI or build step — the HTML/CSS/JS is served as-is.
