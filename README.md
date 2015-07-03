# Website Performance Optimization portfolio project

## Purpose of this project

1. Learn how to identify and increase web applicaiton's performance
2. Optimize critical rendering path, the process by which the browser receives HTML, CSS and JavaScript and the required processing to turn them into rendered pixels.
3. Sstart to think of your work as a continuously running web application that requires a consistent framerate to produce the most enjoyable user experience.

## How to run the application

1. Download the project from Github: https://github.com/hermanwu/frontend-nanodegree-mobile-portfolio
2. Click and Open index.html in the browser. This will show the home page of the portfolio.
3. Open *./views folder, there is the optimized pizza.html page.

## Optimization have done for pizza.html page

1. Ensure a consistent frame rate at 60 fps when scrolling in pizza.html.

- Store all mover classes into one variable, so they do not need to be called in the loop
- Calculate and store documentBodyScrollTop as a local variable to avoid calculating it in the loop

2. Time to resize pizzas is less than 5 ms

- Create a temporary array to store all "randomPizzaContainer" classes, which reduces DOM manipulation in the loop
- Since all pizza pictures' size are same, only the first one is selected for dx calcuation
- Calculate the new width and store it in a local variable since all pizzas have the same new width
- Store the length of the array as a local variable
- Declare the elem variable (var elem;) outside the loop, so it is not created every time the loop is executed
