[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)
import thinkstats2
import random

samp = [random.random() for x in range (1000)]

pmf = thinkstats2.Pmf(samp)
thinkplot.Pmf(pmf)
thinkplot.Show()

cdf = thinkstats2.cdf(samp)
thinkplot.Cdf(cdf)
thinkplot.Show()
