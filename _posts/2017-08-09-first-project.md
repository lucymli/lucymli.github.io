---
layout: post
title: Looking back at my first R scripts
date: 2017-08-09
---


I regularly hung out with bacteria on petri dishes during my undergraduate days. Since then, I have become good friends with all things Bayesian, played around with particle filters, and enthusiastically adopted R Markdown as my notetaking method of choice. I still hang out with pathogens, but only on screen and in the form of plushie toys. This is my first blog post, so I'll start from the beginning with my first foray into the world of maths and computing (my first [R scripts](https://github.com/lucymli/predator-prey-dynamics/tree/master/R) and my first computational project [report](https://github.com/lucymli/predator-prey-dynamics/raw/master/Final%20Year%20Project%20Report.pdf)).

![Meet my Gonorrhea triplets.](https://github.com/lucymli/lucymli.github.io/raw/master/images/gono-triplets.JPG  "Meet my Gonorrhea triplets!")

---

Final year of university. After a summer in the wet lab, I was more uncertain than ever about what I wanted to do next. It was the first time that I had actually thought about my future career, instead of just blindly doing whatever was available and interesting. While I still found biology interesting, I could not see myself 5 years down the line in a lab coat. It was time for a change of direction. 

After a couple of quantitative courses in my final year, I joined the Ecology department to work on a mathematical modeling project. The aim of my project was to predict the outcome of competition between two consumers and a common resources, e.g. two predators one prey.

Without going into the mathematical details, I simulated competition between two predator species and observed the outcome under various assumptions about the prey carrying capacity (maximum population size), rate of attacking prey, predator death rate, assimilation efficiency (from prey to energy), and immigration rate. 

The first thing that stood out to me while looking over my R code for this project: 

<center> <bold> SO. MANY. FILES. </bold></center>

[Exhibit A](https://github.com/lucymli/predator-prey-dynamics/tree/master/R/Results/9.%20Extras) - At first glance, this looked like a lot of work. But these 15 files only differed at one line. I copy and pasted the same file 15 times, manually edited one parameter, then ran each file individually to obtain simulations with different parameter values.

Another part of my project was to compare the differences between a deterministic (solving differential equations) and a stochastic model (generating random numbers). Because of the randomness of the stochastic model, multiple simulations were required to understand the average behavior of the model. A simple way to do this is to use _for_ loops, which was [what I did](https://github.com/lucymli/predator-prey-dynamics/blob/master/R/Stochastic%202-consumer%20model/Stochastic%202-consumer%20model%201000%20runs.R). Not the most terrible approach, but now that I've learnt about vectorization and parallelization in R, these simulations would have taken a fraction of the time. If I were to rewrite this code now, I would just delegate the simulations to C++ via the [Rcpp package](http://www.rcpp.org/).

Finally, the biggest change I've made to my work in R has been the switch-over from base graphics to [ggplot2](http://ggplot2.tidyverse.org/reference/). Besides being more aesthetically pleasing, the main advantage of using ggplot2 is the ability to save plots as objects, which allows them to be passed to other functions, saved for later reproducibility, and manipulated later (e.g. to add additional data points). I also like the fact that ggplot2 forces me to describe the statistics or relationships that I want to visualize, rather than just describing the lines to draw.

From making base R plots like this:

![](https://github.com/lucymli/predator-prey-dynamics/raw/master/R/Stochastic%202-consumer%20model/Stochastic%202-consumer%20model.png)

To multi-layered ggplot2 graphics like this:

![](https://github.com/lucymli/lucymli.github.io/raw/master/images/Multitree.png)
