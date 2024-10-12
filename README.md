# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Dataset: Use pandas to load the dataset (CSV, Excel, etc.) into a DataFrame.
2. Handle Missing Values: Identify and fill or drop missing values.
3. Encode Categorical Variables: Use label encoding or one-hot encoding for categorical data (e.g., department, gender).
4. Split the Dataset: Divide the dataset into features (X) and target (y), then split into training and testing sets.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: MadhanKumar j
RegisterNumber:  2305001016
*/
import pandas as pd
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt


df=pd.read_csv("/content/Employee_EX6.csv")
data=df.copy()
data

le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data

x=data.drop(['Departments','left'],axis=1)
y=data['left']

clf=DecisionTreeClassifier()
clf.fit(x,y)


plt.figure(figsize=(80,80))
plot_tree(clf,feature_names=x.columns,class_names=['LEFT','NOT LEFT'],filled=True)
plt.show()
```

## Output:
![decision tree classifier model](sam.png)

![Screenshot 2024-10-12 100424](https://github.com/user-attachments/assets/f1af08bc-7c72-4538-aa28-674b71554899)

![Screenshot 2024-10-12 100445](https://github.com/user-attachments/assets/fe584324-8f63-44a6-b232-620c741613f4)

![Screenshot 2024-10-12 100607](https://github.com/user-attachments/assets/89174ce9-3376-40f1-9321-33f9e3909126)







## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
