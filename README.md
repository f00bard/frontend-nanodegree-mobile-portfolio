Front-end Nanodegree Mobile Portfolio
=====================================

A number of performance enhancements were made to the provided mobile portfolio.

index.html Pagespeed Insights
-----------------------------

In order to speed up the provided index.html and acheive a PageSpeed Insights score of 92/100, the following changes were made:

- Comment out reference to Google Web Fontfamily in favor of the specific font faces that are in use.
- Inline CSS to avoid an additional HTTP call (no longer relevant in the face of HTTP 2.0?)
- Add media query for print stylesheet
- Move Google Analytics inline script to end of page

pizza.html JS
-------------

In order to speed up page rendering and provide for 60 FPS performance the following changes were made:

- Store document.body.scrollTop in a local variable to avoid reevaluating the DOM for each Math.sin call in updatePositions()
