# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 
name: MAHALAKSHMI K
reg  no:212222240057

# AIM:

To Develop a python program to Plot a time series data on  corona  2021 analysis

# ALGORITHM:

 Import the required packages like pandas and matplot

 Read the dataset using the pandas
 
 Calculate the mean for the respective column
  
 Plot the data according to need and can be altered monthly, or yearly.
   
 Display the graph.
 
# PROGRAM:

import pandas as pd

import matplotlib.pyplot as plt

import seaborn as sns

# Load the dataset

file_path = '/content/Covid Data - Asia.csv'

data = pd.read_csv(file_path)

# Clean column names by stripping any extra spaces

data.columns = data.columns.str.strip()

# Rename the first column for easier access

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

![Screenshot (553)](https://github.com/user-attachments/assets/bcd5076d-2af5-46cd-af52-72e479614096)





# RESULT:

Thus we have created the python code for plotting the time series of given data.
