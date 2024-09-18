### Developed by: Sriram S
### Reg no:212222240105
###  Date: 
# Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data (mulgrave_river)
# ALGORITHM:
1. Import pandas and matplotlib.
2. Load the CSV data into a DataFrame.
3. Display the first few rows and column names.
4. Group data by Airline and Year, summing Enplaned complaints.
5. Plot the number of complaints over time for each airline.
6. Add title, labels, legend, and grid to the plot.
7. Show the plot.
# PROGRAM:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("/content/Mulgrave_river_deeral_joined.csv")
data.head()
data['Timestamp']=pd.to_datetime(data['Timestamp'])
data.set_index('Timestamp',inplace=True)
mean_value=data['Level'].mean()
print("Mean Volume:", mean_value)
plt.plot(data.index, data['Level'],color='b')
plt.xlabel('Date')
plt.ylabel('Level')
plt.title('Level Over Time')
plt.show()
```


# OUTPUT:

![Screenshot 2024-09-18 091555](https://github.com/user-attachments/assets/9a5a9187-ff58-44ca-ae53-3ad502e71faf)


# RESULT:
Thus the python program was successfully created to Plot a time series data.
