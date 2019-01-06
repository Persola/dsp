[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

```python
%matplotlib inline

import random
import thinkstats2
import thinkplot

rands = []
for i in range(0, 1000):
    rands.append(random.random())

pmf = thinkstats2.Pmf(rands, label='random module output')
thinkplot.Pmf(pmf)
thinkplot.Show(xlabel='random module output', ylabel='probability mass')
```

[notebook plots here]

```python
cdf = thinkstats2.Cdf(rands, label='random module output')
thinkplot.Cdf(cdf)
thinkplot.Show(xlabel='random module output', ylabel='cumulative distribution')
```

[notebook plots here]

> Is the distribution uniform?

The PMF plot shows a near uniform distribution because the random numbers have a limited number of digits. The CMF plot shows a near uniform distribution.
