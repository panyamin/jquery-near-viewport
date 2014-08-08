# near-viewport [![Build Status](https://travis-ci.org/cobbdb/jquery-near-viewport.svg?branch=master)](https://travis-ci.org/cobbdb/jquery-near-viewport) [![Bower version](https://badge.fury.io/bo/jquery-near-viewport.svg)](http://badge.fury.io/bo/jquery-near-viewport)

A jQuery selector to find elements near the viewport.

    $ bower install jquery-near-viewport

[![Saucelabs Test Status](https://saucelabs.com/browser-matrix/query-near-viewport.svg)](https://saucelabs.com/u/query-near-viewport)

-------------
### Selecting visible elements
By default the selector will match elements that are at least partially showing in the viewport.

    var visibleImages = $('img:near-viewport');

### Testing if an element is visible
The selector can be used with .is() to test if an element is or is not in range of the viewport.

    var trackingPixel = $('#lower-tp');
    if (trackingPixel.is(':near-viewport')) {
        trackingPixel.recordMetrics();
    }

### Using the offset option
An offset can be set which will increase the range beyond the viewport both top and bottom.
For example, if given an offset of 100, then items will match 100px above the viewport and 100px below the viewport.

    $('.ad:near-viewport(100)').loadFromServer();

### No jQuery, no problem
Provided is also a global version that can be used in any project. Just use
`dist/near-viewport.js` instead of the jQuery plugin.

    var el = document.getElementById('mydiv');
    var visible = nearViewport(el);
    var nearby = nearViewport(el, 100);

---------
* See: http://plugins.jquery.com/near-viewport/
* See: http://github.com/cobbdb/jquery-near-viewport
* License: MIT

---------
### Change Log
#### 1.0.0
* Offset option to match above and below the viewport.