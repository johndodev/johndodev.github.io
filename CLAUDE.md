# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static portfolio/resume website for Jonathan Plantey (Senior PHP/Symfony developer), hosted on GitHub Pages at `jonathan-plantey.fr`. No build system, no dependencies, no compilation step — just push to `main` and GitHub Pages serves it.

## Architecture

Two source files drive the entire site:

- **`resume.json`** — All content in [JSON Resume](https://registry.jsonresume.org/) schema format (basics, work, education, skills, languages, projects, publications, volunteer).
- **`index.html`** — Single-page HTML with all CSS embedded inline. Renders the resume data directly in markup (not dynamically from the JSON — the two files are kept in sync manually). Sections: masthead, Work, Education, Skills, Languages, Projects, Publications, Volunteer.

When updating content, both files typically need to stay in sync.

## Deployment

Push to `main` → GitHub Pages auto-deploys. CNAME file points to `jonathan-plantey.fr`.
