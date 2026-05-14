# Filament Collection Town

A visual color reference for a 3D printing filament collection, hosted via GitHub Pages.

**Live site:** https://goggledefogger.github.io/filament-gallery/

## What's here

- `index.html` — self-contained gallery page (dark mode, filterable by material type)
- `images/` — product photos sourced from manufacturer sites
- `.github/workflows/deploy.yml` — auto-deploys to GitHub Pages on every push to `main`

## Updating

This gallery is generated from a private vault. To update after adding or removing filaments, run from the vault root:

```bash
python3 scripts/publish-filament-gallery.py --push
```

That script:
1. Reads filament metadata from the vault
2. Regenerates the `FILAMENTS` data block in `index.html`
3. Syncs any new/updated images to `images/`
4. Commits and pushes — GitHub Actions handles the Pages deploy automatically

## Stack

Plain HTML + CSS + JS. No build step, no dependencies, no framework.

## License

This project is open source and available under the [MIT License](LICENSE).
