[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

firsts = resp.[resp.birthord == 1]
others = resp.[resp.birthord != 1]

first_birthwgt = firsts.totalwgt_lb
other_birthwgt = others.totalwgt_lb

mean1 = first_birthwgt.mean()
mean2 = other_birthwgt.mean()

var1 = first_birthwgt.var()d
var2 = other_birthwgt.var()

d = thinkstats2.CohenEffectSize(first_birthwgt, other_birthwgt)
print ('Cohen d', d)
