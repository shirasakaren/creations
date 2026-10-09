# Creations by Ren

A static exhibition of fourteen projects, in the supplied order. The home page is a scroll-led story. `/list` is a searchable archive. `/list/:slug` contains the project story, media, and one primary destination.

## Local development

Use Node.js 22 or newer.

```sh
npm ci
npm run dev
```

```sh
npm run check
npm test
npm run build
npm run preview
```

## GitHub Pages

The included workflow builds and deploys pushes to `main`. In the repository's **Settings → Pages**, select **GitHub Actions** as the publishing source. Set your custom domain there when ready. No deployment hostname or CNAME is embedded in the source.

`BASE_PATH` defaults to `/`. The workflow obtains the path from GitHub Pages. To test a project subdirectory locally:

```sh
BASE_PATH=/creations/ npm run build
```

The build emits an HTML document for every route, plus `404.html` and `.nojekyll`. Direct detail links therefore work without a server or rewrite rule. All routes include readable static content before JavaScript runs.

## Content and media

Edit `src/projects.json` for content, ranking, categories, technologies, media, and primary links. Bundled images and videos live in `public/media`. `asset-sources.json` records exact provenance and distinguishes original recordings from animated screenshot studies. Keep links to planned domains even when their deployment is pending.

## Motion and access

The exhibition supports keyboard navigation, a skip link, live search counts, manual video controls, light and dark themes, and reduced motion. The header can pause decorative motion. Offscreen videos and decorative WebGL scenes stop running. The archive falls back to its original DOM presentation when WebGL is unavailable.

## Source and boundaries

The archive, library world, portals, detail transitions, and image interactions are adapted from the user-supplied `MGM-Laboratory/mgm-website` repository at revision `b962558e3ffbdeb356b2bf5ae5c184e09f16b028`. Fonts are bundled through Fontsource. Laptop and coffee models come from the supplied Zemi repository. No agency code or agency project media is included.

Yorusa's live endpoint returned HTTP 521 and its repository was unavailable through the connected account. Its project, description, and live destination remain in the exhibition, with a typographic presentation. No fabricated Yorusa screenshot is included. Calendar and Voxpop each contain one live capture with explicitly labeled crops and animated screen studies. BiznetGIO and infrastructure videos are labeled screenshot/diagram studies. The two MGM clips are distinct excerpts of its original laboratory film.

This version passed compilation, catalog/search/routing/media checks, and static-route verification. Interactive browser QA was unavailable in this workspace. Visual parity with MGM and interaction behavior across real devices still require a browser review.
