---
layout: post
title: Why is Exponential Growth needed? 
subtitle: Corona virus affected count prediction
tags: [MACHINE_LEARNING, data-science]
image: /img/post_1.jpg
comments: true
---

# **Why is Exponential Growth needed?**

Exponential Growth is a mathematical function that can be used in several situations. The formula tells us the number of cases at a certain moment in time, in the case of Coronavirus, this is the number of infected people. In other use cases of exponential growth, this number could be the size of an animal population or the value on your bank account. The reason to use Exponential Growth for modeling the Coronavirus outbreak is that epidemiologists have studied those types of outbreaks and it is well known that the first period of an epidemic follows Exponential Growth.

The formula of Exponential Growth Exponential Growth is characterized by the following formula: x(t) = x0 \* b\*\*t

The Exponential Growth function In which: x(t) is the number of cases at any given time t x0 is the number of cases at the beginning, also called initial value b is the number of people infected by each sick person, the growth factor

A simple case of Exponential Growth: base 2 To make this more clear, I will make a hypothetical case in which: we start with an initial value of 1 infected person, so x0= 1 each sick person infects 2 other people, so the growth rate b = 2 we will inspect the development of the epidemic from time 0 to time 14 We first need to plug the values for a and b in the formula to obtain the formula for our specific epidemic:

Then we can use this formula to compute the value of y for each value of t from 0 to 14. When we do this, we obtain the following numbers of Infected people at every time step, as seen in the below table. This shows that starting from 1 person and with a growth factor of 2 per person, we obtain more than 16000 cases after 14 days.

# **Linear Regression for finding the Growth Factor**

When looking at the data, we only have the number of cases per day, and not the growth factor. The best method to find the growth factor from empirical daily observations is to use a statistical model called Linear Regression. Linear Regression allows us to estimate the best values for a and b in the following formula, given empirical observations for y and x. In this formula, y is the number of cases and x is the time. But we need to do some rewriting on the Exponential Growth function, because Linear Regression can only estimate formulas that look as below:

The type of formula that we need for Linear Regression Rewriting the exponential formula for a linear regression First, we need to rewrite the formula in a form that has the shape of the Linear Regression. The tool we need for this is logarithms. Logarithms allow to rewrite the function in the correct form: y = a + b \* x

where y = log x(t), a = log(x0), b = log(b), x = t

which means log x(t) = log(x0) + log(b) \* t

we use the log of the number of infections instead of the number of infections.

we use the log of growth factor instead of growth factor

The statsmodels table gives the values for a and b under coef (in the middle): The value const is the value for a in our Linear Regression: 0.4480 The value Time is the value for b in our Linear Regression: 0.1128 Therefore we can now fill in the Linear Regression function.
