# Upload these files to GitHub — 4 minutes

## 0. Read this first — your repo is currently a dead link

`https://github.com/Rehan199-pixel/Stratanuats-space-mission-` returns **404 Page not found** as of 15 Nov 2026. The account `Rehan199-pixel` has exactly one public repository: `Student-library-management-system`. So the source-code link in your submission currently leads nowhere.

Two ways out:

- **Option A (recommended, keeps every existing link working):** create a new public repo named exactly `Stratanuats-space-mission-` and upload these files.
- **Option B:** create it with a different name, then every place that mentions the old URL must change — the README, the submission description, the Drive documents. If you take this route, send me the new name and I will regenerate the text.

## 1. Create the repository

1. Go to https://github.com/new
2. **Repository name:** `Stratanuats-space-mission-` (copy it exactly — the trailing dash is in your submission links)
3. **Public** (a judge cannot open a private repo without being invited)
4. Do **not** tick "Add a README" — you are uploading your own
5. Create repository

## 2. Upload these files

Fastest way, no command line:

1. On the empty repo page click **uploading an existing file** (or Add file → Upload files)
2. Drag **the contents of this `GitHub-Upload` folder** into the browser: `README.md`, `LICENSE`, `.gitignore`, `AI_USE.md`, `TECH-STACK-AND-CREDITS.md`, `.env.example`, and the whole `docs` folder
   - Dragging the `docs` folder keeps the `docs/` path, which the README needs for its images and links
   - `.gitignore` and `.env.example` start with a dot — if your file browser hides them, switch on "show hidden files" first
3. Commit message: `Documentation, licence, AI disclosure, screenshots`
4. Click **Commit changes**

## 3. What is in here

| File | Why a judge cares |
|---|---|
| `README.md` | What the project is, how it works, NASA data used, stack, how to run it, team, limitations |
| `LICENSE` | © Team The Stratanauts 2026 — free for education, credit required |
| `.gitignore` | Keeps keys and build output out of the repo |
| `.env.example` | Shows the app needs a NASA key, with no real key in it |
| `AI_USE.md` | SI disclosure: which tools, what they did, where it is labelled |
| `docs/nasa-ai-disclosure.md` | Same, mapped to the guide's code / data / audio / image rules |
| `docs/data-sources.md` | Every NASA and JPL endpoint, plus provenance labels |
| `docs/limitations.md` | What is simplified and what is declared but unused |
| `docs/screenshots/` | Four captures of the running app, embedded in the README |
| `TECH-STACK-AND-CREDITS.md` | Every library, asset and source, with attribution |

## 4. What is NOT in here — the actual source code

The application source (`src/`, `package.json`, `public/`, `locales/`) is not in my hands; it lives in your Lovable project and your local folder. Upload it the same way:

1. In Lovable: **GitHub → Connect / Export** to this repo, or download the project zip from your Lovable project settings
2. If you downloaded a zip: unzip it, select everything **inside** it (not the folder itself), and drag it into the repo's upload page
3. Confirm `package.json`, `src/`, `public/` and `locales/` now sit at the repo root, so the README's structure section is true

Until that is done, the repo is honest documentation but it is not "the source code". If the source genuinely cannot be published, say so in the submission instead of claiming a public repo — a judge who clicks a docs-only repo and reads "the repository holds the full source" will mark down Validity.

## 5. Verify before you submit

- Open the repo in an **incognito window** — you should see the README with screenshots, the licence badge in the sidebar, and the `docs` folder
- Click every link in the README: live app, demo, Drive folder
- Check `AI_USE.md` and `docs/` open without a login
- If you published a different repo name, update the *Link to Final Project* / description in the Project tab to match
