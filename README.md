# Fontsource Sass Integration Proposal

> An attempt to provide a modern Sass integration for Fontsource.

* Website [fontsource.org](https://fontsource.org/)
* GitHub [fontsource/fontsource](https://github.com/fontsource/fontsource)
* Discussion [Proposal for a modern Sass integration via Sass Modules](https://github.com/fontsource/fontsource/discussions/384)

## Goal

* Usage of `fontsource` font files in `Sass`-based projects.
* Support for `Sass Modules` with a hassle-free usage.
* Support for classic/static font-files and variable/dynamic font-files.

## Features

* [x] metadata for each font
* [x] mixin to generate font-face declarations
* [ ] mixin to generate font-related declarations (needed?)
* [ ] utility functions to generate (property) values (needed?)

## Setup
```
git clone https://github.com/thasmo/fontsource-sass-integration.git
cd fontsource-sass-integration
npm install
npm run build
```

## Research

**Articles**
* https://web.dev/variable-fonts/
* https://css-tricks.com/newsletter/259-how-to-use-variable-fonts/
* https://css-tricks.com/getting-the-most-out-of-variable-fonts-on-google-fonts/
* https://pimpmytype.com/variable-font-fallback/
* https://webplatform.news/issues/2019-07-31
* https://developer.mozilla.org/en-US/docs/Web/CSS/font-synthesis

**Tools**
* https://v-fonts.com/
