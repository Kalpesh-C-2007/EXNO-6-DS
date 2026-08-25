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
Name : KALPESH C

Reg No : 212225230121

```
import pandas as pd 
import seaborn as sns 
import matplotlib.pyplot as plt 
df=pd.read_csv("titanic_dataset.csv") 
df.head()
```

![alt text](image.png)

###  LINE PLOT

```
x=[1,2,3,4,5] 
y=[3,6,2,7,1] 
sns.lineplot(x=x,y=y) 
plt.title('Line Plot')
```

![alt text](image-1.png)

### MULTI-LINE PLOT 

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

![alt text](image-2.png)

## TO VISUALIZE RELATIONSHIPS:

### 1. BAR CHART

```
plt.figure(figsize=(8,5)) 
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

![alt text](image-3.png)

### 2. SCATTER PLOT 

```
sns.scatterplot(x="Age", y="Fare", data=df) 
plt.title('Scatterplot of Age vs Fare') 
plt.show()
```

![alt text](image-4.png)

### 3. BUBBLE CHART

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200)) 
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class') 
plt.show()
```

![alt text](image-5.png)

### 4. HISTOGRAM

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

![alt text](image-6.png)

### 5. BOX PLOT

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow') 
plt.title("Age By Passenger Class")
```

![alt text](image-7.png)

### 6. VIOLIN PLOT

```
sns.violinplot(x="Pclass", y="Fare", data=df) 
plt.title('Violin Plot of Fare by Passenger Class') 
plt.show()
```

![alt text](image-8.png)

### 7. DENSITY PLOT

```
sns.kdeplot(data=df['Age'], shade=True) 
plt.title('Density Plot of Passenger Ages') 
plt.show()
```

![alt text](image-9.png)

### 8. HEATMAP

```
numeric_df = df.select_dtypes(include=['float64', 'int64']) 
corr_matrix = numeric_df.corr() 
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm') 
plt.title('Heatmap of Titanic Dataset') 
plt.show()
```

![alt text](image-10.png)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
