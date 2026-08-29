# Python Bench

A polished, instrument-panel styled Python interpreter that runs entirely in the browser via [Pyodide](https://pyodide.org) (CPython compiled to WebAssembly). No backend, no build step — just static files.

## What's inside

- `index.html` — the entire app (markup, styles, and logic in one file)
- `vercel.json` — minimal static-hosting config

## Run it locally

Just open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy to Vercel

**Option A — Vercel CLI**

```bash
npm i -g vercel   # if you don't have it
cd py-bench
vercel            # follow the prompts
vercel --prod     # promote to production
```

**Option B — Git + Vercel dashboard**

1. Push this folder to a GitHub repo.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Framework preset: **Other** (it's a static site — no build command needed).
4. Deploy.

No environment variables, no server code, no API routes — it's a static export, so Vercel deploys it as-is.

## Notes

- First load takes a couple of seconds while the Python runtime downloads (~cached after that).
- `input()` is supported via a browser prompt dialog.
- Everything runs client-side — code never leaves the visitor's tab.
