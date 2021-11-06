# Fontsource Sass Integration Proposal

> An attempt to provide a modern Sass integration for Fontsource.

- Website [fontsource.org](https://fontsource.org/)
- GitHub [fontsource/fontsource](https://github.com/fontsource/fontsource)
- Discussion [Proposal for a modern Sass integration via Sass Modules](https://github.com/fontsource/fontsource/discussions/384)

## Goal

- Usage of `fontsource` font files in `Sass`-based projects.
- Support for `Sass Modules` with a hassle-free usage.
- Support for classic/static font-files and variable/dynamic font-files.

## Features

- [x] metadata for each font
- [x] utility functions to generate (property) values
- [x] mixin to generate font-face declaration blocks
- [ ] mixin to generate font-related declarations (needed?)

## Setup

```
git clone https://github.com/thasmo/fontsource-sass-integration.git
cd fontsource-sass-integration
npm install
npm run build
```

## Files

Every font features two `scss` files.

**metadata.scss**

Located at `source/fonts/<font-identifieer>/metadata.scss`
the file provides general font metadata for usage via Sass.

- `$name` — Name of the font family.
- `$identifier` — Short and machine-friendly identifier of the font family.
- `$category` — The type of font family. (`serif`, `sans-serif`, `display`, `handwriting`, `monospace`)
- `$styles` — Available font styles. (`normal`, `italic`)
- `$widths` — Available font widths. (`normal`)
- `$weights` — Available font weights. (`100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`)
- `$formats` — Available font file formats. (`woff2`, `woff`)
- `$directory` — File system path storing the font files.
- `$defaults` — Default values for various font properties. (`style`, `width`, `weight`, `subset`)
- `$subsets` — Available subsets and their glyphs.
- `$axes` — Available variable font axes and their metrics.

**utilities.scss**

Located at `source/fonts/<font-identifieer>/utilities.scss` the file
provides functions and mixins for generating font-related styles.

The `faces` mixin is the primary API used to generate `font-face` blocks for your project.

- mixin `faces` — Generate (multiple) `font-face` blocks for the given arguments.
- function `face-style` — Determine a `font-style` value for the given arguments.
- function `face-weight` — Determine a `font-weight` value for the given arguments.
- function `face-width` — Determine a `font-stretch` value for the given arguments.
- function `face-variation` — Determine a `font-variation-settings` value for the given arguments.
- function `face-glyphs` — Determine a `unicode-range` value for the given arguments.
- function `face-source` — Determine a `src` value for the given arguments.
- function `path` — Get a font file path for the given arguments.

## Research

**Articles**
- https://web.dev/variable-fonts/
- https://css-tricks.com/newsletter/259-how-to-use-variable-fonts/
- https://css-tricks.com/getting-the-most-out-of-variable-fonts-on-google-fonts/
- https://pimpmytype.com/variable-font-fallback/
- https://webplatform.news/issues/2019-07-31
- https://developer.mozilla.org/en-US/docs/Web/CSS/font-synthesis

**Tools**
- https://v-fonts.com/
