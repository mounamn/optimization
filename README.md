## Website Performance Optimization portfolio project 4

## Github

Github Repository: https://github.com/mounamn/optimization

Github Pages: http://mounamn.github.io/optimization/

## Goals:

1. PageSpeed score of 90 or above in index.html (Both Mobile and Desktop).

2. Frame rate of 60fps when scrolling in pizza.html

3. Time to resize pizzas must be less than 5ms in pizza.html

## Results:

1. PageSpeed score of 93/100 on Mobile, and 95/100 on Desktop.
2. Frame rate of 60fps.
3. Time to resize pizzas is less than 5ms.


## Run the Project

--> Use Github pages http://mounamn.github.io/optimization/
   
    or
	
--> Install the project in your machine. You can clone the repository using ## git clone https://github.com/mounamn/optimization.git , or you can download the ZIP from https://github.com/mounamn/optimization

## Optimizations 

-First, I started by optimizing all the images using Grunt and some online optimizers. I converted pizzeria.jpg to png to get smaller size.

*Index.html

-Use Web Font Loader to load the Google webfont asynchronously. 
-Move all the scripts to buttom of the page.
-Set to asynchronous the perfmatters and analytics scripts using the attribute async.
-Used will-change: transform and transform: translateX(); on the class .hero to reduce layout time.
-Define critical CSS and inline it in HTML pages.
-Minify CSS.
-Use media in print.css
-Use Cache-Control for Leverage Browser Cashing.



*Pizza.html and main.js

-Optimized the Javascript bottle neck by modifying updatePosition function:
	+Reduced the writed code.
	+Moved the variables outside the loop.
	+Used getElementByClassName() instead of querySelectorAll() to access specified DOM elements much faster.
	+Reduced the number of phases for every scroll to 5.
-Reduced the number of the moving pizzas created in the background from 200 to 40.
-Moved element.style.width and element.style.height to the file style.css.
-Inline style.css in Pizza.html.
-Used transform:translateX() in style.css to reduce layout time.
-To reduce paint time, I used backface-visibility:hidden.

As a result, the scripting, rendering, and painting times are reduced. Also, the time to resize pizzas is less than 5 ms.
