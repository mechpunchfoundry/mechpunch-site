# mechpunch-site

The MechPunch Foundry website — a static site, no build step.

Live at **https://www.mechpunch.com** (GitHub Pages).

## Layout

```
index.html    the whole homepage: markup, styles and the fist sting, inlined
assets/       what the site serves — icons, og card, wordmark SVGs
CNAME         custom domain for GitHub Pages
```

Source art (`art/`) is deliberately not in this repo — see `.gitignore`.

## Working on it locally

```sh
python3 -m http.server 8080
```

Then open http://localhost:8080. The opening sting is skipped if your system
is set to reduce motion, or after the first view in a session (`sessionStorage`).
