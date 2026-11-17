# Mutsu OS Website

Static site for [Mutsu OS](https://github.com/markymark5127/mutsu-os), a calm, Mac-familiar Linux desktop.

## Design

- Japandi liquid-glass look matching the default Mutsu OS desktop: the Japandi wallpaper hero, frosted-glass panels, and the brand palette from `branding/docs/BRAND_GUIDE.md`
- One theme only, with no switcher
- Plain HTML and CSS with no build step. Assets live in `assets/`.

## Download button

The download buttons look up the newest release on GitHub, **including beta pre-releases**:

1. If `ISO_URL` at the bottom of `index.html` is set, every download button uses that direct link.
2. Otherwise, if a release has an `.iso` file attached, the buttons link straight to it and show its size.
3. Otherwise, they open the newest release page (currently `v0.9.0-beta.20261115`).

> GitHub release files must be under 2 GiB. The live ISO is about 5.7 GB, so host it somewhere else (for example SourceForge, Cloudflare R2 or archive.org) and put that link in `ISO_URL`.

## Enable GitHub Pages

1. Go to the repository **Settings** → **Pages**
2. Source: Deploy from a branch
3. Branch: `main` / `/ (root)`
4. Save

The site will be at **https://markymark5127.github.io/mutsu-os-website/**

## Local preview

Open `index.html` in a browser, or run `python3 -m http.server` in this folder.
