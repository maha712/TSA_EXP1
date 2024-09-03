# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

Developed by: MAHALAKSHMI K
Register no.: 212222240057

# AIM:
To Develop a python program to Plot a time series data FOR  Total COVID-19 Cases by Country in Asia (2021)

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the total  cases  in  the  country
4. Plot the data according to country and  given  details
5. Display the graph.
# PROGRAM:

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

file_path = '/content/Covid Data - Asia.csv'
data = pd.read_csv(file_path)


data.columns = data.columns.str.strip()


data.rename(columns={'Country, Other': 'Country'}, inplace=True)

# Plotting Total Cases by Country
plt.figure(figsize=(12, 8))
sns.barplot(x='Total Cases', y='Country', data=data.sort_values('Total Cases', ascending=False))
plt.title('Total COVID-19 Cases by Country in Asia')
plt.xlabel('Total Cases')
plt.ylabel('Country')
plt.grid(True)
plt.show()










# OUTPUT:

![Screenshot (553)](https://github.com/user-attachments/assets/f0df9641-4f10-4fc2-9241-2e34226c1a02)





# RESULT:
Thus we have created the python code for plotting the time series of given data.
