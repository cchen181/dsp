[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> #####Q2. Think Stats, Chapter 2 Exercise 4  
>>##Statement of problem  
>>Using data from The National Survey of Family Growth, I need to determine whether first born babies are heavier than non-first born babies or not. This investigation is expanded to determine the extent of the difference between the first borns and non-first borns. Then, compare the Cohen’s d value to the difference in pregnancy length.
>>
>>##Solution  
```
#to determine whether first born babies are heavier than non-first born babies or not  
#This question relates to the concept of central tendency. I address this using the mean() function in pandas.


import nsfg

df = nsfg.ReadFemPreg()
df.columns
#columns of interest: 
#df.numkdhh -> NUMBER OF BIO/ADOPT/RELATED/LEGAL CHILDREN UNDER AGE 18 IN HOUSEHOLD

firstWeight = df.loc[df.birthord == 1, ‘totalwgt_lb’]
othersWeight = df.loc[df.birthord > 1, ‘totalwgt_lb’]

firstWeightMean = firstWeight.mean() 
othersWeightMean = othersWeight.mean() 

print(‘First born babies, mean weight in lbs:’)
print(firstWeightMean) #7.201094430437772
print(‘Non-first born babies, mean weight in lbs:’)
print(othersWeightMean) #7.325855614973262




#to determine the extent of the difference between the first borns and non-first borns
#This question relates to the calculation of effect size, or computing Cohen’s d. I address this by applying the definition of Cohen’s d to the problem above.

def Cohensd(group1, group2):
    diff = group1.mean() - group2.mean()
    var1 = group1.var()
    var2 = group2.var()
    n1 = len(group1)
    n2 = len(group 2)
    pooledVar = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / math.sqrt(pooledVar)
    return d

print(‘Cohen\’s d, weight:’)
Cohensd(firstWeight, othersWeight) #-0.088672927072602
dweight = d
print(‘The difference in the means of the weight of first and non-first born babies is -0.0886 standard deviations, which is small.’)


#compare the Cohen’s d value to the difference in pregnancy length
#This question relates to the comparison of Cohen’s d values for weight and pregnancy length. In support of a solution,  I apply the definition of Cohen’s d to pregnancy length.
firstPregDur = df.loc[df.birthord == 1, ‘prglngth’]
othersPregDur = df.loc[df.birthord > 1, ‘prglngth’]

print(‘Cohen\’s d, pregnancy length:’)
Cohensd(firstPregDur,othersPregDur) #0.028879044654449883

print(‘The difference in the means of the pregnancy length of first and non-first born babies is 0.0289 standard deviations, which is even smaller.’)

dpreg = d
ratio = dweight / dpreg
print(‘ratio of Cohen’s d for weight to pregnancy length:’)
print(ratio) #-3.0704937830739034
print(‘The Cohen’s d for the weight of first borns to non-first borns is -3.070 times larger in comparison to the Cohen’s d for pregnancy length.’)
```


