# SYZYGY PL - SEO Styleguide

## Rules
* [Content is the king](https://www.semrush.com/blog/why-content-is-king-is-the-biggest-myth-in-seo/)!
* Make sure that Headings Structure is correct:
  * there **must be** one and only `h1` tag on each page,
  * check [heading-level outline][validator] to verify headings hierarchy.
* Take care of Document Structure and Semantics.
  * check [structural outline][validator] to verify document structure.
* Remember that good [Accessibility][accessibility] translates into better SEO.
* Optimise website's performance - *loading time is important factor in SEO*:
  * minify JS, CSS and HTML,
  * optimise images,
  * [and much more...](https://developers.google.com/web/tools/lighthouse/audits/critical-request-chains)

***

### Further reading:

* Our [Accessibility Styleguide][accessibility]
* [The HTML5 Semantic Elements and What They Mean For SEO](https://www.inboundnow.com/html5-semantic-elements-mean-seo/) by Roy Dopaishi
* [What You Should Know About Accessibility + SEO](https://moz.com/blog/accessibility-seo-1) by Laura Lippay
* [Does site speed influence SEO?](https://yoast.com/does-site-speed-influence-seo/) by Edwin Toonen 


### Tools for everyday use:
* [Google Webmaster Tools](https://www.google.com/webmasters/tools/home)
* W3C's [Nu Html Checker][validator] for Validation and Document Outlines
* Google's [Lighthouse][lighthouse] for "improving the quality of web pages", includes SEO Audit
* Google's [Page Speed Insights][page-speed] for Performance Audit
* Google's [Rich Snippets Testing Tool](rich-snippets)



[accessibility]: ../a11y/README.md
[validator]: https://validator.w3.org/nu/?showoutline=yes
[lighthouse]: https://developers.google.com/web/tools/lighthouse/
[page-speed]: https://developers.google.com/speed/pagespeed/insights/
[rich-snippets]: https://developers.google.com/structured-data/testing-tool
