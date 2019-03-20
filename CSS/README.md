# SYZYGY PL - CSS Styleguide

* [CSS](#css)
* [Sass](#sass)
* [BEM](#bem)

---

### CSS
* Always style by class name (_never `id` or tag name selectors_). 
* Order your declarations as proposed in [Idiomatic CSS](https://github.com/necolas/idiomatic-css#declaration-order).
* Make sure that your preferable solution meets desirable Browsers Support.

**Exceptions**
* `content` declaration should be on the first place in Declaration Order.


### Sass
* Always use `.scss` syntax.
* Use all the benefits - variables, nesting, mixins, build-in and custom functions,
  placeholders, etc. - to make code smarter, simpler, clearer and easier to maintain.
* Prefer `hex` or other color model over named colors (_`#ff0000` rather than `red`_).


### BEM
* Use BEM in it's most popular [Two Dashes style](https://en.bem.info/methodology/naming-convention/#two-dashes-style).
* 1 block per 1 file with corresponding name (_e.g. `.card` block in `_card.scss` file_).
* Declare block name only once at top of the file. Use `$root` / [`$this` variable](https://www.devbridge.com/articles/7-sass-techniques-to-help-you-write-better-code/)
  to reuse it.
* Media Queries should be placed at the end, once for each block rather than
  independently for block elements.
 
**Exceptions**
* Using CSS resets / normalizers is allowed ([yes, it's against BEM](https://en.bem.info/methodology/faq/#why-shouldnt-i-use-a-css-reset))
* We use [No Naming style](https://en.bem.info/methodology/naming-convention/#no-namespace-style)
  syntax for "state modifiers" - (`.-is-*` and `.-has-*`).
* Styling `img` and `svg` by tag name is allowed. [Why?](FAQ.md#styling-img-and-svg-by-tag-name) 
* In some cases (_like using external component with imposed markup_) it may be
  unavoidable to break BEM naming convention rules.


---


## [Solved problems](FAQ.md)


## Resources

### CSS
* [CSS Specifications](https://www.w3.org/Style/CSS/specs.en.html)
* [Idiomatic CSS](https://github.com/necolas/idiomatic-css) by Nicolas Gallagher

### Sass
* [Sass documentation](https://sass-lang.com/)
* ["7 Sass techniques to help you write better code"](https://www.devbridge.com/articles/7-sass-techniques-to-help-you-write-better-code/)
  by Andrius Juskenas

### BEM
* [BEM Methodology](https://en.bem.info/methodology/)
 

### Files organization
* [BEM - File structure organization](https://en.bem.info/methodology/filestructure/)
