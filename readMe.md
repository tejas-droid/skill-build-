# Apply exploratory analysis with Python for Business Values
ValuesSkills: Data pre-processing, descriptive statistics, Python 
# Task
The manager invited you to a meeting to introduce you to the company's international expansion project. He asks you to do an exploratory analysis to see if the education data of the World Bank can inform the academy's expansion project.Here are the questions you have been asked to explore:   
●Which countries have a high customer potential for our services?    
●For each of these countries, what will be the evolution of this customer potential?   
●In which countries should one set up first?

# Tech 
 Google collab - To perform the  data analysis

 # Intsallation or Libraries
```bash
pip intsall pandas 
pip intsall matplotlib
pip install -U wbdat #Api for accesing world bank data
 ```
 ### Importing the libraries 
 ```python
 import pandas as pd
 import matplotlib.pyplot as plt
 import wbdata
 ```
 Fetching the data 
 ```python
wbdata.get_source() #data source available in world banck data 
wbdata.get_source(12) #the source required for this project 12 = Education Statistics
wbdata.get_indicator(source=12)
 ```
 ### The following indicators which include the secondary or high school students Education status of diffrenct countries over past years.
* School enrollment, secondary, private (% of total secondary)
* Secondary education, teachers
* Pupil-teacher ratio, secondary
* Secondary education, general pupils
* Secure Internet servers (per 1 million people)
* Government expenditure on education, total (% of government expenditure)
* Expenditure on secondary education (% of government expenditure on education)

# The following data frame indicates list of countries sorted according to values under each indicator.
```python
df_country.head(16)
```
![countries list](./table1.png)

### Performing data visualization based on the indicators and comparing it with different countries.
```python
plot1(["IN",'BD'],internet_ind,"internet acces per million")
#the following function takes in input as(country, indicator,title for graph) and provides a line grapg over  years 2009-2019 as per the data available.

```
![internet users in india and bangladesh](./graph1.png)
```python
onecon(['BD'],"Bangladesh Graphs")#thefollowing functions takes in the parmeter(onecountry alpha code as list,title)and provides the variton of each parameters over years 
```
![internet users in india and bangladesh](./ban.png)

# conclusions







## Links
