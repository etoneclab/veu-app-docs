# Unterschriftenmappe — public site

Static site for the EBICS VEU iOS app, served through GitHub Pages.

| Page | Content |
|---|---|
| `index.html` | Landing page |
| `benutzerhandbuch.html` | User manual (German), screenshots in `images/` |
| `datenschutz.html` | Privacy policy |

**Do not move or rename `datenschutz.html`.** Its URL is registered in App Store Connect.

## Do not edit this repository directly

This repository is a mirror. The source is the `docs/site/` folder of the main app repository, and it is pushed here with `git subtree`. Changes made directly here will be lost or cause the next push to be rejected.

To update the site, in the main repository:

```sh
# edit files in docs/site/, then commit
Scripts/publish-docs.sh
```

The script refuses to run while `docs/site/` has uncommitted changes. It pushes to the `docs-pages` remote (`git@github.com:etoneclab/veu-app-docs.git`), branch `main`.

## Local preview

Open `index.html` in a browser; the pages are plain HTML with inline styles and no build step.
