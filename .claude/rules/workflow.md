# Workflow

1. **Generate** a single `index.html` file using Tailwind CSS (via CDN). Include all content inline — no external files unless requested.

2. **Reference screenshots** will be provided by the user showing the desired visual style (layout, spacing, colors, typography, section structure). Use these as the primary design reference — not as content to copy, only as style/layout inspiration.

3. **Populate** the page using the content in the "Portfolio Content" section of CLAUDE.md — never invent placeholder text, names, or projects not listed there.

4. **Screenshot** the rendered page using Puppeteer (`npx puppeteer screenshot index.html --fullpage` or equivalent). If the page has distinct sections, capture those individually too. If Node/npx/Puppeteer isn't available in the environment, fall back to `chromium-cli` if present; if neither is available, say so explicitly and ask the user to open the file locally and share a screenshot (or feedback) for comparison instead of skipping verification silently.

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

9. **Validate** the HTML markup before considering the page complete — check for unclosed tags, invalid nesting, duplicate IDs, and other structural errors (e.g. via the W3C Markup Validator or an offline HTML linter). Fix anything it flags.

Do NOT stop after one pass. Always do at least 2 comparison rounds. Only stop when the user says so or when no visible differences remain.
