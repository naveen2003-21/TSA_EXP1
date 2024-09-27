# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date:
## Name: NAVEEN KUMAR A
## Reg No:212221240032

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.

# PROGRAM:
## Population:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
## Market Price:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
## Temperature:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```

# OUTPUT:
## Population:
![ts1](https://github.com/Ishu-Vasanth/TSA_EXP1/assets/94154614/422d6b38-3268-4a3b-903a-2a995cc97997)

## Market Price:
![ts2](https://github.com/Ishu-Vasanth/TSA_EXP1/assets/94154614/744432ae-0d4a-4eed-8251-30766677b6f5)

## Temperature:
![ts3](https://github.com/Ishu-Vasanth/TSA_EXP1/assets/94154614/86d585df-0eb1-434b-9674-a6f8ad3f8e97)

# RESULT:
Thus we have created the python code for plotting the time series of given data.
