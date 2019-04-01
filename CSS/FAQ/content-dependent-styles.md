## Content dependent styles

Or "CSS overuse". If the code is bound to specific assets - texts, images, etc. - it means that every
content change requires some work of a programmer. It also may make CSS harder to maintain
if there are many unnecessary modifiers in the code just to position specific images properly.
**Assets should be prepared to fit the layout, not vice versa.**

**Real code issues:**
- [Example of modifier used to position badly prepared image](https://github.com/syzygypl/nutricia-platform/commit/ae401f7a741a5fc367889af911b07f3eb9f7c61f#diff-7e086921787caf16870fd55ae3caa3a9L191)
