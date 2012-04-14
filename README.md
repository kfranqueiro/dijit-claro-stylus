# Dijit Claro Stylus Conversion

This repository contains a straight port of Dijit's Claro theme (as of Dojo
version 1.7.2) from [LESS](http://lesscss.org/) to
[Stylus](http://learnboost.github.com/stylus/).

To generate the CSS resources, install Stylus (e.g. using NPM), then within
the directory this repository was cloned to, run...

    stylus . form layout

This was quickly tested using `dijit/themes/themeTester.html`, and results of
the CSS compilation were verified via diff against the OOTB CSS exported from
LESS.  The majority of differences were blank lines, line breaks between multiple
selectors, and a few off-by-one differences from BIFs such as `saturate`,
`lighten`, and `darken`.

The only noticeable difference was in the result of 2 calculations for disabled
textbox/textarea styles for WebKit in `form/Common.css`, which have been
tweaked to be more in line with their appearance in other browsers.