# Through Their Eyes — A Day in the Life of Colour-Vision Deficiency

An interactive, bilingual data-storytelling experience that puts the user in the shoes of someone with colour-vision deficiency (CVD). Built as a static single-page website with HTML5, CSS3, and vanilla JavaScript.

---

## What this project is about

Colour-vision deficiency affects roughly **1 in 12 men** and **1 in 200 women** worldwide — around **350 million people**. Yet many digital interfaces still rely on colour alone to convey meaning.

*Through Their Eyes* turns that statistic into a narrative. Users pick a type of CVD (deutan, protan, tritan, or achromatopsia) and walk through five everyday moments — waking up, choosing clothes, crossing the street, filing an expense report, and taking an elevator — experiencing the friction that colour-only design can create.

---

## Folder structure

```
through-their-eyes-cvd/
├── README.md          # You are here
├── .gitignore         # Files Git should ignore
├── report/            # AI workflow report (Word)
│   └── AI_Workflow_Report_Through_Their_Eyes.docx
└── site/              # The actual website
    ├── index.html     # Single-page markup
    ├── app.js         # Interactions, state, CVD simulator
    ├── i18n.js        # English / Simplified Chinese translations
    ├── style.css      # Styling, animations, responsive layout
    ├── cividis.png    # Cividis colour-map reference
    ├── wcag_aa.png    # WCAG AA conformance badge
    ├── AGENTS.md      # Developer/agent notes
    └── assets/        # Icons and images used in scenes
        ├── android_icon.svg
        ├── apple_icon.svg
        ├── enchroma_with.jpg
        ├── gmail_icon.svg
        ├── japan_pedestrian.png
        ├── japan_traffic_light.png
        ├── spotify_icon.svg
        ├── trello_icon.svg
        └── tube_map.png
```

---

## How to run the site locally

Because the project has no build step, you can run it directly.

### Option 1: Open the file
Open `site/index.html` in your browser.

> Note: some browsers block external resources (Google Fonts, Wikimedia images) when opening HTML directly from the file system.

### Option 2: Use a local server (recommended)
From the project root, run:

```bash
cd site
python -m http.server 8000
```

Then visit: http://localhost:8000

If you prefer Node:

```bash
cd site
npx serve
```

---

## How to edit as a group

1. **Before you start**, pull the latest changes:
   ```bash
   git pull origin main
   ```

2. Make your edits in `site/` or `report/`.

3. Save, commit, and push:
   ```bash
   git add .
   git commit -m "Short description of what changed"
   git push origin main
   ```

4. If someone else pushed while you were working, Git will ask you to pull first:
   ```bash
   git pull origin main
   # resolve any conflicts if prompted, then push again
   git push origin main
   ```

### Tips for group work
- Do **not** commit IDE folders (`.idea/`, `.vscode/`) or virtual environments (`.venv/`). They are already ignored in `.gitignore`.
- The Word report is a binary file, so Git cannot show word-by-word diffs. If several people need to edit it at the same time, consider using a shared Google Doc and exporting the final version into `report/`.
- For the HTML/CSS/JS files, GitHub will show exactly what changed, who changed it, and when.

---

## Deploying to GitHub Pages

You can share the live site for free using GitHub Pages:

1. Go to the repository on GitHub.
2. Click **Settings** → **Pages**.
3. Under **Source**, select **Deploy from a branch**.
4. Choose `main` and `/ (root)`, then click **Save**.
5. After a minute or two, the site will be live at:
   ```
   https://fatduckzzz.github.io/through-their-eyes-cvd/site/
   ```
   The `/site/` part is needed because `index.html` lives inside the `site/` folder.

---

## Key features

- **Vision simulation** — SVG colour-matrix filters approximate deutan, protan, tritan, and achromatopsia vision.
- **Bilingual** — full English and Simplified Chinese support via `i18n.js`.
- **Accessible** — keyboard focusable, reduced-motion support, and colour-independent cues.
- **No build tools** — pure HTML/CSS/JS; runs on any static host.

---

## Credits and data sources

- CVD prevalence data and colour-science references are cited inline in the experience.
- External images are hotlinked from Wikimedia Commons with inline SVG fallbacks.
- Fonts are loaded from Google Fonts.

---

## License

This is a student group project. Please check with all team members before reusing assets or code outside the group.
