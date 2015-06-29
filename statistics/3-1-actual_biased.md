[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

# coding: utf-8

# Exercise from Think Stats, 2nd Edition (thinkstats2.com)<br>
# Allen Downey
# 
# Read the female respondent file.

# In[4]:

get_ipython().magic(u'matplotlib inline')

import chap01soln
resp = chap01soln.ReadFemResp()


# Make a PMF of <tt>numkdhh</tt>, the number of children under 18 in the respondent's household.

# In[6]:

import thinkstats2
pmf = thinkstats2.Pmf(resp.numkdhh)


# Display the PMF.

# In[10]:

import thinkplot
thinkplot.Pmfs([pmf])
thinkplot.Show


# Define <tt>BiasPmf</tt>.

# In[11]:

def BiasPmf(pmf, label=''):
    """Returns the Pmf with oversampling proportional to value.

    If pmf is the distribution of true values, the result is the
    distribution that would be seen if values are oversampled in
    proportion to their values; for example, if you ask students
    how big their classes are, large classes are oversampled in
    proportion to their size.

    Args:
      pmf: Pmf object.
      label: string label for the new Pmf.

     Returns:
       Pmf object
    """
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf


# Make a the biased Pmf of children in the household, as observed if you surveyed the children instead of the respondents.

# In[12]:

biased_pmf = BiasPmf(pmf, label='observed')


# Display the actual Pmf and the biased Pmf on the same axes.

# In[14]:

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Show(xlabel='class size', ylabel='PMF')


# Compute the means of the two Pmfs.

# In[18]:

pmf.Mean()


# In[19]:

biased_pmf.Mean()


# In[2]:
