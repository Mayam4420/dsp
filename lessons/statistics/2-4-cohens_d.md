[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> def CohenEffectSize(group1, group2):
    """Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.totalwgt_lb.mean() - group2.totalwgt_lb.mean()

    var1 = group1.totalwgt_lb.var()
    var2 = group2.totalwgt_lb.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    
    print(diff)
    return d
    
    Results:
    diff = -0.12476118453549034 : the mean of firsts is smaller than others since diff is negative
    d = -0.088672927072602

