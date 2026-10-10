# Creations by Ren

A static exhibition of fourteen projects, in the supplied order. The home is a scroll-led story with animated 3D objects and project media. `/list` is a searchable archive. `/list/:slug` contains the project story, gallery, video studies, and one primary destination.

## Development

Use Node.js 22 or newer. Media validation uses FFmpeg.

```sh
npm ci
npm run dev
```

```sh
npm run check
npm test
npm run build
node scripts/verify-static.mjs
npm run preview
```

## GitHub Pages

Pushes to `main` run the included build and deployment workflow. GitHub Pages is configured to use GitHub Actions. Set the custom domain in **Settings → Pages** when ready. No deployment domain or CNAME is embedded in the source.

`BASE_PATH` defaults to `/`. The workflow obtains the path from GitHub Pages. To test a repository subdirectory:

```sh
BASE_PATH=/creations/ npm run build
BASE_PATH=/creations/ node scripts/verify-static.mjs
```

The build emits an HTML document for all sixteen routes, plus `404.html` and `.nojekyll`. Direct detail links therefore work without a server or rewrite rule. Each route has readable static content before JavaScript runs.

## Content and media

Edit `src/projects.json` for content, ranking, categories, technologies, media, and primary links. Bundled assets live in `public/media`. `asset-sources.json` records exact provenance and distinguishes screenshots, original recordings, original motion backgrounds, and animated source studies.

The collection includes 85 media entries, with at least five for every project and two video entries per project. Video posters are additional files. Original recordings are used for Zemi, Atlas, Anonchat, Asset Library, WAAWer Coaster, Tenki Weather, and Can Shooting. MGM videos are two excerpts of its laboratory film. Personal Portfolio videos show its original character animation. Yorusa videos are its original motion backgrounds. BiznetGIO and infrastructure videos are animated screenshot or diagram studies. Calendar uses one public capture with labeled crops and screen studies. Voxpop uses source geometry renders with simplified materials and animated studies; these are not gameplay captures. Its live capture remained at the loader and was excluded.

## Motion and accessibility

Keyboard navigation, a skip link, live search counts, manual video controls, light and dark themes, and reduced motion are supported. The header can pause decorative motion. Offscreen videos and decorative WebGL scenes stop running. The archive falls back to its original DOM presentation when WebGL is unavailable.

The home switches from sticky scroll chapters to a normal document layout on narrow screens. Landscape and reduced-motion layouts are included. Interactive browser QA was unavailable in this workspace, so visual parity with MGM and behavior across real devices still require browser review.

## Source provenance

The archive, library world, portals, detail transitions, and image interactions are adapted from the user-supplied `MGM-Laboratory/mgm-website` repository, revision `b962558e3ffbdeb356b2bf5ae5c184e09f16b028`. Fonts are bundled through Fontsource. Laptop and coffee models come from the supplied Zemi repository. Project screenshots and recordings come from the supplied repositories and MGM's published project media. No agency code or agency project media is included.

All commits are attributed to Shirasaka Ren. No credentials belong in the source, bundle, or deployment.
