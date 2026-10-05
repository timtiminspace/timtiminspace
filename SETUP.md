# Profile README maintenance

The animated header is generated from `terminal.yml` and committed to this repository. GitHub renders the generated SVG without running scripts in the README.

## Regenerate locally

Node.js 22 or newer is required.

```bash
npx svg-terminal generate --config terminal.yml --output terminal.svg --strict
npx svg-terminal generate --config terminal.yml --output terminal-static.svg --static --strict
```

The static file is used when a visitor has enabled reduced-motion preferences.

## Regenerate with GitHub Actions

Run **Actions → Refresh profile terminal → Run workflow**. The workflow also runs each Monday at 12:00 UTC and commits changed output files automatically.

## Repository structure

```text
timtiminspace/
├── .github/
│   └── workflows/
│       └── refresh-svg.yml
├── README.md
├── SETUP.md
├── terminal.yml
├── terminal.svg
└── terminal-static.svg
```

Edit project copy in `README.md` and terminal content in `terminal.yml`. Keep the two synchronized when projects or interests change.
