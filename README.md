Front-end Nanodegree Mobile Portfolio
=====================================

If you'd like to see my Mobile Portfolio in action, visit my [GitHub.io project page](https://f00bard.github.io/frontend-nanodegree-mobile-portfolio/).

A number of performance enhancements were made to the provided mobile portfolio.

index.html Pagespeed Insights
-----------------------------

In order to speed up the provided index.html and acheive a PageSpeed Insights score of 92/100 for Mobile and 94/100 for Desktop the following changes were made:

- Comment out reference to Google Web Fontfamily in favor of the specific font faces that are in use
- Inline CSS to avoid an additional HTTP call (no longer relevant in the face of HTTP 2.0?)
- Add media query for print stylesheet
- Move Google Analytics inline script to end of page
- Optimize size of pizzeria.jpg image

pizza.html JS
-------------

In order to speed up page rendering and provide for 60 FPS performance the following changes were made:

- Store document.body.scrollTop in a local variable to avoid reevaluating the DOM for each Math.sin call in updatePositions()
- Store array of pizzas in array after generating all pizzas to avoid requerying the DOM for each call to updatePositions()
- Only add as many "mover" pizzas as needed to fill the available screen height
- Calculate delta width once and apply to all elements