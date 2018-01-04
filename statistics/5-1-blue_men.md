[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```
#####Q4. Think Stats, Chapter 5 Exercise 1  
##Statement of problem  
#From the survey data from the Behavioral Risk Factor Surveillance System (BRFSS), find the percentage of the U.S. male population with heights between 5’10” and 6’1”. This height requirement needs to be met in order for one to be considered for the Blue Man Group.  


##Solution

import scipy.stats

mean = 178 #centimeters
stddev = 7.7 #centimeters

def ftandin2cm(feet, inches):
   feet2inches = feet * 12
   inchesTotal = feet2inches + inches
   cmTotal = inchesTotal * 2.54
   return cmTotal
   
#desired lower bound
lowerincm = ftandin2cm(5, 10)

#desired upper bound
upperincm = ftandin2cm(6, 1)


lowerpctrank = scipy.stats.norm.cdf(lowerincm, loc = mean, scale = stddev)
upperpctrank = scipy.stats.norm.cdf(upperincm, loc = mean, scale = stddev)
pctdiff = (upperpctrank - lowerpctrank) * 100
print(‘% of US male population with heights between 5 feet 10 inches and 6 feet 1 inch:’)
print(pctdiff)
```
