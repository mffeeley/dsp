[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

Generate 1000 "random" numbers:
```
sample = np.random.random(1000)
```

Plot the PMF of the sample:
```
sample_pmf = thinkstats2.Pmf(sample, label = 'Sample of 1000')
thinkplot.Pmf(sample_pmf, linewidth = .1)
thinkplot.Config(xlabel = 'Numbers', ylabel = 'PMF')
```
The entire chart is filled because all of the numbers have the same probability.


Plot the CDF of the sample:
```
sample_cdf = thinkstats2.Cdf(sample, label = 'Sample of 1000')
thinkplot.Cdf(sample_cdf)
thinkplot.Config(xlabel = 'Numbers', ylabel = 'CDF')
```
The distribution is uniform since it's a straight diagonal line.
