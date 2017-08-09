---
layout: post
title: Looking back at my first R script
---

Most of my days are spent sitting in front of a computer, debugging C++ code and writing new R functions. The 20 year old me would have never dreamt such a thing possible as I was hanging out with bacteria on petri dishes (although some things never change...). I have since picked up a wide range of mathematical, statistical, and programming skills, enabling me to become a more well-rounded infectious disease scientist. 

This is my first blog post, so I'll start from the beginning with my first foray into the world of maths and computing (my first [R scripts](https://github.com/lucymli/predator-prey-dynamics/tree/master/R) and my first computational project [report](https://github.com/lucymli/predator-prey-dynamics/raw/master/Final%20Year%20Project%20Report.pdf)).

![Meet my Gonorrhea triplets.](https://github.com/lucymli/lucymli.github.io/raw/master/images/Avatar.png)

---

Final year of university. After a summer in the wet lab, I was more uncertain than ever about what I wanted to do next. It was the first time that I had actually thought about my future career, instead of just blindly doing whatever was available and interesting. While I still found biology interesting, I could not see myself 5 years down the line in a lab coat. It was time for a change of direction. 

After a couple of quantitative courses in my final year, I joined the Ecology department to work on a mathematical modeling project. The aim of my project was to predict the outcome of competition between two consumers and a common resources, e.g. two predators one prey.

Without going into the mathematical details, I simulated competition between two predator species and observed the outcome under various assumptions about the prey carrying capacity (maximum population size), rate of attacking prey, predator death rate, assimilation efficiency (from prey to energy), and immigration rate. 

The first thing that stood out to me while looking over my R code for this project: SO. MANY. FILES.

[Exhibit A](https://github.com/lucymli/predator-prey-dynamics/tree/master/R/Results/9.%20Extras) - 15 almost identical files to simulate under 15 different sets of parameter values...

