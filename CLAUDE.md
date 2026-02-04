# masonnix.com

Interactive resume website for Mason L. Nix hosted on GitHub Pages.

## Project Overview

- **Purpose**: Professional resume/portfolio site
- **Stack**: Vanilla HTML/CSS/JS (no build step, GitHub Pages compatible)
- **Domain**: masonnix.com (pointed to GitHub Pages)
- **Repo**: github.com/nixfred/masonnix.com

## Files

```
masonnix.com/
├── index.html          # Main site (single-page, self-contained)
├── CLAUDE.md           # This file
├── CNAME               # GitHub Pages custom domain (add after setup)
└── MLN_CV_MAY_2024.pdf # Source resume
```

## Design

- Dark theme with purple/cyan gradient accents
- Interactive cards with 3D hover effects
- Scroll-triggered timeline animations
- Mobile responsive
- Gaming/creative industry aesthetic (matches Mason's Blue Ghost role)

## Deployment Checklist

1. Create GitHub repo: `masonnix.com`
2. Push files to main branch
3. Settings → Pages → Enable from main branch
4. Add custom domain: `masonnix.com`
5. Configure DNS at registrar:
   ```
   A     @     185.199.108.153
   A     @     185.199.109.153
   A     @     185.199.110.153
   A     @     185.199.111.153
   ```
6. Enable "Enforce HTTPS"
7. Create CNAME file with `masonnix.com`

## Updates

When updating Mason's resume:
- Edit `index.html` directly
- All styles and scripts are inline (no external dependencies)
- Test locally with `python -m http.server 8000` or `bun serve`

## Contact Info (for reference)

- Mason L. Nix
- Woodstock, GA
- (404) 903-2119
- masonlnix@gmail.com
