# PRIOR KNOWLEDGE
---
### Key factors of the domain
When analyzing data science salaries in 2023, several key factors need to be considered to provide accurate and meaningful insights. These factors include:
+ **Work Year**: The number of hours or days an employee works per year, which can vary based on full-time, part-time, or contractual arrangements.
+ **Experience Level**: The number of years of relevant experience in the field of data science, which significantly influences salary levels.
+ **Employment Type**: Whether the position is full-time, part-time, contract-based, or freelance, as different employment types offer varying salary structures and benefits
+ **Employment Title**: The specific role within the data science domain, such as data scientist, data analyst, machine learning engineer, or AI researcher, each with its own salary range.
+ **Salary USD**:  The equivalent salary amount converted to US dollars, which provides a standardized comparison for salaries across different countries and currencies.
+ **Employment location**: The location where the employment resides, as salaries can vary significantly based on different countries.
+ **Remote Ratio**: The proportion of remote work allowed in the job, ranging from fully remote positions to those requiring on-site presence.
+ **Employe location**: We can provide career recommendations by suggesting a relocation for the employee based on their current place of residence.
Analyzing data science salaries in 2023 involves considering these factors in combination to provide a comprehensive understanding of the salary landscape in the field. Data scientists and analysts use statistical techniques and data modeling to extract meaningful insights from salary data, considering these variables and their interactions to draw accurate conclusions about salary trends and patterns.

### Business Questions
Following are the business question which we're going to answer by our insights through data science process.
+ **Job Recommendation**:Business Question: Can we suggest a job based on the user's current employment title, experience, and current salary?
+ **Salary Recommendation**: Business Question: Is it possible for us to suggest salaries based on experience?
+ **Location-Based Analysis:**  Business Question: How does the geographic location impact career opportunities and salaries in Data Science, and what recommendations can be provided for individuals considering relocation for their career?
+ **Analysis of Career Growth:** Business Question: What are the various factors that influence the growth of salary in the field of Data Science, including job title and location? Additionally, what recommendations can be made to ensure that salaries of professionals in this field stay competitive based on their job title and location?
+ **Salary Prediction** Business Question: Can future salaries for data science be predicted by considering factors like experience and job title?

### Data Collection
This is the prior knowledge phase to gather relevant data about career recommendation of data science, including its subfield such as data analyst, machine learning etc. We have sourced this data from kaggle to ensure that we meet our requirements then we can able to answer the business questions that are necessary in the data science process.

Sources from which we collect data 
[Kaggle](https://www.kaggle.com/datasets)

# DATA PREPARATION
---
Our Dataset contains 3755 rows × 11 columns which include featuers of data science and these attributes has relationship among them and we'll explore the data by visualization with various libraries available in python to visualize data.

### Importing Libraries
We need to import libraries that are required to process dataset, which will be using to clean data and which are using to visualize data

```python
#Following libraries will be used to perform data exploration
import pandas as pd
import numpy as np
import seaborn as sns                       #Visualisation
import matplotlib.pyplot as plt             #Visualisation
%matplotlib inline
sns.set(color_codes=True)
```

### Loading the data into the data frame
Loading the data into a data frame using the Python library pandas is the initial and crucial step in data exploration or exploratory data analysis. Hence, we must read our CSV file named "ds_salaries2023.csv" that contains a collection of rows and columns and is located in the directory.

```pytho
from google.colab import drive
drive.mount('/content/drive')
```
```pytho
df = pd.read_csv("/content/drive/MyDrive/DSDataSet/ds_salaries2023.csv")
df
```
Now, we will demonstrate the size of our existing unstructured data set prior to cleaning, which will facilitate the comparison of its size post data preparation.

![Data shape and size](/assets/images/shape_size.png)

The execution of the given line of code will generate the visualization of the dataset, displaying its rows and columns.

```pytho
df #just to show the consitency of the data we're going to show the top 5 and bottom 5 rows of the dataset
```

![first df img](/assets/images/df1.png)

Furthermore, we will present the dataset's information, which will help us to understand the dataset.

![first info img](/assets/images/info1.png)

The DataFrame contains data description and generates statistical summaries that depict the distribution's central tendency and shape, excluding NaN values. Additionally, the percentile indicates the number of values that are less than the specified percentile, provided that the DataFrame comprises numerical data.

![first desc img](/assets/images/desc1.png)

### Data type verification
It is important to note that the dataset may consist of attributes of different types. In situations where the data is categorical, it is crucial to transform them into continuous numeric attributes.
![first desc img](/assets/images/dtype1.png)


# 3 - EXPLORATORY DATA ANALYSIS (EDA)
In the exploratory data analysis, We will be looking at the data and try to understand the data. I will begin by looking at the distribution of data across the dat-set, followed by visualising the data to understand the relationship between the features and the target variable.

## 3.1 Work Year
We will showcase the dataset comprising the work done in the years 2020 to 2023.
```pytho
df['work_year'].value_counts()
```
2023    1065

2022    1011

2021    223

2020    75

Name: work_year, dtype: int64

```pytho
plt.figure(figsize=(16,20))
plt.subplot(121)
df['work_year'].value_counts().plot(kind="pie",autopct="%2f",explode=(0.1,0.1,0,0))
plt.title('Job Count by Year')
plt.ylabel('Work Year Count')
plt.savefig("work_year.png")
plt.legend()
plt.show()
plt.savefig("work_year_distribution.png")
```
![first desc img](/assets/images/workYear_pieChart.png)

From above numbers we can say that, we have
```pytho
# A data from 2020 to 2023. Total we have 4 year of data.
```
Based on above counts/data its looks like the requirement of data scientist increased as per years.

## 3.2 Experience Level
The Following lines of code demonstrate the count of job positions categorized by their level of experience in the field of data science.

```pytho
df['experience_level'].value_counts()
```
Senior-Level / Expert         1395

Mid-Level / Intermediate       623

Entry-Level / Junior           261

Executive-Level / Director      95

Name: experience_level, dtype: int64

```pyth
plt.figure(figsize=(16,20))
plt.subplot(121)
df['experience_level'].value_counts().plot(kind="pie",autopct="%2f",explode=(0,0,0,0))
plt.title('Job count by work experience')
plt.savefig("exp_level.png")
plt.legend()
plt.show()
plt.savefig("exp_level_distribution.png")
```
![first desc img](/assets/images/ExLevel_pieChart.png)






