# Siren Capital — Board Intelligence Report (Group 007)

A single self-contained `index.html` (no build step, no dependencies beyond two CDNs:
Google Fonts + Chart.js). Hosting it is just "put `index.html` in a repo and turn on Pages."

---

## Option A — GitHub web UI (no terminal, ~3 minutes) ✅ recommended

1. Sign in at **github.com** (create a free account if needed).
2. **New repository** → name it e.g. `board-report` → **Public** → Create.
3. On the repo page: **Add file → Upload files** → drag in **`index.html`**
   (and this `README.md` if you like) → **Commit changes**.
4. **Settings → Pages** → under *Build and deployment*, Source = **Deploy from a branch**,
   Branch = **main**, folder = **/ (root)** → **Save**.
5. Wait ~1 minute, refresh the Pages settings page. Your live URL appears:
   **`https://<your-username>.github.io/board-report/`**

That URL is public, password-free, and shareable. To update later, upload a new
`index.html` (same steps) — Pages redeploys automatically.

---

## Option B — Claude Code (local project + terminal)

Use this if you want a local project you can iterate on. Claude Code needs a **paid Claude
plan** (Pro/Max/Team/Enterprise) and **git** installed; the **GitHub CLI (`gh`)** makes the
push one command.

1. **Install Claude Code** (macOS/Linux/WSL):
   ```bash
   curl -fsSL https://claude.ai/install.sh | bash
   ```
   Windows PowerShell: `irm https://claude.ai/install.ps1 | iex`
   (Or use the Claude **Desktop app** if you'd rather not use a terminal.)

2. Make a project folder and put `index.html` inside it:
   ```bash
   mkdir board-report && cd board-report
   # copy index.html into this folder
   ```

3. Start Claude Code in that folder and let it do the git + GitHub steps:
   ```bash
   claude
   ```
   Then ask it:
   > "Initialise a git repo here, create a public GitHub repo called board-report,
   >  push index.html, and enable GitHub Pages on the main branch."

   Or run it yourself (after `gh auth login`):
   ```bash
   git init && git add . && git commit -m "Board report"
   gh repo create board-report --public --source=. --push
   # then enable Pages in Settings → Pages (branch: main, folder: / root)
   ```

Result is the same live URL as Option A.

---

## Notes

- **Free GitHub Pages requires a public repo.** (Pages on private repos needs a paid GitHub plan.)
- **`index.html` is the magic filename** — it loads automatically at the repo root.
- This page already works as-is on **tiiny.site**; the fastest no-account alternative is
  **app.netlify.com/drop** — drag the file onto the page and you get an instant URL.
- Keep your group number visible (it already is) and test the final link in a private window.
