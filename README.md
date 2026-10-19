# Taskflow

This site is ready to host as a static website. GitHub Pages serves `index.html`,
`styles.css`, and `app.js` directly; Node.js and `node_modules` are not needed
to launch it.

## Publish with GitHub Pages

1. Push this repository to GitHub. The `.gitignore` file excludes `node_modules`.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select your branch and the `/(root)` folder, then save.

GitHub Pages will publish the site at the URL shown in the Pages settings.

## Update the static files

The static `app.js` and `styles.css` are built from the files in `src/`. After
changing the source app or styles, run `npm install` and `npm run build`, then
copy the generated JavaScript and CSS from `dist/assets/` over `app.js` and
`styles.css` before publishing the root files. Upload the updated `index.html`
as well so stylesheet cache-busting changes take effect.

For a build-based deployment instead, publish the contents of `dist/`. Its
asset paths are relative, so it also works when GitHub Pages serves the site
from a repository subpath.
