# Galcon-Sentek Brand Guidelines 2026

Static site of the Galcon-Sentek brand identity guidelines, by OZ GLOBAL B2B.
No build step: `index.html` plus the `assets/` folder is the whole site.

## Publish on GitHub Pages

1. Create a repository and push these files to the `main` branch.
2. In the repository: Settings → Pages → Source: "Deploy from a branch" → `main`, folder `/ (root)`.
3. The site is served at `https://<account>.github.io/<repository>/`.

All paths are relative, so the site works under any repository name or custom domain.
`.nojekyll` tells GitHub Pages to serve the files as they are.

Note: a public repository makes the logo files and the guideline public.
The page carries `noindex`, which keeps it out of search results but does not restrict access.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole guideline (markup, styles and script) |
| `assets/logo/` | Logo files in SVG and PNG, offered as downloads on the page |
| `assets/img/` | Visuals cropped from the guideline PDF |
| `brand-story.json` | Source text of chapter 10.0 Verbal Language (draft, pending approval) |
| `build-voice.py` | Rebuilds chapter 10.0 inside `index.html` from `brand-story.json` |

## Editing the Verbal Language chapter

```bash
python3 build-voice.py
```

Edit `brand-story.json`, run the command in this folder, then commit `index.html`.
Other chapters are edited directly in `index.html`.

## Preview locally

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173
