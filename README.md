# Folio3 IDR Appendix

Static appendix site for the **Folio3 IDR Market Evaluation** readout. Renders the data derivation tables, primary sources, and methodology notes that the readout deck cites.

**Live URL (target):** [folio3-idr-appendix.vercel.app](https://folio3-idr-appendix.vercel.app)

---

## What's in this repo

A single static HTML file (`index.html`). No build step. No framework. No dependencies.

The site mirrors the deck's design system (navy / paper / burgundy / Cambria + Calibri + IBM Plex Mono) so the appendix reads as continuous with the readout.

---

## Deploying to Vercel from GitHub (3 steps)

### 1 · Push this folder to a new GitHub repo

```bash
cd folio3-idr-appendix
git init
git add .
git commit -m "Initial commit — IDR appendix"
git branch -M main
git remote add origin https://github.com/<your-org>/folio3-idr-appendix.git
git push -u origin main
```

### 2 · Connect to Vercel

- Go to [vercel.com/new](https://vercel.com/new)
- Click **Import Git Repository** and select the repo you just pushed
- Framework Preset: **Other** (Vercel auto-detects this as a static site)
- Build Command: *(leave blank)*
- Output Directory: *(leave blank — defaults to repo root)*
- Click **Deploy**

### 3 · Set the custom domain

- In your Vercel project → **Settings → Domains**
- Add `folio3-idr-appendix.vercel.app` (Vercel-provided subdomain — no DNS config needed)
- Or add a custom domain if Folio3 prefers (e.g., `appendix.folio3health.com`)

---

## Updating the appendix

Edit `index.html` directly. Push to `main`. Vercel auto-deploys on commit. There is no build step.

To preview locally before pushing:

```bash
cd folio3-idr-appendix
python3 -m http.server 8000
# Then open http://localhost:8000
```

---

## Structure

```
folio3-idr-appendix/
├── index.html       # The appendix — A.1 funnel, A.2 state pool
├── vercel.json      # Vercel routing config (minimal)
├── README.md        # This file
└── .gitignore
```

The current scope is **Section A · Market only** (A.1 Funnel Derivation + A.2 State + Combined Gap). Sections B–F are disabled placeholders in the nav, reserved for future expansion if the engagement extends.

---

## Source attribution philosophy

Every numerical claim in the readout traces to a primary source. Where a figure is a calculated estimate rather than a directly reported number, the derivation is shown in full — including which inputs are confirmed primary data, which are vendor estimates, and which are working assumptions that should be replaced as better data becomes available.

Three figures are explicitly flagged as vendor-sourced and should be replaced with primary data before final external distribution: the average claim value (~$500, HFMA), the commercial denial rate (~11%, Change Healthcare), and the state IDR eligible pool (10–15M, no published primary source).

---

*Folio3 IDR Final Readout · Appendix · Prepared by Nizam Ali, Independent Consultant*
