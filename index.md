---
title       : Developing Data Products
subtitle    : Development of a Shiny Application
author      : Quaffle51
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## What the Shiny App is about

The [Shiny](https://quaffle51.shinyapps.io/project1/) App displays five important standard distribution that arise in various areas of statistics.

- the [**Chi-squared**](http://en.wikipedia.org/wiki/Chi-squared_distribution) distribution;
- the [**Student's t**](http://en.wikipedia.org/wiki/Student%27s_t-distribution) distribution;
- the [**F**](http://en.wikipedia.org/wiki/F-distribution) distribution;
- the [**gamma**](http://en.wikipedia.org/wiki/Gamma_distribution) distribution; and
- the [**beta**](http://en.wikipedia.org/wiki/Beta_distribution) distribution.

--- .class #id 

## Features used in making the App

The app makes use of the following features:

- Radio buttons;
- sliders with the animation feature;
- R plots;
- tabs; and
- [MathJax.](http://www.mathjax.org/)
    - For example,  latex commands can by typeset using MathJax to produce the following output.
$$
f_{\gamma}(x) =
\left[
\frac{b^a}{\Gamma(a)}    
\right]
\times
x^{a-1}\exp (-bx)
\quad \text{on } x>0,\\
\text{where } \Gamma(.) \text{ is the Gamma function.}
$$

--- .class #id 
## Example of the R code used in the app
The following code was used to plot the gamma distribution where `a` and `b` are variables set using the sliders.

```r
a <- 1;b <- 1; x <- seq(0,10,0.01); 
k <- function(a,b) (b^a)/gamma(a); f <- function(x,a,b) k(a,b) * x^(a-1) * exp(-b*x)
plot(x, f(x,a,b),type="l",col="red")
```

<img src="assets/fig/gamma-plot-1.png" title="plot of chunk gamma-plot" alt="plot of chunk gamma-plot" style="display: block; margin: auto;" />

--- .class #id

## Overview of the Shiny App

<img src="image1.png" alt="Image of the app" width="800px"></img>
