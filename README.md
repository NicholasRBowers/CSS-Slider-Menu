CSS Menu Slider
===============
*A CSS-only layout that emulates the new popular "slide" menu on many web and native mobile apps.*

---------------------------------------------------------------------------

**Original Author**: [@NicholasRBowers](http://twitter.com/NicholasRBowers)

---------------------------------------------------------------------------

Objective
---------
To create a CSS-only layout including a scrollable menu that slides out from the left. Meant for mobile versions of sites.

Live Demo
---------
[Embedded JSFiddle Result](http://jsfiddle.net/NicholasRBowers/PPZ8b/embedded/result/)
[JSFiddle Code](http://jsfiddle.net/NicholasRBowers/PPZ8b/)

Operation Logic
---------------
* Uses the [checkbox-hack](http://css-tricks.com/the-checkbox-hack/) to store state information
    * When unchecked, menu is closed, when checked menu is open.
* Input checkbox exists at the base level of the HTML (under `<body>`) with an absolutely positioned `<div>` tag afterwards that encapsulates the page.
* `<div>` tag holds the rest of the page, including fixed absolutely positioned elements.
* Header and Navigation toggle are fixed at top, scrollable `<div>` under, and fixed/scrollable menu to the left.
* An extra invisible label allows a click anywhere on the right to toggle states and collapse the menu.

Additional Information
----------------------
* CSS-only
* Meant for mobile devices
* Meant to be used in conjunction with Responsive Design
* Want to design as semantic as possible
* Akin to Facebook's Mobile and App layout
* Completely breaks in IE
* **Collaboration welcome!**

Comments
--------
* Completely broken in IE, but as this is meant for mobile only, I'm not sure that's a problem.
* Zooming out on a mobile device sometimes causes rendering problems.
* Had to put the rest of the page in a `<div>` that was a sibling to the `<input>` element, because the default Android browser only supports the adjacent sibling combinator (`+`) when used in tandem with a pseudo-class (`:checked`). **NOTE**: It does support the sibling combinator (`~`), but it only picks up the **adjacent** element.