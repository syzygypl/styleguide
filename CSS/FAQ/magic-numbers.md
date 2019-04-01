## Magic numbers

AKA "unnamed numerical constants" make code less readable - it's hard to deduce what
is the value related to. It also complicates the maintenance as change of magic number
value may cause need to change other related magic numbers which is not clearly visible in
the code.

If there is a need of using numerical constant in the code it **always** should be assigned
to some `$variable` (Sass) or `--custom-property` (CSS) with descriptive name -
e.g. `$bar-height: 50px;`.

One numerical constant should be defined only once. Even if there are some magic numbers
that need to be used in both - CSS (Sass) and JS. To achieve that
[`node-sass-json-importer`](https://github.com/Updater/node-sass-json-importer) may be useful,
so one common config (e.g. `@media` queries breakpoints) can be stored in JSON and imported
in our CSS (_Sass_) and JS (_ES6_) files.

**Further read:**
- ["Magic Numbers in CSS"](https://css-tricks.com/magic-numbers-in-css/) by Chris Coyier

**Real code issues:**
- [Discussion about `$gutter` / `$spacing` variable](https://github.com/syzygypl/danwood/pull/32/#discussion_r237577498)
- [Some magic numbers in production code](https://github.com/syzygypl/nutricia-platform/search?q=%22magic+number%22&type=Code)
