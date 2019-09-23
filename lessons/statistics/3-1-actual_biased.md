[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> Compute the pmf for kids per household:
```
kids_pmf = thinkstats2.Pmf(resp.numkdhh, label = 'Kids Per HH PMF')
```

Plot the kids PMF using a bar chart:
```
thinkplot.Hist(kids_pmf)
thinkplot.Config(xlabel = 'Number of Kids', ylabel = 'PMF')
```

Create the biased PMF for kids per household:
```
biased_kids_pmf = kids_pmf.Copy(label = 'Kids Per HH Biased PMF')
for x, p in biased_kids_pmf.Items():
    biased_kids_pmf.Mult(x, x)
biased_kids_pmf.Normalize()
```

Plot the biased PMF for kids per household:
```
thinkplot.Hist(biased_kids_pmf)
thinkplot.Config(xlabel = 'Number of Kids', ylabel = 'PMF')
```

Compute the mean for each PMF:
```
print('Mean actual distribution:', kids_pmf.Mean())
print('Mean biased distribution:', biased_kids_pmf.Mean()
