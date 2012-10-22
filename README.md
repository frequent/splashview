splashview
----------

**Cross browser/decive splash screen for desktop/mobile applications**

Setting up an iOS splashscreen can be a real challenge both in terms
of number of images required, formatting and getting them to display
regularly in an HTML5 web-app. Plus you can only use them on iOS 
devices, which makes for half the fun only.

The idea of splashview came up when I was trying to troubleshoot 
unenhanced blinking content and ended up covering the page up with
a white canvas to be removed once my application was running.

This had to be done in Javascript / CSS, because usually plugins like
Jquery or Jquery Mobile will not have initilized by the time the splash
image should be displayed.

Therefore, it's javascript only. 

There is not much to set besides a class on the body (demo uses `.splash`).
A single CSS rule sets the "canvas" background-color, loading text and 
base dimensions. Once the page is being loaded the background-image 
is added via addRule/insertRule according to screen size and orientation. 

A set timeout removes everything again.

This also works nice with both requireJS and Jquery Mobile. In JQM the
body is only loaded on the first page-load, so the `.splash` class can be
added to all pages, but will only be visible on the first page the user
loads.
