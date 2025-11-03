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
Developed By: Ashqar Ahamed S.T
Register No.: 212224240018
```

```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("titanic_dataset.csv")
df
```

<img width="1392" height="677" alt="data" src="https://github.com/user-attachments/assets/874a6f46-6f0e-475d-abfd-efc52b4e3675" />

<br>

**Line Plot**
<br>
```
X = [1,2,3,4,5,6,7]
Y = [10,15,13,17,18,15,14]
sns.lineplot(x=X,y=Y)
plt.title("Line Plot")
```

<img width="773" height="659" alt="lineplot" src="https://github.com/user-attachments/assets/038e4b32-86db-4c76-a572-a44bec3df649" />

<br>

**Multi Line Plot**
<br>
```
X = [1,2,3,4,5,6,7,8]
Y1 = [12,14,15,16,18,19,20,23]
Y2 = [23,20,18,19,16,14,15,12]
Y3 = [15,17,14,16,18,16,15,17]
plt.figure(figsize=(10, 6))
sns.lineplot(x=X,y=Y1,color='red',label='Y1')
sns.lineplot(x=X,y=Y2,color='green',label='Y2')
sns.lineplot(x=X,y=Y3,color='blue',label='Y3')
plt.xlim(1,8)
plt.ylim(10,25)
plt.title("Multi Line Plot")
```

<img width="927" height="799" alt="multilineplot" src="https://github.com/user-attachments/assets/d890ab44-2930-40cf-9be6-fb99506cf86d" />

<br>

# To Visualize Data Relationships

<br>

**Box Chart**
<br>
```
plt.figure(figsize=(10, 6))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare of Passenger By Embarked Town")
```

<img width="1046" height="764" alt="barchart" src="https://github.com/user-attachments/assets/8e3e79d2-3ace-4047-ab8a-2a2d9aba9bff" />

<br>

**Scatter Plot**
<br>
```
sns.scatterplot(x='Age',y='Fare',data=df)
plt.title("Scatter Plot for Age vs Fare")
```

<img width="742" height="631" alt="SC" src="https://github.com/user-attachments/assets/6afb1192-8ffa-4b38-9466-8b2a08915b18" />

<br>

**Bubble Chart**
<br>
```
sns.scatterplot(x='Age',y='Fare',data=df,size='Pclass',sizes=(30,100))
plt.title("Bubble Chart for Age vs Fare, size by passenger class")

```

<img width="738" height="607" alt="BC" src="https://github.com/user-attachments/assets/440de9b2-ba19-4a83-95ca-00e45c815619" />

<br>

# To Analyze Distributions:

**Histogram**
<br>
```
sns.histplot(data=df,x='Pclass',hue='Survived',kde=True)
```

<img width="741" height="564" alt="hist" src="https://github.com/user-attachments/assets/c464c200-1b3f-4c73-b283-d4fa092b8966" />

<br>

**Box Plot**
<br>
```
sns.boxplot(x='Pclass',y="Age",data=df)
plt.title("Age by Passenger Class")
```

<img width="738" height="617" alt="BP" src="https://github.com/user-attachments/assets/dc3c7bad-c9ef-4459-b9ac-54f4e59c1d1d" />

<br>

**Violine Plot**
<br>
```
sns.violinplot(x='Pclass',y='Fare',data=df)
plt.title("Violin Plot of Age by Passenger Class")
```

<img width="797" height="619" alt="VP" src="https://github.com/user-attachments/assets/3c3e2444-17bc-4eaf-8706-c096b2bd8185" />


**Density Plot**
<br>
```
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
```

<img width="812" height="645" alt="Density" src="https://github.com/user-attachments/assets/e51b1b58-0a07-4357-9a4e-211cba6887a1" />

<br>

**Heat Map**
<br>
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
```

<img width="800" height="736" alt="Heatmap" src="https://github.com/user-attachments/assets/7f30e543-f124-44ab-8915-1bfeceb6aee9" />


<br>

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

