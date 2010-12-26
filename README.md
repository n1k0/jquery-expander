jQuery Expander plugin
======================

This [jQuery](http://jquery.com/) plugin adds links to expand and shorten (truncate) plain or html texts.

Installation
------------

In your HTML document:

    <script src="jquery.js" type="text/javascript"></script>
    <script src="jquery.expander.js" type="text/javascript"></script>

Sample use
----------

**HTML:**

    <p class="truncate-200">Lorem ipsum dolor sit amet, consectetur adipisicing
    elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
    enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
    aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
    voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
    occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit
    anim id est laborum.</p>

**Javascript:**

    $('p.truncate-200').expander({
       slicePoint: 200,
    });

**Result:**

    <p class="truncate-200">Lorem ipsum dolor sit amet, consectetur adipisicing
    elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
    enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
    ut… <a href="#" class="read-more">read more</a></p>


Available settings
------------------

* `slicePoint`: the number of characters at which the contents will be sliced
    into two parts. Any tag names in the HTML that appear inside the sliced 
    element before the slicePoint will be counted along with the text characters
    (default: `100`).
* `widow`: a threshold of sorts for whether to initially hide/collapse part of 
    the element's contents. If after slicing the contents in two there are 
    fewer words in the second part than the value set by widow, we won't bother 
    hiding/collapsing anything (default: `4`).
* `expandText`: text displayed in a link instead of the hidden part of the element. 
    Clicking this will expand/show the hidden/collapsed text (default: `read more`).
* `expandPrefix`: prefix to add before expanded text (default: `&hellip;`).
* `collapseTimer`: number of milliseconds after text has been expanded at which 
    to collapse the text again (default: `0`).
* `expandEffect`: expanding jquery effect name (default: `fadeIn`).
* `expandSpeed`: speed in milliseconds of the animation effect for expanding the text.
* `userCollapse`: allow the user to re-collapse the expanded text (default: `true`).
* `userCollapseText`: text to use for the link to re-collapse the text (default: `[collapse expanded text]`).
* `userCollapsePrefix`: prefix to add after collapsed content (default: `' '`).
* `cssReadLessClassName`: css class name to add to the read-less span (default: `re-collapse`).
* `cssReadMoreClassName`: css class name to add to the read-more span (default: `read-more`).
* `cssDetailsClassName`: css class name to add to the details span (default: `details`).
* `truncatedSuffix`: a suffix to add to truncated inner text (default: `...`).

Some callbacks are also available as settings:

* `beforeExpand`: called just before the text has been expanded.
* `afterExpand`: called just after the text has been expanded
* `onCollapse`:  called when text is collapsed.

Credits
-------

This plugin is a fork of the great [original Expander plugin](http://plugins.learningjquery.com/expander/), slightly adapted to my personal needs and with some added features and behaviors.
