[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> 
# Q: Compute the median, mean, skewness and Pearson’s skewness of the resulting sample.
**Code**: Mean(sample), Median(sample), Skewness(sample), PearsonMedianSkewness(sample)
**Result** 163.3557637457159, 163.2436902397369, 0.10963897481972912, 0.04825166961016246
# Q: What fraction of households reports a taxable income below the mean? How do the results depend on the assumed upper bound?
**Code**: cdf.Prob(Mean(sample))
**Result** 0.660005879566872 >> ~ 66% of the people in the sample have a taxable income below the mean. The higher the upper bound is the higher this % will be, beacuse it it increases the mean and so more people in the same sample fall below the mean.
