[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

Since the distribution of heights if roughly normal, we can use the normal distribution with the mean and standard deviation to calculate the percentiles.  Calculate the percentile rank of the high end of the range (6'1"), and subtract the percentile rank of the low end of the range (5'10") to get the percentage of the population in between.

Create the norm object with the mean and std of the dataset:

```
import scipy.stats

heights_norm = scipy.stats.norm(loc = 178, scale = 7.7)
```

Find the CDF percentile ranking of each height:

```
tallest = heights_norm.cdf(185.42)
shortest = heights_norm.cdf(177.80)
```

Compute the difference in percentile ranks for the percentage of population between two heights:

```
tallest - shortest
```
34.2% of men are able to join the Blue Man Group.
