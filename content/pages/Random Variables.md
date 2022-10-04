---
type:
- 🌳 Evergreen
tags:
- Math
- Statistics
- Probability
title: Random Variables
categories:
date: 2022-09-26
lastMod: 2022-09-26
---
## Sources

  + [[DTU: Introduction to Statistics]]

## Related Notes

  + [[Discrete Distributions]]

  + [[Continuous Distributions]]

## [[Notes]]

  + **Random variables**
Are the basic building block to describe random outcomes of an experiment. They are functions which assigns a _numerical value_ to _each outcome in the sample space_. They are denoted with capital letters, e.g.
$$X, Y, ...$$

    + They can be either _discrete_ (e.g. dice roll) or _continuous_ (e.g. time spent on homework each week).

    + The outcomes can be _limited_ or _unlimited_. E.g. a dice roll is limited. But also continuous r.v. can be limited to e.g. only positive values such as weights, distances.

    + **Difference between discrete and continuous random variables**

      + In the **continuous** case _integrals_ are used, in the **discrete** case _sums_ are used.

      + In the **continuous** case the probability of observing a _single value is always zero_. In the **discrete** case it _can be positive or zero_.

      + Details see below.

  + **Discrete random variables**
e.g. the roll of a dice

    + **Probability density function (PDF)**
is defined as:

      + $$f(x)=P(X=x)$$

      + It assigns a probability to every possible outcome value of $$x$$. A discrete $$pdf$$ fulfills two properties:

        + There are no negative probabilities for any outcome: $$f(x) \geq 0$$ for all $$x$$

        + And the probabilities of all outcomes sum to 1: $$\sum_{\text {all } x} f(x)=1$$

    + **Cumulated distribution function (CDF)**
for a discrete case is the probability of realizing an outcome or equal to the value x:
$$ F(x)=P(X \leq x)=\sum*{j \text { where } x*{j} \leq x} f\left(x*{j}\right)=\sum*{j \text { where } x*{j} \leq x} P\left(X=x*{j}\right) $$

      + The probability that the outcome of X is in a range is
$$P(a<X \leq b)=F(b)-F(a)$$

      + So basically we are summing the PDF over the range of discrete values of desire. Hence, by definition it can be at most 1.

    + **Expected value**
Is the mean of a discrete random variable X.

      + $$\mu=\mathrm{E}(X)=\sum_{i=1}^{\infty} x_{i} f\left(x_{i}\right)$$

      + So we sum up the all values times their probability. Recall that $$f(x_i)$$ sums to one. That's why this works nicely. So it's a _weighted average_.

    + **Variance**
It is the _squared weighted average_ of all values of $$X$$ subtracted by the mean.

      + $$\mathrm{V}(X)=\mathrm{E}\left[(X-\mu)^{2}\right]=\sum_{i=1}^{\infty}\left(x_{i}-\mu\right)^{2} f\left(x_{i}\right)$$

      + In contrast the standard deviation, it empathizes more on large variations, and less on small ones. (nature of the squaring)

      + Note: It cannot be negative (because of the squaring)

    + **Standard deviation**
Is the _square root of the variance_

      + $$\sigma^{2}=\mathrm{V}(X)$$

      + That way it is easier to describe, as it is on the same scale as the original values.

    + [[Discrete Distributions]]

  + **Continuous Random variables**
heading:: true
e.g. time spent on homework each week

    + **Probability density function (PDF)**
is defined as:

      + The area below the function of one:
$$ \int\_{-\infty}^{\infty} f(x) d x=1 $$

      + So the probability of observing an outcome in the range $$a$$ to $$b$$ is:
$$P(a<X \leq b)=\int_{a}^{b} f(x) d x$$

      + Note that a single value has no area, hence we cannot give a probability for a single value in the continuous case, see:
$$P(X=x)=P(x<X \leq x)=\int_{x}^{x} f(u) d u=0$$

Visualization:
![2021_03_11_image.png](/assets/d812906894ce4474a4b9b7d0be9270dfb1c46c6b379b4503b8794d1d3449f100ab2025b581f14edc8eff8aea3eed8523.png)

    + **Cumulated distribution function (CDF)**

      + We simply use a similar are as in the PDF, but only start on the left side in infinity:
$$F(x)=P(X \leq x)=\int_{-\infty}^{x} f(u) d u$$

      + See how this can never be smaller than 0, and is non-decreasing.

    + **Expected Value**

      + $$\mu=\mathrm{E}(X)=\int_{-\infty}^{\infty} x f(x) d x$$

    + **Variance**
      + $$ \sigma^{2}=\mathrm{E}\left[(X-\mu)^{2}\right]=\int\_{-\infty}^{\infty}(x-\mu)^{2} f(x) d x $$

    + [[Continuous Distributions]]

  + **How to calculate the Mean and Variance of linear combinations?**

    + Holds true for both discrete and continuous variables

    + [[Linear Combinations of Random Variables]]

## Questions
