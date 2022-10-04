---
type:
- 🌳 Evergreen
tags:
- Math
- Statistics
title: statistics of samples
categories:
date: 2022-09-26
lastMod: 2022-09-26
---
## Sources

  + [[DTU: Introduction to Statistics]] Lecture 4

  + [Khan Academy Confidence intervals](https://www.youtube.com/watch?v=hlM7zdf7zwU)

  + [Khan Academy Z Statistics VS T-Statistics](https://www.youtube.com/watch?v=5ABpqVSx33I)

## Related Notes

  + [Random Variables]({{< ref "/pages/Random Variables" >}})

  + [[Discrete Distributions]]

  + [[Continuous Distributions]]

  + [[Hypothesis Test]]

**Mean and variance of repeating an experiment**


  + When you repeat an experiment with new data multiple times, you will always get different **Summary Statistics**
 results.

  + But the nice thing is, that such Mean and Variance will follow the normal distribution!

    + **Central Limit Theorem (CLT)**
      + No matter what, the _distribution of the mean_ becomes a **Normal Distribution**
 when n is large enough! So we can use our confidence intervals also with non-normal distributed data if $$n$$ is large!

      + Rule of thumb: $$n > 30$$

  + Now, see how the expected value of a set of random samples is the _population_ mean, not the sample mean! Should make sense, that the underlying mean is the true mean!
$$ E(\bar{X})=\frac{1}{n} \sum*{i=1}^{n} E\left(X*{i}\right)=\frac{1}{n} \sum\_{i=1}^{n} \mu=\frac{1}{n} n \mu=\mu $$

    + Now more interestingly:
Similarly the **variance of an experiment gets smaller with increasing repetitions of the experiment**!
$$\operatorname{Var}(\bar{X})=\frac{1}{n^{2}} \sum_{i=1}^{n} \operatorname{Var}\left(X_{i}\right)=\frac{1}{n^{2}} \sum_{i=1}^{n} \sigma^{2}=\frac{1}{n^{2}} n \sigma^{2}=\frac{\sigma^{2}}{n}$$

      + Hence, $$\sigma =  \frac{\sigma}{\sqrt{n}}$$

**Standard error**
  + For this, we just subtract the value from the mean (how much "off" is the value from the mean), and divide it by the standard deviation!
$$\frac{\bar{X}-\mu}{\sigma}$$

![2021_03_13_image.png](/assets/ed0720174048424c9779bcf936eb58aac0bdb80cdfb44ab9a22dcf59a478e17d7eb83d6bc66d4375bbd10268061163de.png)

  + The only problem is, that we _do not know_ $$\sigma$$! Luckily we can approximate it by using the proof at the top of this note!
Also as we learned above, this will follow a normal distribution for large $$n$$!
$$\frac{\bar{X}-\mu}{\sigma / \sqrt{n}} \sim N\left(0,1^{2}\right)$$

  + **But what for smaller values?**

    + That's where the **t-Distribution**
 comes in! This distribution represents the behavior much better for especially $$n<30$$, and approaches the normal distribution on larger $$n$$. Hence we can say:
For small $$n$$:
$$\frac{\bar{X}-\mu}{\sigma / \sqrt{n}} \sim N\left(0,1^{2}\right)$$

  + **x-Standard error**

    + Often we use the terminology of e.g. 2-standard error, which means that we mean the interval that is $$2\sigma$$ left and right of the mean $$\mu$$.

**Confidence Interval**
  + Given a experiment that we repeated $$n$$ times to get the _mean of the n sample means of a distribution_.

  + Now we look at a single sample mean (just like in the Standard Error):
What is the _probability_ that this mean lies within e.g. 2-standard error of the actual mean?

    + It's $$\approx 95\%$$ which can be looked up in tables. Note: Take either a Z-table or T-table depending on the size of n.

  + Now, the **confidence interval** tells us in what _range / interval_ the mean lies with e.g. 95% probability.

  + Therefore, we calculate the standard error using our approximation proved at the top of the note:

    + $$\frac{\sigma}{\sqrt{n}}$$

    + And, add and subtract it from the mean!

    + These two values are now our $$1\sigma$$ confidence intervals. For other ones, just multiply the value by the interval you are searching for, and look the confidence up for that new interval.

![2021_03_13_image.png](/assets/3d7e72d86db142ad8767bf3bd06109d32f1efaa432ed48a19aef4fffb66e8d1f7848f4291a1044b695bc34aebcdded2d.png)

  + see close connection to **t-test and p-value**


[[Hypothesis Test]]

[[QQ-Plot]]

## Questions
