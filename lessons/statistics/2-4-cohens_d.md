[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> First, compare the weights of first babies and second babies
```
firsts.totalwgt_lb.mean()
others.totalwgt_lb.mean()
```

Average for firsts: 7.201094
Average for others: 7.325855


Cohen's effect:
```
diff = firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()

var1 = firsts.totalwgt_lb.var()
var0 = others.totalwgt_lb.var()

n1, n0 = len(firsts.totalwgt_lb), len(others.totalwgt_lb)

pooled_var = (n1 * var1 + n0 * var0) / (n1 + n0)

d = diff / np.sqrt(pooled_var)

d
```
Cohen's effect size -0.08867.  This is negative, as opposed to the positive number for pregnancy length.


