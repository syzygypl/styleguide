# Solved problems

* [Good class names](#good-class-names)
* [Magic numbers](#magic-numbers)
* [Content dependent styles](#content-dependent-styles)
* [Styling `img` and `svg` by tag name](#styling-img-and-svg-by-tag-name)

**Note:**
If you are from outside our organization [Syzygy Warsaw](https://github.com/syzygypl) -
**Real code issues** will probably not work for you as most of them refers to code
in our private repositories.

---

## Good class names
> Think about why you want something to look a certain way, and not really about how it
> should look. **Looks can always change, but the reasons for giving something a look stay
> the same.**

– [W3C Quality Assurance](https://www.w3.org/QA/Tips/goodclassnames) - from 2004 but still up-to-date.

Class names should be named is semantic way to make code more readable - represent the purpose
of an element, not it's visual appearance.
You never know if the layout you are working on currently will not change it's color palette
one day. That's why `.button--primary` will always be a better name than `.button--red` so you
don't have to refactor all your markup after all. Believe me or not but it happens!

**Further read:**
- ["Use class with semantics in mind."](https://www.w3.org/QA/Tips/goodclassnames) - W3C Quality Assurance
- [MaintanableCSS - "Semantics"](https://maintainablecss.com/chapters/semantics/) by Adam Silver

**Real code issues:**
- [We had to rename button modifiers (non-semantic) in tens of templates due to brand colors change](https://github.com/syzygypl/nutricia-platform/pull/519/files)


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


### Content dependent styles

Or "CSS overuse". If the code is bound to specific assets - texts, images, etc. - it means that every
content change requires some work of a programmer. It also may make CSS harder to maintain
if there are many unnecessary modifiers in the code just to position specific images properly.
**Assets should be prepared to fit the layout, not vice versa.**

**Real code issues:**
- [Example of modifier used to position badly prepared image](https://github.com/syzygypl/nutricia-platform/commit/ae401f7a741a5fc367889af911b07f3eb9f7c61f#diff-7e086921787caf16870fd55ae3caa3a9L191)


## Styling `img` and `svg` by tag name

In some cases there is no reasonable solution to add a class name to those elements.
An example **might be** `svg` included directly in TWIG template or `img` received
directly from WYSIWYG.

_**However** - if adding a class name to those elements does not sound like an
overengineering we should always style by a class name._   
