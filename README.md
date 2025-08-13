## Kleine AT website

Static site for the Kleine AT workshop series.

Once published as a user/organization site at `https://kleineat.github.io/`, this repo serves the homepage for the series and each upcoming edition.

### Repo layout

- `index.html`: main HTML page
- `assets/`: CSS, JS, images, PDFs
  - `assets/styles.css`: styling
  - `assets/main.js`: small UX helpers; also auto-updates footer year
  - `assets/Kleine_AT_Syllabus.pdf`: program/abstracts PDF (replace per event)

### How GitHub Pages serves this site

If this repo is named `kleineat.github.io` (user/organization site), GitHub Pages serves from the REPO ROOT by default.

- Status: Already configured. Content lives at the root (`/index.html`, `/assets/`).
- Recommended: add a root `.nojekyll` file to disable any implicit Jekyll processing (optional but safe for pure static sites).
- Deploy: push to the default branch (e.g., `main`) and Pages will serve from `/` automatically.

Optional (advanced): You can deploy with GitHub Actions if you ever change structure or want previews, but it is not required when serving from the repo root.

### Add or update an event (checklist)

All edits live in `index.html` and `assets/`.

1) Update metadata (SEO/social)

- Edit `<title>` and the main meta description near the top of `index.html`
- Update Open Graph tags (`og:title`, `og:description`, `og:url`) if needed

2) Update the hero copy

- In the first section under `<main>`, update the heading and intro text if you want edition-specific messaging

3) Update the “Next event” card

- In the `<aside id="next">` block, change:
  - Date/time (📅)
  - Venue (📍)
  - Theme (🧭)
  - Organisers list

4) Replace the syllabus/program PDF

- Put the new file in `assets/` (e.g., `Kleine_AT_Syllabus.pdf`)
- Update the link in the “Inaugural theme” section to point to the new filename

5) Edit the schedule

- Update the rows in the “Day schedule” section to match the new agenda

6) Registration link

- Replace the placeholder `href="#"` with the live form URL once available

7) Footer year

- No action needed; it is auto-updated by `assets/main.js`

There are inline maintainer comments in `index.html` pointing to each edit location.

### Local preview

Open `index.html` directly in a browser.

### Conventions

- Keep all static assets under `assets/`
- Use relative links like `assets/...` from `index.html`
- Prefer accessible content: use meaningful link text, ensure contrast, keep headings logical

### Troubleshooting

- 404 on assets: verify files are under `assets/` and links in `index.html` are relative (`assets/...`)
- Social previews wrong: clear caches and confirm `og:` tags are correct
- Registration link not working: ensure full `https://` URL and that the form is published publicly


