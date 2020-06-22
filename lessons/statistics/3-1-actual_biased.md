[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 

# create an object of Pmf for the actual children under 18
pmf1 = thinkstats2.Pmf(resp['numkdhh'], label='actual')

# Create an object for the children under 18 as observed by the children in the household
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
    
# plot the actual and observed variables defined above
biased_pmf1 = BiasPmf(pmf1, label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf1])
thinkplot.Config(xlabel='# under 18 Children', ylabel='PMF')

# print the mean for actual and observed
print('Actual mean', pmf1.Mean())  # 1.024205155043831
print('Observed mean', biased_pmf1.Mean()) #  2.403679100664282
