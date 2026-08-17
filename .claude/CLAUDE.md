# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

This is a static, no-build site: no `package.json`, no test runner, no linter.

- Preview: open `index.html` directly in a browser, or serve the directory with any static file server.
- Deploy: pushing to `main` publishes automatically via GitHub Pages (this repo is the `markomarkotasocial.github.io` user site).
- Node.js/npm/npx and `chromium-cli` are **not installed** in this environment, so the Puppeteer screenshot step in [.claude/rules/workflow.md](.claude/rules/workflow.md) needs its documented manual fallback (open the file in a browser / ask the user for a screenshot) rather than being run directly.

## Architecture

- The entire site is one file, `index.html`. Styling is Tailwind CSS via CDN plus a small inline `tailwind.config` block that defines two custom color tokens, `accent` and `ink` — always restyle through these tokens (and Tailwind utilities) rather than hardcoding hex values or using Tailwind's default palette colors, so a global recolor stays a one-line change.
- Navigation is duplicated by design: the desktop `<nav>` and the JS-toggled `#mobileMenu` block each hardcode their own copy of the same anchor links (`#about`, `#project`, `#skills`, `#contact`). Adding, renaming, or removing a section requires updating both.
- The only JavaScript on the page is the mobile menu toggle at the end of the file.

# Portfolio Website Build

@.claude/rules/workflow.md
@.claude/rules/technical-defaults.md
@.claude/rules/content-rules.md

## Portfolio Content

Use this content exactly — do not invent or embellish beyond what's provided:

**Hero**
- Name: Marko Markota
- Title: [npr. .NET / Azure Developer — 14 years of experience]
- CTA: link to contact section or LinkedIn

**About**
- 14 years in IT, focused on .NET, recently expanded into .NET MAUI
- Experience across Azure (App Service, SQL Server, query/index optimization), client-facing support
- Currently exploring GitHub AI agents / Claude Code in workflow
- Remote-first, flexible with hours, project-driven mindset

**Featured Project — Fabrizio App**
- Cross-platform travel planning app (.NET MAUI client + .NET 8 layered API)
- Layered architecture: API / BLL / DAL / Repository / Shared (DTOs) / MAUI client
- Azure App Service + Azure SQL Server, JWT authentication
- GitHub Actions CI/CD
- Link to GitHub repo: [LINK]

**[Additional projects — TO BE ADDED]**

**Skills**
- .NET 8, .NET MAUI, C#
- Entity Framework Core
- Azure (App Service, SQL Server, Functions, WebJobs)
- Query/index optimization
- JWT authentication, REST APIs
- GitHub Actions / CI-CD
- Client-facing support / communication

**Contact**
- [Email / LinkedIn / GitHub — po tvom izboru]
