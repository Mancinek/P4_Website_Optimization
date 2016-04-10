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

##How to run


To run this game [download](https://github.com/Mancinek/P4_Website_Optimization/archive/master.zip) the repository and open the `index.html` file in your browser - the game will start immediately.

OR http://mancinek.github.io/

##Optimizations

###Critical Rendering Path

Goal: index.html achieves a PageSpeed score of at least 90 for Mobile and Desktop.


###Frame Rate

Goal: Optimizations made to views/js/main.js make views/pizza.html render with a consistent frame-rate at 60fps when scrolling.

###Computational Efficiency

Goal: Time to resize pizzas is less than 5 ms using the pizza size slider on the views/pizza.html page. Resize time is shown in the browser developer tools.


##Regrets

I regret I used no build tools (such as Gulp/Grunt) to automatize process of building distribution version of this webpages. It has been done manually with help of compression tools listed in next paragraph (Links).

##Links

The repository can be download[here](https://github.com/Mancinek/P4_Website_Optimization).
Index.html - http://mancinek.github.io/
to test https://developers.google.com/speed/pagespeed/insights/?url=mancinek.github.io

Compression and minify tools:
https://cssminifier.com/
http://jscompress.com/
http://www.willpeavy.com/minifier/
http://compresspng.com/
