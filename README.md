# Mutsu OS Website

Static site for [Mutsu OS](https://github.com/markymark5127/mutsu-os), a calm, Mac-familiar Linux desktop.

## Design

- Japandi liquid-glass look matching the default Mutsu OS desktop: the Japandi wallpaper hero, frosted-glass panels, and the brand palette from `branding/docs/BRAND_GUIDE.md`
- One theme only, with no switcher
- Plain HTML and CSS with no build step. Assets live in `assets/`.

## Downloads

The Download section reads the newest Mutsu OS release from GitHub, **including beta pre-releases**, and lists the live USB parts that the `beta-release` workflow attaches:

- **Online** (`mutsu-os-<version>-live-online.iso.7z.001`, `.002`, …): about 5 GB, installs over the internet
- **Offline** (`mutsu-os-<version>-live.iso.7z.001`, `.002`, …): about 21 GB, installs without internet

Each download comes with its `.iso.sha256` file. The parts are uncompressed 7-Zip volumes of 2000 MiB each, because GitHub limits release files to 2 GiB. Until the parts are attached (about an hour after a beta is published), each card links to the release page.

The **Build the disk image** panel has Linux, Windows and macOS steps for joining the parts into the bootable ISO (`7z x …7z.001`), checking it with `sha256sum`, and writing it to USB. The file names in the commands update to match the current release and the Online/Offline choice.

## Enable GitHub Pages

1. Go to the repository **Settings** → **Pages**
2. Source: Deploy from a branch
3. Branch: `main` / `/ (root)`
4. Save

The site will be at **https://markymark5127.github.io/mutsu-os-website/**

## Local preview

Open `index.html` in a browser, or run `python3 -m http.server` in this folder.
