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
Name: Sanjay C
Reg.no: 212223240150
```
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/c111b446-500b-4b06-b284-572eb6a6d182"> 


### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/2b7fed29-04ac-42de-b325-5ad68b3e36b2" width="300" height="300"> 

### 2.Multi Line Plot
```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/6b052b9d-b734-4079-a94d-f9c0f46039d6" width="300" height="300"> 


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/bcc83b1f-3e33-4793-ac34-686308202586" width="300" height="300"> 

### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/f88c86d0-a615-4347-a4ab-9726858d2b85" width="300" height="300"> 

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/a981076a-4aec-4dd5-8793-5c37af9b3d8b" width="300" height="300"> 

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/8f3d6fba-04a6-414e-aeed-4136c6a3d2ee" width="300" height="300"> 

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/0256c67c-dcc1-4099-8220-572400671d34" width="300" height="300"> 

### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/822c14ba-e4a5-4705-8097-ec0b3b93c880" width="300" height="300"> 

### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/701e4bca-dc51-4963-82d6-4f3b6541d905" width="300" height="300"> 

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img src="https://github.com/PriyankaAnnadurai/EXNO-6-DS/assets/118351569/82f41352-a05b-482c-9328-5da56e384c85" width="300" height="300"> 


## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

