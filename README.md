# OmniShop releases

Landing and download page for OmniShop. The application source lives in
[`pnoch/omnishop`](https://github.com/pnoch/omnishop).

## Website

The page is in `docs/` and is served by GitHub Pages at
<https://omnishop.siamcreations.app/> (custom domain) and
<https://pnoch.github.io/omnishop-releases/> (project URL until the custom
domain is live).

- **Custom domain:** `docs/CNAME` contains
  `omnishop.siamcreations.app`. DNS uses GitHub Pages **A/AAAA records**, not a
  CNAME: `web.omnishop.siamcreations.app` is a child CNAME to Railway, and a
  parent CNAME at `omnishop` would shadow it in some resolvers.
- **Android download:** the page reads the rolling `android-latest` release in
  `pnoch/omnishop` through the GitHub API and links the first `.apk` asset.
  Publish a new APK by replacing that release's asset (new tag, or delete and
  re-upload). The asset should be named `OmniShop-<version>.apk` so the page can
  show the version.
- **Desktop download:** links to `pnoch/omnishop/releases/latest`.
- **Web app:** links to <https://web.omnishop.siamcreations.app>.
- **App links:** the Android/iOS association files are served by the app at
  `web.omnishop.siamcreations.app`, not by this release page.

## Updating screenshots

Replace `docs/screenshots/desktop-watchlist.png` and
`docs/screenshots/android-product.png`. Keep the desktop image wide
(1440×900-ish) and the phone image portrait (390×844-ish).

## Deploy

Push to `main`. GitHub Pages builds from `main` / `docs`.
