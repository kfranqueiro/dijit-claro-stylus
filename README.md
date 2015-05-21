# Dijit Claro Stylus Conversion

This repository contains a straight port of Dijit's Claro theme (as of Dojo
version 1.7.8) from [Less](http://lesscss.org/) to [Stylus](http://learnboost.github.com/stylus/).

## Usage

Make sure Stylus is installed...

```
npm install -g stylus
```

...then inside the top level of this repository, run:

```
stylus . form layout
```

## Notes

This was quickly tested using `dijit/themes/themeTester.html`, and results of
the CSS compilation were verified via diff against the OOTB CSS exported from
LESS.  The majority of differences were blank lines, line breaks between multiple
selectors, and a few off-by-one differences from BIFs such as `saturate`,
`lighten`, and `darken`.

The only noticeable difference was in the result of 2 calculations for disabled
textbox/textarea styles for WebKit in `form/Common.css`, which have been
tweaked to be more in line with their appearance in other browsers.

## License

The contents of this repository are available under the same dual
modified BSD / AFL 2.1 license as the Dojo Toolkit.
