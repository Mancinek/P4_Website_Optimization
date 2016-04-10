#Website Optimization

This is a repository that contains two webpages index.html and views/pizza.html optimized to work fast and silky smooth. You will find here source (src folder) and distribution (dist folder) version of the project.

##Contents

1. How to run
2. Optimizations:
	- Critical Rendering Path
	- Frame Rate
	- Computational Efficiency
3. Regrets
4. Links

##1. How to run

First [download](https://github.com/Mancinek/P4_Website_Optimization/archive/master.zip) the repository.

To run firts web page (Cam's Portfolio) open the `dist/index.html` file in your browser. To test speed you can use ngrok to virtualize your localhost and test it with PageSpeed. You can also run this [page](http://mancinek.github.io/) - it is version of this page hosted on github. You can test it directly on [PageSpeed](https://developers.google.com/speed/pagespeed/insights/?url=mancinek.github.io).

To run second web page (Cam's Pizzeria) run `dist/views/pizza.html` in your browser and then test it with Chrome Developer Tools.

##2. Optimizations

I've made several optimizations in both files to reach the set goals.

###Critical Rendering Path

*Goal: index.html achieves a PageSpeed score of at least 90 for Mobile and Desktop.*

Summary of changes I've made:
- inline `style.css` and added `@font-face` in this style
- created `css/print.min.css` and used `media="print"` in HTML
- inline scripts and placed at the end of the body with `async` attribute
- compressed images


###Frame Rate

*Goal: Optimizations made to `views/js/main.js` make `views/pizza.html` render with a consistent frame-rate at 60fps when scrolling.*

Summary of changes I've made:
- changes in updatePositions() function:
	- pulling `scrollTop` outside the loop (`scroll` variable)
	- created array `phaseTab` filled with sines of scroll's
	- refactored for-loop with use of `phaseTab` array
	- `items[i].style.left` and `basicLeft` replaced with faster `translateX`
	- selector of items `window.items=document.getElementsByClassName("mover")` placed in last anonymous function at the end of file. The method of selecting items has been also changed from `querySelectorAll` to faster `getElementsByClassName`
- changed max number of pizzas in last function to dependant on screen size
- replaced `elem.basicLeft` in last function with `elem.style.left`
- used `will-change` and `backface-visiblity` for `.mover` in `style.css`
- used hacks `translate3d(0,0,0)` and `translateZ(0)` for `.mover` in `style.css`
- compressed `pizza.png`

###Computational Efficiency

*Goal: Time to resize pizzas is less than 5 ms using the pizza size slider on the `views/pizza.html` page. Resize time is shown in the browser developer tools.*

Summary of changes I've made:
- deleted ineffective `determineDX()` function
- `switch(size)` method moved to `changePizzaSizes()` function
- new variable `newWidth` placed in `switch(size)` method and converted to percentage
- changed `querySelectorAll` to faster `getElementsByClassName` for `randomPizzas` variable
- refactored the for-loop in `changePizzaSizes()` for effective calculation of new width of pizzas without `determineDX()` function


##3. Regrets

I regret I used no build tools (such as Gulp/Grunt) to automatize process of building distribution version of this webpages. It has been done manually with help of compression tools listed in next paragraph (Links).

##4. Links

Cam's Portfolio: http://mancinek.github.io/

PageSpeed: https://developers.google.com/speed/pagespeed/insights/

Compression and minify tools:
- https://cssminifier.com/
- http://jscompress.com/
- http://www.willpeavy.com/minifier/
- http://compresspng.com/
