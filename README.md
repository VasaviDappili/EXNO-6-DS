# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
Name: DAPPILI VASAVI
Reg.no: 212223040030
```
```py
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("C:/Users/admin/Downloads/titanic_dataset.csv")
 df.head()
```
<img width="1000" height="193" alt="image" src="https://github.com/user-attachments/assets/4ec8bc17-f6cf-4d16-b792-b69217a75e85" />



### 1.Line Plot
```py
x=[2,4,6,8,10]
y=[1,2,3,4,5]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="654" height="478" alt="image" src="https://github.com/user-attachments/assets/3b429c6b-c4c2-497a-b549-fd5cf0cb855a" />

### 2.Multi Line Plot
```py
 x=[2,4,6,8,10]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```
<img width="586" height="475" alt="image" src="https://github.com/user-attachments/assets/0e4ecc4f-c9d8-4d9a-8941-2942a2ed1c2e" />


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(2,3))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="464" height="362" alt="image" src="https://github.com/user-attachments/assets/e92e2a78-6f1c-4453-92ad-5f530fbfb2a7" />


### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="716" height="469" alt="image" src="https://github.com/user-attachments/assets/1806a175-1c73-4f2e-9a10-44f1183c3ca9" />


### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(40, 100))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="692" height="464" alt="image" src="https://github.com/user-attachments/assets/4249dab7-6686-4509-8662-2329d9e852ec" />

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="741" height="472" alt="image" src="https://github.com/user-attachments/assets/1131ff03-4105-4e25-a957-6dce0db8510a" />


### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="707" height="495" alt="image" src="https://github.com/user-attachments/assets/de182153-4ff5-4896-afee-ff928df54c68" />

### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="778" height="463" alt="image" src="https://github.com/user-attachments/assets/21f5bb8f-f3c8-4096-a2ee-a3c0fc2cb7a3" />

### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="760" height="468" alt="image" src="https://github.com/user-attachments/assets/2a9c2a0e-7527-499a-916f-5a184f4bc556" />

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="774" height="521" alt="image" src="https://github.com/user-attachments/assets/f3e9cce3-07b5-4a9e-9d6f-c19f59f0e24f" />


## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

