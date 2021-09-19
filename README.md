# school-district-analysis


# School District Analysis using Pandas

### Introduction

Our client, Maria, the chief data scientist for a city school district. We have been contacted to assist with preparing all test data for analysis, reporting, and presentation to provide insights about performance trends and patterns within the various schools within the district.  The overall task we have been hired for is to aggregate the data and show trends in school performance.

### Data Analysis

##### Data

We recieved two csv files to begin analysis, one of which contains personal identifying student information and grades and the other which contains information about the schools within the district. Due to FERPA, no individual student name will be associated with any individual student grade in this report for the privacy of the student. Each individual student is listed with their current grade, current school, and current scores in reading and math. All schools included are high schools, so only grades 9 through 12 are in this analysis. Overall there are 39170 students within the school district at the high school level split between 15 high schools within the district.

##### Analysis

The primary python package we are using for analysis is pandas due to it's strength in handling large amounts of data like we have, and the ease of analysis due to many of the methods and functions contained within the package. Using pandas allows us to read in the csvs directly as dataframes and begin analysis immediately. The data is first cleaned to remove any unnecessary prefixes or suffixes on names, such as Mr or Ms. We further vet our data by checking for any missing data entries and that every columns contains the correct data type. Once the data is validated we merge the two dataframes created by importing the csvs to create one data frame that is a summary of the full school district. 


