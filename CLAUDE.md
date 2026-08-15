# Portfolio Website Build

## Workflow

1. **Generate** a single `index.html` file using Tailwind CSS (via CDN). Include all content inline — no external files unless requested.

2. **Reference screenshots** will be provided by the user showing the desired visual style (layout, spacing, colors, typography, section structure). Use these as the primary design reference — not as content to copy, only as style/layout inspiration.

3. **Populate** the page using the content in the "Portfolio Content" section below — never invent placeholder text, names, or projects not listed there.

4. **Screenshot** the rendered page using Puppeteer (`npx puppeteer screenshot index.html --fullpage` or equivalent). If the page has distinct sections, capture those individually too.

5. **Compare** your screenshot against the reference image(s). Check for mismatches in:
   - Spacing and padding (measure in px)
   - Font sizes, weights, and line heights
   - Colors (exact hex values)
   - Alignment and positioning
   - Border radii, shadows, and effects
   - Responsive behavior
   - Image/icon sizing and placement

6. **Fix** every mismatch found. Edit the HTML/Tailwind code.

7. **Re-screenshot** and compare again.

8. **Repeat** steps 5–7 until the result is within ~2–3px of the reference everywhere.

Do NOT stop after one pass. Always do at least 2 comparison rounds. Only stop when the user says so or when no visible differences remain.

## Technical Defaults

- Use Tailwind CSS via CDN (`<script src="https://cdn.tailwindcss.com"></script>`)
- Light, professional color scheme — clean background, restrained accent color, no dark mode toggle needed
- Mobile-first responsive design
- Single `index.html` file unless the user requests otherwise (this will be deployed to GitHub Pages)
- No build step, no npm dependencies — must run as a static file

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

## Rules

- Do not add features, sections, or content not present in the "Portfolio Content" section above.
- Do not fabricate project descriptions, metrics, or testimonials.
- Do not use stock photos of people — use icons, initials, or a real photo if the user provides one.
- Keep the tone professional, not overly casual or "salesy."
- If a reference screenshot conflicts with the professional/light-theme direction, flag it to the user rather than silently deviating.