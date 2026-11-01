# Aman Singh portfolio

The original Lovable React design, adapted for GitHub Pages without a Lovable runtime.

Live URL: https://kingaman11.github.io/Aman.Singh.github.io/

## Develop

Use Node.js 22.16 or newer (Node 22 LTS recommended).

```sh
npm ci
npm run dev
```

## Verify and build

```sh
npm test
npx tsc --noEmit
npm run build
```

The output is in dist/. The project base path is /Aman.Singh.github.io/.
All images are included locally. Google Fonts is used, as on the original site.

## Publish

For a normal source checkout, commit this directory's contents to your repository and select Settings → Pages → Source → GitHub Actions. The included .github/workflows/deploy.yml builds, tests, and publishes on pushes to main.

For the browser-upload deployment, built files live at the repository root and the complete editable project is included as portfolio-source.zip. Extract that ZIP to edit the website, then build and upload the contents of dist/ to the repository root. Keep Pages configured to deploy from main, / (root), for this mode.

The old server entry points are retained as .original files for reference; they are not required for this browser-only portfolio. No visible component content or styling was redesigned.

## Static-first delivery

The production build renders the complete portfolio into index.html at build time, then loads the same React interactions in the browser. The portfolio remains readable if JavaScript fails to load. Search and social metadata have one owner in index.html; sitemap.xml and robots.txt are included in dist/.

Initial section links are aligned once fonts settle, unless the visitor has already interacted. Alert scenarios support arrow keys, Home, and End with a single tab stop, without changing their appearance.

The build verifies that actual portfolio content and unique search metadata are present. Tests include keyboard selection/focus behavior. Renderer files in .prerender/ are build-only and should not be published.
