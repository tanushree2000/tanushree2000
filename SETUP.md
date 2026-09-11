# Setup checklist

This repo has been renamed and re-branded for **Tanushree Poojary / github.com/tanushree2000**,
role **AI-Powered PM**, terminal handle **tanu@aipm**. All the structural stuff (name, username,
handle, GitHub Action targets, repo links) is already wired up correctly.

What's *not* filled in yet are Shehab's specific personal facts — his numbers, his projects, his
bio. Every one of those has been replaced with a clearly marked `TODO` placeholder rather than
carried over, since they aren't true of you. Search the repo for `TODO` (87 hits) to find them all:

```
grep -rn "TODO" . --include=*.md --include=*.js --include=*.html
```

## 1. Fill in the placeholders

- **`README.md`**
  - Tagline line near the top (`TODO: your one-line tagline...`)
  - Signal badges: `Product_launches`, `Users_impacted`, `PMs_coached` numbers
  - The whole **Projects** table (4 category columns) — replace with your real repos
  - **Connect** section: website, LinkedIn, WhatsApp number, booking link (search `TODO-your-`,
    `TODO_PHONE_NUMBER`, `TODO-your-booking-link.com`)
- **`scripts/gen_about.js`** — the `--tldr` line (titles + headline metrics) and the `--how-i-work`
  bullets (sample voice, rewrite as your own)
- **`scripts/gen_stats.js`** — the 6 impact tiles (`TILES` array)
- **`scripts/gen_projects.js`** — the sample `info project-1` / `info project-2` terminal lines
- **`scripts/gen_terminal.js`** — `shipping since TODO_YEAR`
- **`scripts/gen_languages.js`** — the `LANGS` array is Shehab's real language mix; swap in yours
  (GitHub shows this on any repo's sidebar, or run `scc --by-repo` locally)
- **`docs/index.html`** — this is the interactive terminal (served via GitHub Pages). It has its
  own copies of the same data: `PROJECTS` object, `impact()`, `neofetch()`, `projects()`,
  `SITE` links object, and the `about()`/`resume()` narrative text. Keep these in sync with the
  README so the live terminal matches.

## 2. Regenerate the SVGs after editing the scripts

The `.svg` files in the repo root are generated, not hand-edited. After changing anything in
`scripts/gen_*.js`, regenerate locally:

```
node scripts/gen_terminal.js
node scripts/gen_stats.js
node scripts/gen_languages.js
node scripts/gen_about.js
node scripts/gen_projects.js
```

(`.github/workflows/refresh.yml` also does this automatically once a day after you push.)

## 3. Photos

- `docs/assets/me.png` — already set to your photo, pre-cropped and vignetted (soft light
  background) so the braille dot-art in the interactive terminal renders cleanly. If you swap in a
  different photo later, a plain/light background works much better than a busy outdoor one for
  the dot-conversion — see `docs/assets/README.md`.
- `assets/website-hero.png` — a simple generated banner (navy background, your photo, name, and
  role). Feel free to redesign it; it's just a static image referenced from the README's Connect
  section.

## 4. Push it up as your GitHub profile repo

GitHub shows this README on your profile page **only** if the repo is named exactly your username.

```
cd tanushree2000
git init
git add .
git commit -m "Initial profile"
git branch -M main
git remote add origin https://github.com/tanushree2000/tanushree2000.git
git push -u origin main
```

If `github.com/tanushree2000/tanushree2000` doesn't exist yet, create it first on GitHub (public,
no README/gitignore/license — this repo already has those) before pushing.

## 5. Turn on GitHub Pages (for the interactive terminal)

Repo → Settings → Pages → Source: **Deploy from a branch** → Branch: `main`, folder **`/docs`**.
It'll be live at `https://tanushree2000.github.io/tanushree2000/` within a minute or two — this is
the URL already wired into the README's terminal link and CTA button.

## 6. Kick off the auto-generating Actions once

The three workflows in `.github/workflows/` run on a schedule, but you can trigger them manually
right after your first push so the SVGs match your real GitHub activity immediately:

Repo → Actions → pick each workflow → **Run workflow**:
- `Refresh terminal + impact` — regenerates terminal.svg, impact.svg, languages.svg, about.svg,
  projects.svg from the scripts
- `Contribution snake` — needs no extra setup, uses the public `Platane/snk` action
- `Metrics isocalendar` — uses `lowlighter/metrics`; the default `GITHUB_TOKEN` works for public
  contribution data. If your calendar looks sparse/wrong, add a personal access token as a repo
  secret named `METRICS_TOKEN` (Settings → Secrets and variables → Actions)

## 7. Toolbox badges

The **🧰 Toolbox** section in the README (Jira, Figma, Amplitude, etc.) was left as a generic
reusable template — trim it down to tools you actually use.
