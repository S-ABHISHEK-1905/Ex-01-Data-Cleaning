# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
~~~
import pandas as pd
d=pd.read_csv("./Data_set.csv")
d.head()
d.info()
d.isnull().sum()
#mode
d['show_name']=d['show_name'].fillna(d['aired_on'].mode()[0])
d['aired_on']=d['aired_on'].fillna(d['aired_on'].mode()[0])
d['original_network']=d['original_network'].fillna(d['aired_on'].mode()[0])
d.head()
#mean
d['rating']=d['rating'].fillna(d['rating'].mean())
d['current_overall_rank']=d['current_overall_rank'].fillna(d['current_overall_rank'].mean())
d.head()
#median
d['watchers']=d['watchers'].fillna(d['watchers'].median())
d.head()
d.info()
d.isnull().sum()
~~~

# OUPUT
##DATA
![image](https://user-images.githubusercontent.com/66360846/188836810-458f8404-df1d-41ea-9e25-ff1a7cae38f6.png)

##BEFORE NON NULL
![image](https://user-images.githubusercontent.com/66360846/188837076-5213a681-5cf1-4bcd-8c28-67191b4b3b78.png)


##MODE
![image](https://user-images.githubusercontent.com/66360846/188837288-99a75581-7537-413f-8b33-b8786deb9ed9.png)

##MEAN
![image](https://user-images.githubusercontent.com/66360846/188837521-26f767af-f4e4-4af8-85e0-6b6571b4e9c7.png)

##MEDIAN
![image](https://user-images.githubusercontent.com/66360846/188837605-cf301432-4446-41b4-b01b-d6d933e6e0df.png)

##AFTER NOT NULL
![image](https://user-images.githubusercontent.com/66360846/188837726-f193aea2-c1f6-4eac-a2f9-2b42b7bd28cd.png)

#RESULT:
Thus ,the given data is red and cleansed and the cleaned data is saved into the file.
