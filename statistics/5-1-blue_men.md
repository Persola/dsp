[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```python
import scipy.stats

CM_PER_INCH = 2.54

male_height_dist = scipy.stats.norm(loc=178, scale=7.7)
male_height_dist.cdf(73*CM_PER_INCH) - male_height_dist.cdf(70*CM_PER_INCH)
# => 0.34274683763147457
```
