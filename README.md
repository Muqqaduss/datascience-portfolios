# PRIOR KNOWLEDGE
---
### Key-factors of the domain
When analyzing data science salaries in 2023, several key factors need to be considered to provide accurate and meaningful insights. These factors include:
+ **Work Year**: The number of hours or days an employee works per year, which can vary based on full-time, part-time, or contractual arrangements.
+ **Experience Level**: The number of years of relevant experience in the field of data science, which significantly influences salary levels.
+ **Employment Type**: Whether the position is full-time, part-time, contract-based, or freelance, as different employment types offer varying salary structures and benefits.
+ **Job Title**: The specific role within the data science domain, such as data scientist, data analyst, machine learning engineer, or AI researcher, each with its own salary range.
+ **Salary**: The total compensation received by the employee, including base salary and any additional bonuses, incentives, or benefits.
+ **Salary Currency**: The currency in which the salary is denominated (e.g., USD, Euro, GBP, etc.).
+ **Salary USD**: The equivalent salary amount converted to US dollars, which provides a standardized comparison for salaries across different countries and currencies.
+ **Employee Residence**: The location where the employee resides, as salaries can vary significantly based on the cost of living in different regions and countries.
+ **Remote Ratio**: The proportion of remote work allowed in the job, ranging from fully remote positions to those requiring on-site presence.
+ **Company Size**: The number of employees in the company, which can influence salary levels due to factors such as company revenue, funding, and market position.

Analyzing data science salaries in 2023 involves considering these factors in combination to provide a comprehensive understanding of the salary landscape in the field. Data scientists and analysts use statistical techniques and data modeling to extract meaningful insights from salary data, considering these variables and their interactions to draw accurate conclusions about salary trends and patterns.

### Business Questions
Following are the business question which we're going to answer by our insights through data science process.
+ **Trends Analysis**: Business Question: What are the current trends in the field of Data Science that can inform career recommendations for individuals seeking opportunities in this domain?
+ **Gender Pay Gap**: Business Question: How does the gender pay gap manifest in the field of Data Science, and what recommendations can be made to address or mitigate these disparities?
+ **Location-Based Analysis:** Business Question: How does the geographic location impact career opportunities and salaries in Data Science, and what recommendations can be provided for individuals considering relocation for their career?
+ **Education and Experience Impact:** Business Question: How does one's educational background and professional experience influence success in a Data Science career, and what educational and experiential recommendations can be made to Job Role Satisfaction:
+ **Job Role Satisfaction:** Business Question: What factors contribute to job satisfaction in Data Science roles, and what recommendations can be offered to enhance the overall satisfaction of professionals in their careers?
+ **Inflation vs. Salary Growth**: Business Question: How does inflation impact salary growth in the field of Data Science, and what strategies can be recommended to ensure that professionals salaries keep pace with or outpace inflation.
+ **Benefits Analysis**: Business Question: What are the key benefits that Data Science professionals value, and what recommendations can be made regarding the design and provision of benefits to attract and retain top talent?
+ **Employee Retention**: Business Question: What factors contribute to employee retention in Data Science, and what proactive measures can organizations take to retain their skilled Data Science workforce?
+ **Comparative Analysis**: Business Question: How do career prospects and satisfaction in Data Science compare with other related fields, and what recommendations can be drawn from these comparisons to guide career decisions

### Data Collection
This is the prior knowledge phase to gather relevant data about career recommendation of data science, including its subfield such as data analyst, machine learning etc. We have sourced this data from kaggle to ensure that we meet our requirements then we can able to answer the business questions that are necessary in the data science process.

Sources from which we collect data is 
[Kaggle](https://www.kaggle.com/datasets)

# DATA PREPARATION
---
### Exploratory Data Analysis
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
df = pd.read_csv("/content/drive/MyDrive/DSDataSet/ds_salaries2023.csv")
df
```

![Data from creation](/assets/images/1png.png)

Also we're going to show the information of the dataset which will help us to understand the data.
```pytho
df.info()
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3755 entries, 0 to 3754
Data columns (total 11 columns):
 #   Column              Non-Null Count  Dtype 
---  ------              --------------  ----- 
 0   work_year           3755 non-null   int64 
 1   experience_level    3755 non-null   object
 2   employment_type     3755 non-null   object
 3   job_title           3755 non-null   object
 4   salary              3755 non-null   int64 
 5   salary_currency     3755 non-null   object
 6   salary_in_usd       3755 non-null   int64 
 7   employee_residence  3755 non-null   object
 8   remote_ratio        3755 non-null   int64 
 9   company_location    3755 non-null   object
 10  company_size        3755 non-null   object
dtypes: int64(4), object(7)
memory usage: 322.8+ KB



