# Jupyter Notebooks

This repository contains 12 Jupyter notebooks exploring various computational and data visualisation problems.
I’ve started with simpler examples I had on my computer and plan to gradually increase their complexity and depth.

### Collatz Conjecture Paths
I first came across this conjecture through Project Euler (Problem 14), which asks:

“Which starting number under one million produces the longest Collatz sequence?”

It was the first time I applied memoization to reduce computation time from about 14 seconds to under 2. Although the function in this notebook doesn’t use memoization (since only 5,000 sequences are computed), the concept was a valuable learning point.

I was inspired by a Numberphile video showing a visualisation of Collatz paths.
My first attempt used Python’s turtle module, but since turtle only allows lines ≥ 1 px wide, I switched to Matplotlib with NumPy, allowing me to render thinner 0.3 px lines and a more detailed visual.

Turtle result (1000 paths):

<img src="turtle_collatz.png" alt="My diagram" width="400">




Matplotlib result: View notebook

### Newton Fractals
TODO