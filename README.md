CSS Slider Menu
===============
*A CSS-only layout that emulates the new popular "slide" menu on many web and native mobile apps.*

---------------------------------------------------------------------------

**Original Author**: [@NicholasRBowers](http://twitter.com/NicholasRBowers)

---------------------------------------------------------------------------

Objective
---------
To create a CSS-only layout including a scrollable menu that slides out from the left. Meant for use in conjunction with responsive design as the **mobile versions of sites**.

Live Demo
---------
[Embedded JSFiddle Result](http://jsfiddle.net/NicholasRBowers/PPZ8b/embedded/result/)
[JSFiddle Code](http://jsfiddle.net/NicholasRBowers/PPZ8b/)

Operation Logic
---------------
* Uses the [checkbox-hack](http://css-tricks.com/the-checkbox-hack/) to store state information.
    * When unchecked, the menu is closed; when checked, the menu is open.
* Only two sibling elements exist in the base level of the `<body>` tag:  the input checkbox and a `<div>` tag afterwards that encapsulates the whole page.
* The `<div id="page">` tag holds the page, including the fixed header and contents.
* Header and Navigation toggle are fixed at top, while a scrollable `<div>` is below, and a fixed/scrollable navigation menu is to the left.
* An extra invisible label allows a click anywhere on the right to toggle states and collapse the menu.
* When the checkbox is `:checked`, the adjacent sibling combinator (`+`) is used to access the `#page` element and drill down through the HTML to drive the styling.  The sibling combinator (`~`) was originally favored over the adjacent sibling combinator so the whole page wouldn't need to be wrapped in a `<div>`, but most mobile browsers only select the adjacent sibling.

Additional Information
----------------------
* CSS-only
* Meant for mobile devices
* Meant to be used in conjunction with Responsive Design
* Akin to Facebook's Mobile and App layout
* Completely breaks in IE
* **Collaboration welcome!**

Comments
--------
* Completely broken in IE, but as this is meant for mobile only, I'm not sure that's a problem.
* Zooming out on a mobile device sometimes causes rendering problems.