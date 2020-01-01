# Eleventail

A project scaffold for quickly starting a site build with:

- [Eleventy](https://11ty.dev) for templates and site generation
- [Tailwindcss](https://tailwindcss.com) for a utility first CSS workflow
- [PurgeCSS](https://www.purgecss.com/) for optimizing css output
- [UglifyJS](https://www.npmjs.com/package/uglify-js) for a simple JS build pipeline
- [Netlify CLI](https://www.npmjs.com/package/netlify-cli) for Netlify dev pipeline and local replication of prod environment


## Prerequisites

- [Node and NPM](https://nodejs.org/)
- [Netlify CLI](https://www.npmjs.com/package/netlify-cli)


## Running locally

```bash

# install Netlify CLI globally
npm install netlify-cli -g

# install the project dependencies
npm install

# run the build and server locally
netlify dev
```


## Previewing the production build

When building for production, an extra build step will strip out all CSS classes not used in the site. This step is not performed during the automatic rebuilds which take place during dev.

```bash

# run the production build
npm run build
```


## Styling with TailwindCSS

This site uses TailwindCSS to offer utility CSS classes and provide a rapid means to styling the site. This means that most styling can be done without writing any additional CSS. Instead, utility classes can be added directly to the HTML. This may not be to everyone's tastes, but it can provide some very rapid development and also offer surprising levels of familiarity for those used to working in this way (since the conventions and classes are not _per site_.)

While running/developing locally, thw `npm run start` command will recompile the site as files are saved and this includes the CSS pipeline from Tailwind.

### Global CSS utilities.

A small number of bespoke CSS rules are provided for efficiency of repeated or global classes. These reside in `src/css/tailwind.css`
