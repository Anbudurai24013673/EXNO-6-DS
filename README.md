# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
```

<img width="1357" height="508" alt="image" src="https://github.com/user-attachments/assets/d366fc16-6ddd-4b81-b362-95f675bc4515" />

## Line Plot 

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="842" height="732" alt="image" src="https://github.com/user-attachments/assets/5126adc3-bda0-4054-83cf-26ac13558979" />

## Multi Line Plot

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="771" height="772" alt="image" src="https://github.com/user-attachments/assets/c5f9fbfc-373b-40ba-8c5d-490b5be6b5c5" />

###  TO VISUALIZE RELATIONSHIPS

## Bar Chart

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="1375" height="777" alt="image" src="https://github.com/user-attachments/assets/4525c0b4-7329-4e82-b8e2-39e632e61862" />

## Scatter Plot

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="845" height="678" alt="image" src="https://github.com/user-attachments/assets/236f0bb3-5522-4e48-a0ba-180ac5777b3e" />

## Bubble Chart

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="908" height="677" alt="image" src="https://github.com/user-attachments/assets/4e307bea-23f4-4d17-8250-2b5cd0072768" />

###  TO CAPTURE DISTRIBUTIONS

## Histogram

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="837" height="620" alt="image" src="https://github.com/user-attachments/assets/94442c41-c91b-40d2-8f88-320716e8013c" />

## Box Plot

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="1378" height="778" alt="image" src="https://github.com/user-attachments/assets/0e697386-750f-4b24-b048-e53c154c80a0" />

## Violin Plot

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="893" height="697" alt="image" src="https://github.com/user-attachments/assets/2fa127a1-a263-4fe4-a311-7be3f77d5ff4" />

## Density Plot

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="905" height="763" alt="image" src="https://github.com/user-attachments/assets/e2ccf542-c2e4-4f7f-ae0e-4a035647df40" />

## Heatmap

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="892" height="776" alt="image" src="https://github.com/user-attachments/assets/d17e932a-4687-4867-8119-7640b3c0d132" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
