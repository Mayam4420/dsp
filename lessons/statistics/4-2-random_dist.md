[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> 

# define t as numpy array containing 1000 random numbers between 0 and create a PMF for t
t = np.random.random(1000)
pmf = thinkstats2.Pmf(t)

# plot the pmf defined above
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='1000 random # between 0 and 1', ylabel='PMF')

# create cdf from t which is made of 1000 random numbers between 0 and 1
cdf = thinkstats2.Cdf(t, label='np.random.random')

# plot the cdf 
thinkplot.Cdf(cdf)
thinkplot.Show(xlabel='1000 random # between 0 and 1', ylabel='CDF')
