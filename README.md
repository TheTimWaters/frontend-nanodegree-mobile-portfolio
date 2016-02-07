## Website Performance Optimization portfolio project

The objective of this project was to optimize the critical rendering path and make this page (an example online portfolio) render as quickly as possible by applying the techniques taught in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### Summary of Optimizations made to views/js/main.js 

#### Critical Rendering Path
* In all for-loops moved DOM element operations to be outside loop to avoid forced synchronous layouts.

#### Computation Efficiency improvements
* Replaced instances of document.querySelector("#...") with document.getElementById(), since this Web API call is faster.
* Replaced instances of document.querySelectorAll(".<classname>") with document.getElementsByClassName(), since this Web API call is faster.
* In updatePositions(), used the transform CSS property to update background pizza position while page is scrolling and moved DOM element access functions out of the for loop, and removed metrics timing calculations.
Removed function determineDx and in-lined logic to resize pizza image in the changePizzaSizes() function. The switch statement sets the width the a percentage value

#### Frame Rate improvements
* To ensure a steady 60 fps framerate, changed the number of mover pizza elements to be dynamically calculated according to the number of pizzas needed to fill the screen, based on browser window resolution.

### Steps to successfully run the application
1. Download all files in this repository
2. Open index.html in a browser