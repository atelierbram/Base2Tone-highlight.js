# Base2Tone Highlight.js
Generate syntax-highlighting schemes for Highlight.js with color variations from 2 colors with [Base2Tone](http://github.com/atelierbram/Base2Tone).

Highlight.js is one of the applications containing the colorschemes of [Base2Tone](http://base2t.one) which are based on [Duotone Themes](http://simurai.com/projects/2016/01/01/duotone-themes/) by [Simurai](http://simurai.com/) for Atom.

> “DuoTone themes use only 2 hues (7 shades in total). It tones down less important parts (like punctuation and brackets) and highlights only the important ones. This leads to a more calm color scheme, but still lets you find the stuff you're looking for.”

### Demo
Go see [the Demo for Highlight.js](http://atelierbram.github.io/Base2Tone-highlight.js/).

### Dependencies
 Some customized commands from the latest fork of Base16 Builder can be found here in an executable bash script (`io.sh`). Read more on this versatile and flexible <abbr title="Command Line Interface">CLI</abbr> building tool [on the Github repo for Base16 Builder](https://github.com/base16-builder/base16-builder), and the many ways to use it from the command-line.

Base16 Builder is available on NPM<sup>1</sup>, you can install it on your machine like so from the commandline:

```
$ npm install --global base16-builder
```

Typing `io.sh` and hitting enter from the command line in the root folder, will output the gererated Highlight.js code-highlighting files in the `docs assets/css/styles` folder. They all come in a dark and light variation, though most were originally conceived as dark background themes.

```bash
base16-builder --scheme "db/schemes/base2tone-morning.yml" --template "db/templates/highlight.js/light.ejs" > "docs/assets/css/styles/base2tone-morning-light.css"
```

### Create your own colorscheme.
This is the hard part; although the idea is to make color-schemes from just two color-hues, there is no easy way (_at least not on this repository_) to generate colorschemes from these two color-hues, (_because I don’t believe in an automated process that takes account of the peculiarities of the human eye, in connection to the perception of color_). It will always be a manual iterative process. My process is editing the demo-tile colors, you can see those demo-tiles on top of the pages [over here](http://atelierbram.github.io/Base2Tone-prism/demo/evening/dark/). So what I do is edit the `sass` file for those demo-tiles (_I use `HSL` and then convert those values from the browser, or a tool like [HSL Color Picker](http://hslpicker.com/) to `HEX` values_), and then manually copy and paste the new color-values over into a new `schemes/my-new-colorscheme.yml`. After that generate the `prism-my-new-colorscheme.scss` and see how the syntax-highlighting turns out on that demo-page. There are 32 color-value variables to be defined, so it will require a dedicated effort to build your own Base2Tone colorscheme. But if you do succeed in this, you will have the blueprint for generating colorthemes for these applications (_see above , and for many more applications in the future_).

The schemes and templates used can be found in the `db` folder. Copy and edit one of them `schemes/colorschemes.yml` from 32 color-value variables, and build your own DuoTones Highlight.js theme.

Alternatively, to make this process a bit more easy going and straight forward, one can fork [this demo of Base2Tone-prism on Codepen](http://codepen.io/atelierbram/pen/WrjVyv/).

In essence; one doesn't generate `yml` colorschemes, these are created, color-values manually copied over from a, for example, forked and adapted version of that demo on Codepen. (Tip: use the Developer Tools in your Browser to copy the HEX-color-values output from the rendered `css`). Base16-Builder’s commands are used for generating theme files for ... _anything really_, as long as you can make a template for this application.

### Conversions
The light version of the Morning theme, and dark versions of Evening, Sea, Space, Earth and Forest were converted from [DuoTone Themes for Atom](http://simurai.com/projects/2016/01/01/duotone-themes) by [Simurai](http//simurai.com). Morning and Evening are the default Duotone Light and Duotone Dark schemes, but renamed here in order to have a consistent naming convention.

### Credits
- [Simurai](http//simurai.com) for creating [DuoTone Themes](http://simurai.com/projects/2016/01/01/duotone-themes): I am merely recreating/converting these themes for other applications, while also making some variations of my own.
- [Chis Kempson](http://github.com/chriskempson) for creating [Base16 Builder](http://http://github.com/chriskempson/base16-builder)
- [Alois](https://github.com/aloisdg) and [Alex Booker](https://github.com/bookercodes) for rejuvenating the best colorscheme builder tool on the internet: [Base16 Builder](https://github.com/base16-builder/base16-builder)

### License
Copyright (c) 2016 [Bram de Haan](http://atelierbramdehaan.nl/)

Released under [MIT Licence](http://atelierbram.mit-license.org)

1. Installing from NPM means you will also need to have Node.js installed; instructions can be found [here](https://docs.npmjs.com/getting-started/installing-node).
