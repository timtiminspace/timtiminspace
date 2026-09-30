# Setup

## Which version should I use?

Use **README_SELF_HOSTED.md** if you want the most original result.

It uses `svg-terminal` to generate a self-contained animated `terminal.svg` that lives in your own GitHub profile repository.

Use **README_HOSTED.md** if you want something you can paste in immediately with almost no setup.

---

## Version 1 — hosted widgets

1. Create a public GitHub repository whose name is exactly your GitHub username.
2. Copy `README_HOSTED.md` into that repository as `README.md`.
3. Replace:
   - `YOUR_GITHUB_USERNAME`
   - `YOUR_LINKEDIN_URL`
   - `YOUR_EMAIL`
   - `YOUR_CV_URL`
4. Replace the generic `my-teditor` repository URL with the actual repository link.

The animated text is provided by Readme Typing SVG.
The skill icons come from skillicons.dev.
The thin accents come from Capsule Render.

---

## Version 2 — self-hosted terminal

Copy these into your profile repository:

- `README_SELF_HOSTED.md` → rename to `README.md`
- `terminal.yml`
- `.github/workflows/refresh-svg.yml`

Then either run locally:

```bash
npx svg-terminal generate --config terminal.yml --output terminal.svg
```

or go to **Actions → Refresh profile terminal → Run workflow**.

The workflow will generate `terminal.svg` and commit it back to the repository.

Before publishing, replace:

- `YOUR_GITHUB_USERNAME`
- `YOUR_LINKEDIN_URL`
- `YOUR_EMAIL`
- `YOUR_CV_URL`

You can change the terminal theme in `terminal.yml`.

Good fits for this profile:
- `oxocarbon` — clean, modern, technical
- `modus-vivendi` — extremely restrained / high contrast
- `nord` — softer blue-grey
- `tokyo-night` — more visibly "developer aesthetic"

I chose `oxocarbon` because it gives the terminal character without making the profile look like a cyberpunk template.

---

## Suggested repository structure

```text
YOUR_GITHUB_USERNAME/
├── .github/
│   └── workflows/
│       └── refresh-svg.yml
├── README.md
├── terminal.yml
└── terminal.svg
```

## One thing I would avoid

Do not fill the page with:
- trophies
- ten different stats cards
- visitor counters
- Spotify
- huge badge walls
- a contribution snake plus multiple other animations

One animated hero is enough. Let the projects be the interesting part.
