# SYZYGY PL - Accessibility Styleguide

## HTML

* Always declare language attribute -- globally on your `html` wrapper and locally on elements containing text in other languages.
* Use HTML5 sectioning elements such as `header`, `main`, `footer` `aside`, `section` to create a comprehensive landmark structure of the website or application. Also, remember about headings hierarchy (`h1` - `h6`).
* Use semantic HTML5 elements to create components, i.e. if component requires user interaction, mark it as `a` or `button` ([more on this topic](https://marcysutton.com/links-vs-buttons-in-modern-web-applications)).
* Remember that all the `img` elements require `alt` attribute (in case of images that are purely decorative and do not have any semantic meaning leave the `alt` attribute empty). 
* If you do not provide text content in your links (for example you use image or icon as a link), add descriptive `aria-label` attribute to your `a` element. Helpful resource: [An alt Decision Tree](https://www.w3.org/WAI/tutorials/images/decision-tree/).
* Use ARIA attributes with understanding, remembering that [no ARIA is better than bad ARIA](https://www.w3.org/TR/wai-aria-practices/#no_aria_better_bad_aria).

## CSS

* Do not add `outline: none` on focusable elements if you do not provide alternative styling for `:focus`. Consider using `:focus-visible` [polyfill](https://github.com/WICG/focus-visible) to add extra styling for those navigating with keyboard.

## Testing 

* Test color contrast and for different types of color blindness. If some parts of application's UI do not have sufficient color contrast or are uncomprehensive for people who do not read colors, do not hesitate to discuss it with the designer you collaborate with.
* Test navigation using keyboard only.
* Test semantics with images and CSS turned off.

***
### Further reading:
* [List of Web Accessibilty Resources by Marcy Sutton](https://marcysutton.com/web-accessibility-resources)
* [Seven easy-to-implement guidelines to design a more accessible web](https://uxdesign.cc/designing-for-accessibility-is-not-that-hard-c04cc4779d94)
* [The 6 Simplest Web Accessibility Tests Anyone Can Do](http://www.karlgroves.com/2013/09/05/the-6-simplest-web-accessibility-tests-anyone-can-do/)
* [Inclusive Components](https://inclusive-components.design/)
* [HTML is the Web](https://www.petelambert.com/journal/html-is-the-web/)
* [What a Year of Learning and Teaching Accessibility Taught Me](https://www.sarasoueidan.com/blog/what-accessibility-taught-me/)

### Tools for everyday use:
* [AXE Chrome Plugin](https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd)
* [Checklist / VOX Media](http://accessibility.voxmedia.com/)
* [Colour Contrast Analyser for Mac](https://developer.paciellogroup.com/resources/contrastanalyser/)
