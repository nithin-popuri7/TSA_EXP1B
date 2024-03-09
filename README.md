# Ex.No: 1B                     CONVERSION OF NON STATIONARY TO STATIONARY DATA
# Date: 

### AIM:
To perform regular differncing,seasonal adjustment and log transformatio on international airline passenger data
### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the data preprocessing if needed and apply regular differncing,seasonal adjustment,log transformation.
4. Plot the data according to need, before and after regular differncing,seasonal adjustment,log transformation.
5. Display the overall results.
### PROGRAM:
```
Developed By:P.Siva Naga Nithin
Reg.No:212221240037
```
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv('international-airline-passengers.csv')
x=data.iloc[:,0]
y=data.iloc[:,1]
plt.xlabel('Month')
plt.ylabel('No. of passengers in thousands.')
plt.plot(x,y)
```
### REGULAR DIFFERENCING:
```
data1=data
data1['diff']=data1.iloc[:,1].diff(periods=1)
data1=data1.dropna()
x=data1['Month']
y=data1['diff']
plt.xlabel('Month')
plt.ylabel('No. of passengers in thousands.')
plt.plot(x,y)
```
### LOG TRANSFORMATION:
```
data3=data
data3['log']=np.log(data3['diff']).dropna()
data3=data3.dropna()
x=data3['Month']
y=data3['log']
plt.xlabel('Month')
plt.ylabel('No. of passengers in thousands.')
plt.plot(x,y)
```






### OUTPUT:


REGULAR DIFFERENCING:


SEASONAL ADJUSTMENT:


LOG TRANSFORMATION:



### RESULT:
Thus we have created the python code for the conversion of non stationary to stationary data on international airline passenger
data.
