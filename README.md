## Project 6 - Website Performance Optimization

The goal of this project was to optimize an online portfolio so that `index.html` would score higher than 90 on Google Pagespeed Insights and the animations in `pizza.html` would consistently perform at 60 FPS or higher.

### Getting Started

To view the optimized website, download the .zip files to your computer locally and run index.html inside your browser.

### Optimizations

#### Part 1: Optimize PageSpeed Insights score for index.html

I optimized index.html by implementing the following:

1. Minify all HTML, CSS, and Javascript files
1. Optimize, compress, and resize all images
1. Eliminate render-blocking Javascript elements by loading them asynchronously: `<script async src="http://www.google-analytics.com/analytics.js"></script>`
1. Eliminate render-blocking CSS by using a media query: `<link href="css/print.min.css" rel="stylesheet" media="print">`
1. Eliminate render-blocking CSS by using inline CSS to replace `style.css`

#### Part 2: Optimize Frames per Second in pizza.html

1. Reduce the number of sliding pizzas generated from 200 to 30 pizzas in `main.js` on `line 534`
1. Use `translateX` instead of `basicLeft` to improve 2D CSS animation performance in `main.js` on `lines 513 - 514`
1. Move number generator outside of loop in `main.js` on `line 508`
1. Move `newWidth` and `determineDX` function outside of loop in `main.js` on `lines 453 - 454`

### Contributing
1. Fork it!
1. Create your feature branch: git checkout -b new-feature
1. Commit your changes: git commit -am 'Add new feature'
1. Push to the branch: git push origin new-feature
1. Submit a pull request

### Resources

1. [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
1. [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
1. [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
1. [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
1. [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
1. [Why Moving Elements With Translate() Is Better Than Pos:abs Top/left](http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/)