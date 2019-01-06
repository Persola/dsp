[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

```python
%matplotlib inline

import nsfg
import thinkstats2
import thinkplot

resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='# of Kids in Household', ylabel='P')
```

[notebook plots here]

```python
biased_pmf = pmf.Copy(label='# Kids per Household (biased)')

for kid_count, record_count in pmf.Items():
    biased_pmf.Mult(kid_count, kid_count)

biased_pmf.Normalize()

thinkplot.Pmf(biased_pmf)
thinkplot.Config(xlabel='# of Kids in Household (biased)', ylabel='P')
```

[notebook plots here]

```
pmf.Mean()
# => 1.024205155043831

biased_pmf.Mean()
# => 2.403679100664282
```
