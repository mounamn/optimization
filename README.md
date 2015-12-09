## Website Performance Optimization portfolio project

-First, I started by optimize all the images using Grunt.

*Index.html

-Download the fonts to use them on my website. 
-Instead of using of referencing the Google Web Font as stylesheet link in the head bu using the following link <link href="//fonts.googleapis.com/css?family=Open+Sans:400,700" rel="stylesheet">, I used @font-face on style.css, which improved the pagespeed score.
-Moved all the scripts to buttom of the page.
-Set to asynchronous the perfmatters and analytics scripts using the attribute async.
-Used will-change: transform and transform: translateX(); on the class .hero to reduce layout time.
-Moved style.css into inline styles.


*Pizza.html and main.js

-Optimized the Javascript bottle neck by modifying updatePosition function:
	+Reduced the writed code.
	+Moved the variables outside the loop.
	+Used getElementByClassName() instead of querySelectorAll() to access specified DOM elements much faster.
	+Reduced the number of phases for every scroll to 5.
-Reduced the number of the moving pizzas created in the background from 200 to 40.
-Moved element.style.width and element.style.height to style.css.
-Used transform:translateX() in dtyle.css to reduce layout time.
-To reduce paint time, I used backface-visibility:hidden.

As a result, the scripting, rendering, and painting times are reduced. Also, the time to resize pizzas is less than 5 ms.
