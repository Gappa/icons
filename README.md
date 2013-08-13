Icons
=====

The goal of this "project" is to eliminate meaningless and empty tags used to insert icons (yes, I'm looking at you Bootstrap).

Description:
* uses data-attributes to insert the icon, eg. `<a href="http://www.example.com/article/edit/1/" data-icon-b="pen">Edit</a>`
* uses ::before and ::after pseudo-elements to insert the icon at the appropriate place

Pros:
* no additional markup for icons
* can be attached to almost any tag (see cons)
* each icon can be (re)used in any position - standalone, before, after or combination of before, after and the tags content
* can be used with CSS sprites
* can be used with base64 encoded icons

Cons:
* is defined as a data-attribute, so it takes some space in the code
* can interfere with other styles that are using before/after (like clearfix)
* non-pair tags (elements with no innerHTML) cannot use this approach, so no inputs and images

Supports:
* Internet Explorer 8+
* Chrome
* Firefox
* Opera (Presto|Blink)
* more info: http://caniuse.com/#feat=css-gencontent

Notes:
* Uses the 2.1 CSS single-colon syntax in order to support IE8, using the CSS3 double-colon syntax would render it incompatible.
