[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> effect size: eff size -0.0886729270726.  (Though a negative value seems weird...)
>> Code below:

``` # Code book for for NSFG data
# https://www.cdc.gov/nchs/nsfg/nsfg_cycle6.htm

import nsfg
import pandas
import numpy as np

preg = nsfg.ReadFemPreg()
nsfg.CleanFemPreg(preg)

live = preg[preg.outcome == 1]
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]
first_total_weight = firsts.totalwgt_lb
other_total_weight = others.totalwgt_lb

def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d

eff_size = CohenEffectSize(first_total_weight, other_total_weight)  ```
