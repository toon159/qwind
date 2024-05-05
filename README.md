# 💠 Qwind

**Qwind** is a free and open-source template to make your website using **[Qwik](https://qwik.builder.io/) + [Tailwind CSS](https://tailwindcss.com/)**. Ready to start a new project and designed taking into account best practices.

## Features

- ✅ Integration with **Tailwind CSS** supporting **Dark mode**.
- ✅ **Production-ready** scores in [Lighthouse](https://web.dev/measure/) and [PageSpeed Insights](https://pagespeed.web.dev/) reports.
- ✅ **Image optimization** and **Font optimization**.

<br>

<img src="./screenshot.jpg" alt="Qwind Theme Screenshot">

[![onWidget](https://custom-icon-badges.demolab.com/badge/made%20by%20-onWidget-556bf2?style=flat-square&logo=onwidget&logoColor=white&labelColor=101827)](https://onwidget.com)
[![License](https://img.shields.io/github/license/onwidget/qwind?style=flat-square&color=dddddd&labelColor=000000)](https://github.com/onwidget/qwind/blob/main/LICENSE.md)
[![Maintained](https://img.shields.io/badge/maintained%3F-yes-brightgreen.svg?style=flat-square)](https://github.com/onwidget)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/onwidget/qwind#contributing)
[![Known Vulnerabilities](https://snyk.io/test/github/onwidget/qwind/badge.svg?style=flat-square)](https://snyk.io/test/github/onwidget/qwind)

<br>

<details open>
<summary>Table of Contents</summary>

- [Demo](#demo)
- [Getting started](#getting-started)
  - [Project structure](#project-structure)
  - [Commands](#commands)
  - [Configuration](#configuration)
  - [Deploy](#deploy)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [License](#license)

</details>

<br>

## Demo

📌 [https://qwind.pages.dev/](https://qwind.pages.dev/)

<br>

## Getting started

This project is using Qwik with [QwikCity](https://qwik.builder.io/qwikcity/overview/). QwikCity is just a extra set of tools on top of Qwik to make it easier to build a full site, including directory-based routing, layouts, and more.

### Project structure

Inside **Qwind** template, you'll see the following folders and files:

```
/
├── adaptors/
|   └── static/
|       └── vite.config.ts
├── public/
│   ├── favicon.svg
│   ├── manifest.json
│   └── robots.txt
├── src/
│   ├── assets/
│   │   ├── images/
|   |   └── styles/
|   |       └── global.css
│   ├── components/
│   │   ├── atoms/
│   │   ├── core/
│   │   ├── icons/
|   |   └── widgets/
|   |       ├── Hero.tsx
|   |       ├── Features.tsx
|   |       └── ...
│   ├── content/
│   |   └── blog/
│   |       ├── post-slug-1.md
│   |       ├── post-slug-2.md
│   |       └── ...
│   ├── routes/
│   |   ├── blog/
│   |   ├── index.tsx
|   |   ├── layout.tsx
|   |   ├-- service-worker.ts
│   |   └-- ...
│   ├── config.mjs
│   ├── entry.dev.tsx
│   ├── entry.preview.tsx
│   ├── entry.ssr.tsx
│   └── root.tsx
├── package.json
└── ...
```

- `src/routes`: Provides the directory based routing, which can include a hierarchy of `layout.tsx` layout files, and an `index.tsx` file as the page. Additionally, `index.ts` files are endpoints. Please see the [routing docs](https://qwik.builder.io/qwikcity/routing/overview/) for more info.

- `src/components`: Recommended directory for components.

- `public`: Any static assets, like images, can be placed in the public directory. Please see the [Vite public directory](https://vitejs.dev/guide/assets.html#the-public-directory) for more info.

[![Edit Qwind on CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://githubbox.com/onwidget/qwind/tree/main)

> **Seasoned qwik expert?** Delete this file. Update `config.mjs` and contents. Have fun!

<br>

### Commands

All commands are run from the root of the project, from a terminal:

| Command            | Action                                         |
| :----------------- | :--------------------------------------------- |
| `npm install`      | Installs dependencies                          |
| `npm run dev`      | Starts local dev server at `127.0.0.1:5173/`   |
| `npm run build`    | Build your production site to `./dist/`        |
| `npm run preview`  | Preview your build locally, before deploying   |
| `npm run fmt`      | Format codes with Prettier                     |
| `npm run lint`     | Run Eslint                                     |
| `npm run qwik ...` | Run CLI commands like `qwik add`, `qwik build` |

<br>

### Configuration

Basic configuration file: `./src/config.mjs`

```javascript
export const SITE = {
  name: "Example",

  origin: "https://example.com",
  basePathname: "/", // Change this if you need to deploy to Github Pages, for example
  trailingSlash: true, // Generate permalinks with or without "/" at the end
};
```

<br>

### Deploy

#### Deploy to production (manual)

You can create an optimized production build with:

```shell
npm run build
```

Now, your website is ready to be deployed. All generated files are located at
`dist` folder, which you can deploy the folder to any hosting service you
prefer.

#### Deploy to Netlify

Clone this repository on own GitHub account and deploy to Netlify:

[![Netlify Deploy button](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/onwidget/qwind)

#### Deploy to Vercel

Clone this repository on own GitHub account and deploy to Vercel:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fonwidget%2Fqwind)

<br>

## Roadmap

### Base

- [ ] Create utilities to generate permalinks tailored to the domain and base pathname.
- [ ] Simplify the way to optimize images.
- [ ] Create component to make SEO simpler and more intuitive.
- [ ] Create configurable blog with categories, tags and authors using MDX.
- [ ] Add more frequently used pages (Portfolio, Services, Contact, Docs ...).
- [ ] Find or create a library to have more icon sources available.
- [ ] Refactor some code that doesn't follow Qwik conventions yet.

### Advanced

- [ ] Achieve perfect 100% Google Page Speed score.
- [ ] Insert complex javascript example widget on home page to demonstrate Qwik features.
- [ ] Create small illustrative admin backend.

<br>

## Contributing

If you have any idea, suggestions or find any bugs, feel free to open a discussion, an issue or create a pull request.
That would be very useful for all of us and we would be happy to listen and take action.

## Acknowledgements

Initially created by [onWidget](https://onwidget.com) and maintained by a community of [contributors](https://github.com/onwidget/qwind/graphs/contributors).

## License

**Qwind** is licensed under the MIT license — see the [LICENSE](https://github.com/onwidget/qwind/blob/main/LICENSE.md) file for details.

## Cloudflare Pages

Cloudflare's [wrangler](https://github.com/cloudflare/wrangler) CLI can be used to preview a production build locally. To start a local server, run:

```
npm run serve
```

Then visit [http://localhost:8787/](http://localhost:8787/)

### Deployments

[Cloudflare Pages](https://pages.cloudflare.com/) are deployable through their [Git provider integrations](https://developers.cloudflare.com/pages/platform/git-integration/).

If you don't already have an account, then [create a Cloudflare account here](https://dash.cloudflare.com/sign-up/pages). Next go to your dashboard and follow the [Cloudflare Pages deployment guide](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/).

Within the projects "Settings" for "Build and deployments", the "Build command" should be `npm run build`, and the "Build output directory" should be set to `dist`.

### Function Invocation Routes

Cloudflare Page's [function-invocation-routes config](https://developers.cloudflare.com/pages/platform/functions/routing/#functions-invocation-routes) can be used to include, or exclude, certain paths to be used by the worker functions. Having a `_routes.json` file gives developers more granular control over when your Function is invoked.
This is useful to determine if a page response should be Server-Side Rendered (SSR) or if the response should use a static-site generated (SSG) `index.html` file.

By default, the Cloudflare pages adaptor _does not_ include a `public/_routes.json` config, but rather it is auto-generated from the build by the Cloudflare adaptor. An example of an auto-generate `dist/_routes.json` would be:

```
{
  "include": [
    "/*"
  ],
  "exclude": [
    "/_headers",
    "/_redirects",
    "/build/*",
    "/favicon.ico",
    "/manifest.json",
    "/service-worker.js",
    "/about"
  ],
  "version": 1
}
```

In the above example, it's saying _all_ pages should be SSR'd. However, the root static files such as `/favicon.ico` and any static assets in `/build/*` should be excluded from the Functions, and instead treated as a static file.

In most cases the generated `dist/_routes.json` file is ideal. However, if you need more granular control over each path, you can instead provide you're own `public/_routes.json` file. When the project provides its own `public/_routes.json` file, then the Cloudflare adaptor will not auto-generate the routes config and instead use the committed one within the `public` directory.
