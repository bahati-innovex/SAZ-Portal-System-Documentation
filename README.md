# SAZ Portal System Documentation

Static mirror of the SAZ Portal system documentation, published via GitHub Pages.

Live: https://bahati-innovex.github.io/SAZ-Portal-System-Documentation/

## How this stays in sync

The Claude artifact at `https://claude.ai/artifact/Jfc6TAfof7ymofx5CGeZch` is
the editable source. `index.html` in this repo is a plain export of that
page's HTML, wrapped in a minimal `<html><head>...<body>` shell so it runs
standalone outside the artifact viewer.

Every push to `main` redeploys Pages automatically
(`.github/workflows/pages.yml`, via `actions/deploy-pages`).

To publish a new revision:

1. Edit/republish the artifact as usual.
2. Pull its current HTML and overwrite `index.html` in this repo.
3. Commit and push to `main`. Pages redeploys within ~1 minute, no manual
   step in the GitHub UI.

No build step, no bundler — `index.html` is served as-is.
