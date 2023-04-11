# Ex-04-Multivariate-Analysis
# AIM:
Write a python program to visualize the given data by analysing the multivariables in data.
# ALGORITHM:
## STEP 1:
Import the csv file using pandas package.
## STEP 2:
Store the data as dataframe in a variable.
## STEP 3:
Display the information of data such as datatypes, value counts, skewness.
## STEP 4:
Display the data in the barplot,scatter plot and heatmap.
# CODE:
```python
import pandas as pd 
import seaborn as sns
from matplotlib import pyplot as plt
df=pd.read_csv('SuperStore.csv')
df.info()
```
```python
df.dtypes
df['State'].value_counts()
df.describe()
df.kurtosis()
```
```python
sns.scatterplot(x=df['Postal Code'],y=df['Sales'])
```
```python
sns.barplot(x=df['Postal Code'],y=df['Sales'])
```
```python
df.info()
```
```python
postal=df.loc[:,["Sales","Postal Code"]]
postal=postal.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")
sns.barplot(x=postal.index,y="Sales",data=postal)
plt.xticks(rotation=90)
plt.xlabel=("Postal")
plt.ylabel=("Sales")
plt.show()
```
```python
sns.heatmap(df.corr())
```
# OUTPUT:
![229866691-ef1373c6-a66e-451a-8ebc-ba22abb25ee2](https://user-images.githubusercontent.com/118707037/231133278-01b00d53-a95c-4f89-b91f-a64436d7b8da.png)
![229867072-05b452c2-d7b9-462e-820c-a54f680b578a](https://user-images.githubusercontent.com/118707037/231133478-17413971-cae5-44a6-bcb4-6ef7e7dc4a56.png)
![229868374-650d6aa8-8b42-4f42-a098-e249f3138c10](https://user-images.githubusercontent.com/118707037/231133536-9b245505-51b2-42b0-8004-82f550c98fbd.png)
![229869371-d6a6a8e3-f6fa-4428-9837-b89833e2dc34](https://user-images.githubusercontent.com/118707037/231133624-67024680-f83f-4cfe-bc37-be06c1cad336.png)
![229869640-5032e76f-ae89-447d-82a6-4b46077d38db](https://user-images.githubusercontent.com/118707037/231133656-74b793d9-eb37-4e88-86fa-82ec1ba04989.png)
![229872246-8c82960f-b50f-48fe-9a01-273ff98786a6](https://user-images.githubusercontent.com/118707037/231137185-744e6b97-f2d4-4a32-aff4-4e76fb8291fe.png)
![229872323-1738e2b3-578e-449b-a553-ff2277109d7d](https://user-images.githubusercontent.com/118707037/231137221-075ceeab-cfe6-4b46-a638-64086d955944.png)
# RESULT:
Thus, the python program to visualize the given data by analysing the multivariables in data ia auxxwaadully done.
