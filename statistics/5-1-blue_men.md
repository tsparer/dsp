[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 34.2 percent

``` import scipy
# 5 10 = 177.8 cm
# 6 1  = 185.42 cm
dist = scipy.stats.norm(178, 7.7)
tall = dist.cdf(185.42)
shorter = dist.cdf(177.8)
range_perc = tall - shorter
print(range_perc)
```
