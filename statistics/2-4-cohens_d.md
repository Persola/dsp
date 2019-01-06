[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python
import nsfg

def cohens_d(group_1, group_2):
  return (
    (group_1.mean() - group_2.mean())
    / group_1.append(group_2).std()
  )

df = nsfg.ReadFemPreg()
live = df[df.outcome == 1]
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

cohens_d(firsts.totalwgt_lb, others.totalwgt_lb)
# => -0.08859523385261192
```
