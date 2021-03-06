# Apply exploratory analysis with Python for Business Values
Values Skills: Data pre-processing, descriptive statistics, Python 
# Task
The manager invited you to a meeting to introduce you to the company's international expansion project. He asks you to do an exploratory analysis to see if the education data of the World Bank can inform the academy's expansion project.Here are the questions you have been asked to explore:   
 ● Which countries have a high customer potential for our services?    
 ● For each of these countries, what will be the evolution of this customer potential?   
 ● In which countries should one set up first?

# Tech 
 Google collab - To perform the  data analysis

 # Intsallation or Libraries
```bash
pip install pandas 
pip install matplotlib
pip install -U wbdat #Api for accessing the world bank data
 ```
 ### Importing the libraries 
 ```python
 import pandas as pd
 import matplotlib.pyplot as plt
 import wbdata
 ```
 Fetching the data 
 ```python
wbdata.get_source() #data source available in world bank data 
wbdata.get_source(12) #the source required for this project 12 = Education Statistics
wbdata.get_indicator(source=12)
df = wbdata.get_dataframe(indicator, country=(list of country),convert_date=False )
 ```
 ### The following indicators which include the secondary or high school students education status of different countries over the past years.
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
![countries list](./image/table1.png)

## Based on the above dataframe which contains the countries list in sorted descending order. 
## Dividing countries based on the continents
### Asia 
### Bangladesh, India, Pakisthan, Nepal, Srilanka, China.
## Europe 
### Germany, France, Ukraine, Irleand, Poland, Finland, UK.
## America
### USA, Brazil, Cuba, Columbia, Argentina.

### Performing data visualization based on the indicators and comparing it with different countries.
```python
plot1(["IN",'BD'],internet_ind,"internet acces per million")
#the following function takes in input as(country, indicator,title for graph) and provides a line graph over years 2009-2019 as per the data available.

```
![internet users in india and bangladesh](./image/graph1.png)
```python
onecon(['BD'],"Bangladesh Graphs")#the following functions takes in the parameter(one country alpha code as list, title)and provides the variation of each parameters over years 
```
![internet users in india and bangladesh](./image/ban.png)

# Conclusions
[google Collab link](https://github.com/tejas-droid/skill-build-/blob/main/edstatsanalysis.ipynb)
 * ### From the above exploration we can note that after considering some of the major features like internet and other sub features we can say in Asia the best countries would        be Bangladesh, China and India.
 * ### From the above exploration it can been seen that Brazil and USA in America.
 * ### From the above exploration it can been seen that Poland, Britain and Finland in Europe.





## Links
[world bank api library documentation](https://pypi.org/project/world-bank-data/)


[Accesing data through its api example using python and R ](https://blogs.worldbank.org/opendata/accessing-world-bank-data-apis-python-r-ruby-stata)

[Accesing data through its api example in kaggle](https://www.kaggle.com/paultimothymooney/how-to-query-the-world-bank-education-data/data?select=series_summary)

[Api git link](https://github.com/OliverSherouse/wbdata)

[world bank Education Statistics (EdStats)](https://datatopics.worldbank.org/education/)

[world bank country list](https://data.worldbank.org/country)

[world banck indicators](https://data.worldbank.org/indicator)

[country name and alpha codes](https://www.iban.com/country-codes)

[World Bank Country and Lending Groups](https://datahelpdesk.worldbank.org/knowledgebase/articles/906519-world-bank-country-and-lending-groups)
