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
<img width="1132" height="205" alt="image" src="https://github.com/user-attachments/assets/6e10242a-70f4-40fa-aa01-f3329620c915" />


### 1.Line Plot
```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="558" height="461" alt="image" src="https://github.com/user-attachments/assets/7351ead7-e0e9-4664-98d1-0dee95ab3033" />

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
<img width="549" height="459" alt="image" src="https://github.com/user-attachments/assets/f74f73a4-b531-48df-8a24-e6d7925da1f8" />


## TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="731" height="494" alt="image" src="https://github.com/user-attachments/assets/5e6fe8ff-1443-4e55-a925-af438c67188d" />

### 2.Scatter Plot
```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="599" height="456" alt="image" src="https://github.com/user-attachments/assets/d84b3fc7-de76-4103-967e-d95258e82693" />

### 3.Bubble Chart
```py
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="625" height="462" alt="image" src="https://github.com/user-attachments/assets/0fba5afd-7e66-4e05-b946-f7f49912fffd" />

## TO CAPTURE DISTRIBUTIONS
### 1.Histogram
```py
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="616" height="474" alt="image" src="https://github.com/user-attachments/assets/532965e5-b4f7-41cc-8b2d-9aa727cd7bad" />

### 2.Box Plot
```py
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="616" height="474" alt="image" src="https://github.com/user-attachments/assets/f2b8a238-b6ba-418d-925c-90b7af907697" />

### 3.Violin Plot
```py
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="583" height="459" alt="image" src="https://github.com/user-attachments/assets/917c7081-aad7-4c7b-aecb-13a567bb4e27" />

### 4.Density Plot
```py
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="658" height="483" alt="image" src="https://github.com/user-attachments/assets/70226d03-0718-488a-a0fe-952fe250d9af" />

### 5.Heatmap
```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="632" height="511" alt="image" src="https://github.com/user-attachments/assets/755373af-7cc0-4ea8-b9a6-bec1dd264124" />


## Result:
  Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

