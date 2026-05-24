# masonnix.com

Interactive resume website for Mason L. Nix.

**Live site:** [masonnix.com](https://masonnix.com)

## Stack

- Vanilla HTML/CSS/JS (no build step)
- **Cloudflare Pages** hosting (project `masonnix`)
- Cloudflare DNS

## How it is hosted & deployed

Hosted on **Cloudflare Pages** — project `masonnix` (`masonnix.pages.dev`), with
`masonnix.com` and `www.masonnix.com` attached as custom domains. The site files
(`index.html`, the PDF, etc.) live at the repo root; repo docs like `README.md`
and `CLAUDE.md` are excluded from the published site.

- **Automatic (live method): push to deploy.** Commit and push to `main` and it
  deploys automatically — `.github/workflows/deploy.yml` runs on every push to
  `main`, stages the public files into a clean `dist/` (via rsync, excluding
  `.git`, `.github`, `README.md`, `CLAUDE.md`), and runs `wrangler pages deploy
  dist`. Auth is via encrypted repo secrets (`CLOUDFLARE_API_TOKEN`,
  `CLOUDFLARE_ACCOUNT_ID`) — no token in the repo. (Direct pushes to `main` are
  allowed; no PR required.)
- **Manual fallback** (machine with the Cloudflare token at
  `~/.config/cloudflare/env`) — deploys the repo root as-is:
  ```sh
  source ~/.config/cloudflare/env
  npx --yes wrangler@latest pages deploy . --project-name masonnix --branch main
  ```

> Migrated off GitHub Pages 2026-05-24. GitHub Pages is no longer used for this
> site; the `CNAME` file is a harmless leftover.

## Features

- Dark theme with purple/cyan gradient accents
- Interactive cards with 3D hover effects
- Scroll-triggered timeline animations
- Mobile responsive
- PDF resume download

## Local Development

```bash
python -m http.server 8000
# or
bun serve
```

Then visit http://localhost:8000
