# school-district-analysis


# School District Analysis using Pandas

### Introduction

Our client, Maria, the chief data scientist for a city school district. We have been contacted to assist with preparing all test data for analysis, reporting, and presentation to provide insights about performance trends and patterns within the various schools within the district.  The overall task we have been hired for is to aggregate the data and show trends in school performance.

### Data Analysis

##### Data

We recieved two csv files to begin analysis, one of which contains personal identifying student information and grades and the other which contains information about the schools within the district. Due to FERPA, no individual student name will be associated with any individual student grade in this report for the privacy of the student. Each individual student is listed with their current grade, current school, and current scores in reading and math. All schools included are high schools, so only grades 9 through 12 are in this analysis. Overall there are 39170 students within the school district at the high school level split between 15 high schools within the district.

##### Analysis

The primary python package we are using for analysis is pandas due to it's strength in handling large amounts of data like we have, and the ease of analysis due to many of the methods and functions contained within the package. Using pandas allows us to read in the csvs directly as dataframes and begin analysis immediately. The data is first cleaned to remove any unnecessary prefixes or suffixes on names, such as Mr or Ms. We further vet our data by checking for any missing data entries and that every columns contains the correct data type. Once the data is validated we merge the two dataframes created by importing the csvs to create one data frame that is a summary of the full school district. We can take the math and reading scores for the students and find the percentage passing each course at each high school in the district and the overall percentage of students passing both classes. We can then carry this analysis forward and determine if there is a relationship between the passing rate of students with parameters such as the size of the school, school type, or school funding. This analysis was done both with and without the Thomas High School 9th graders being taken into account.



### Results

![District Summary without changes](https://github.com/roeggealissa/school-district-analysis/blob/57c3db68172dc3e71798edd02e348aa8777211df/Screen%20Shot%202021-09-19%20at%202.25.16%20PM.png)
![District Summary with changes](https://github.com/roeggealissa/school-district-analysis/blob/d04819cc8ee614b34ef11fe05695b4915c03aaab/Screen%20Shot%202021-09-19%20at%202.09.32%20PM.png)

The district summary once Thomas High School is removed has some changes. The number of students has decreased as well as the average math score. The total students is decreased since we are not counting Thomas High School 9th grade students. The average math score dropped by .1 within our formatting bounds, so the actual change may be smaller but with rounding it's .1. This shows that the Thomas High School 9th graders are performing at or above average math level scores for the district.

![School Summary without removing students](https://github.com/roeggealissa/school-district-analysis/blob/b3e7370fac0c171ba13a24506d933081f330188b/School-no-removal.png)
![School Summary with removing students](https://github.com/roeggealissa/school-district-analysis/blob/b3e7370fac0c171ba13a24506d933081f330188b/School-with-removal.png)


The first of the two charts above details the per school summary of performance without removing the Thomas High School 9th graders, and the second chart details the performance per school with the Thomas High School 9th graders removed. The average math scores for Thomas High School decrease by ~0.05 points and the average math scores for Thomas High School increased by ~0.05 points. The perentage of students passing math, reading, and overall dropped by a signifigant margin but this could be attributed to the average still being found for the whole high school which includes the number of 9th graders. As 461 students out of 1635 are in the 9th grade, including them in the count of total students but not their grades for the percentage could drop the pass rate by ~30%. When the analysis is redone with only the number of 10th-12 graders at Thomas High school, the passing rates of math reading and overall increase to 93.185690,97.018739, and 90.630324 respectively which is not statistically different from the original calculations including the 9th graders. This means by not counting the 9th graders grades or counting them in the total amount of students, there is no difference in the average scores or pass rates.

![Top Schools without removal](https://github.com/roeggealissa/school-district-analysis/blob/bc2df21b9c1c2f3131e7bed196a8a0b579f472bb/Top_no_removal.png)
![Top Schools with removal](https://github.com/roeggealissa/school-district-analysis/blob/bc2df21b9c1c2f3131e7bed196a8a0b579f472bb/Top_with_removal.png)

There is statistically no difference between the performance of Thomas High School relative to other schools with and without the 9th grade students included.

