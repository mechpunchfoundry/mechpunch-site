# mechpunch-site

The MechPunch Foundry website — a static site, no build step.

Live at **https://www.mechpunch.com** (GitHub Pages).

## Layout

```
index.html          homepage; the three.js fist sting is inlined (see below)
pixelsoldiers/      game page, noindex so the homepage stays the way in
404.html            custom not-found page
assets/             site.css, fonts, icons, og cards, game art
robots.txt          crawlers welcome, AI included
sitemap.xml
CNAME               custom domain for GitHub Pages
```

The sting is deliberately inline rather than an external module. Only this
page uses it, so a separate file buys no cross-page caching — and an inline
module keeps working when index.html is opened straight off disk, whereas an
external one gets an opaque origin over `file://` and is blocked.

Source art (`art/`) is deliberately not in this repo — see `.gitignore`.

## Working on it locally

```sh
python3 -m http.server 8080
```

Then open http://localhost:8080. The opening sting is skipped if your system
is set to reduce motion, or after the first view in a session (`sessionStorage`).
