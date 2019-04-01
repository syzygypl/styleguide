## Good class names
> Think about why you want something to look a certain way, and not really about how it
> should look. **Looks can always change, but the reasons for giving something a look stay
> the same.**

– [W3C Quality Assurance](https://www.w3.org/QA/Tips/goodclassnames) - from 2004 but still up-to-date.

Class names should be named is semantic way to make code more readable - represent the purpose
of an element, not it's visual appearance.
You never know if the layout you are working on currently will not change it's visual appearance
one day. That's why `.button--primary` will always be a better name than `.button--red` so you
don't have to refactor all your markup after all. Believe me or not but it happens!

**Further read:**
- ["Use class with semantics in mind."](https://www.w3.org/QA/Tips/goodclassnames) - W3C Quality Assurance
- [MaintanableCSS - "Semantics"](https://maintainablecss.com/chapters/semantics/) by Adam Silver

**Real code issues:**
- [We had to rename button modifiers (non-semantic) in tens of templates due to brand colors change](https://github.com/syzygypl/nutricia-platform/pull/519/files)
