# Jupyter Notebooks

![Python](https://img.shields.io/badge/python-3.7+-blue.svg)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-notebook-orange.svg)
![NumPy](https://img.shields.io/badge/numpy-1.21+-blue.svg)
![Matplotlib](https://img.shields.io/badge/matplotlib-3.5+-orange.svg)
![JavaScript](https://img.shields.io/badge/javascript-ES6+-yellow.svg)



This repository contains half a dozen Jupyter notebooks exploring various computational and data visualisation problems.
I’ve started with simpler examples I had on my computer and plan to gradually increase their complexity and depth.

### Collatz Conjecture Paths
I first came across this conjecture through Project Euler (Problem 14), which asks:

“Which starting number under one million produces the longest Collatz sequence?”

It was the first time I applied memoization to reduce computation time from about 14 seconds to under 2. Although the function in this notebook doesn’t use memoization (since only 5,000 sequences are computed), the concept was a valuable learning point.

I was inspired by a Numberphile video showing a visualisation of Collatz paths.
My first attempt used Python’s turtle module, but since turtle only allows lines ≥ 1 px wide, I switched to Matplotlib with NumPy, allowing me to render thinner 0.3 px lines and a more detailed visual.

Turtle result (1000 paths):

<img src="turtle_collatz.png" alt="collatz turtle" width="400">

Matplotlib result: https://github.com/Michalous/jnb/blob/main/collatz_conjecture.ipynb

### Newton Fractals
$$
\quad x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}\quad
$$

I have been familiar with the Newton–Raphson method for some time. It can, for instance, be used to compute square roots and typically converges much faster than the bisection method.

When I developed the Zoomable Mandelbrot Set project, I was inspired to create something similar using Newton’s method. Both approaches involve evaluating convergence and divergence across the complex plane, however in this case the process requires a polynomial, its derivative, and its roots.

I initially tested the algorithm on a 20 × 20 grid, producing the result shown below:

<img src="newton_fractal.png" alt="newton fractal" width="400">

This first version used only three colors, but it confirmed that the idea worked. The upgraded version uses an 800 × 800 grid and 20 shades per color, where each shade represents the number of iterations required for a point to converge to a particular root. 

Find it here: https://github.com/Michalous/jnb/blob/main/newton_raphson.ipynb

### The Trapped Knight
I came across this problem through another Numberphile video, which demonstrated how a chess knight behaves when constrained to always move to the lowest-numbered unvisited square on an infinite spiral-numbered grid.

The concept is simple: starting from the center (square 1), the knight evaluates its eight possible moves and chooses the one with the smallest number. That square is then marked as visited, and the process repeats. Eventually, after a finite number of moves, the knight becomes "trapped" - all possible moves lead to previously visited squares.


<img src="knight.png" alt="trapped knight" width="400">

The result shows the knight's path over 2016 moves, with color coding representing different phases of the journey.

You can find the path here: https://github.com/Michalous/jnb/blob/main/trapped_knight.ipynb

### Chaos Game
I came across the Chaos Game through James Gleick's book "Chaos: Making a New Science." I had previously implemented the classic triangle version in JavaScript along with the Sierpinski carpet and Barnsley fern.
This can be found here: https://michalous.github.io/sierpinski

<img src="chaos.png" alt="chaos game" width="400">

The Chaos Game is a simple algorithm that generates fractal patterns through iterative rules. Starting from a random point, you repeatedly choose a random vertex of a shape and move halfway toward it, plotting each new point. Over many iterations, this creates self-similar fractal structures that fill the space between the original vertices.

For this implementation, I chose a regular pentagon. I initially experimented with different iteration counts and starting positions to understand how the pattern emerges.

The final version generates 120,000 points, revealing the intricate fractal that develops between the pentagon's vertices.


This project demonstrates how deterministic rules applied randomly can produce complex patterns. 

You can have a look at it here: https://github.com/Michalous/jnb/blob/main/chaos_game.ipynb

