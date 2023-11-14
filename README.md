# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5. Find the accuracy of the model and predict the required values by importing the required module from sklearn.
## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: H.Berjin Shabeck
RegisterNumber:  212222240018
*/
```
```
import pandas as pd
df=pd.read_csv('Employee.csv')
df
```



```
df.head()
```



```
df.info()
```



```
df.isnull().sum()
```


```
df["left"].value_counts()
```


```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
```
```
df['salary']=le.fit_transform(df['salary'])
df.head()
```


```
df["Departments "].value_counts()
```


```
df['Departments ']=le.fit_transform(df['Departments '])
df.head()
```


```
x=df[['satisfaction_level','last_evaluation','number_project','average_montly_hours','time_spend_company','Work_accident','promotion_last_5years','Departments ','salary']]
x.head()
```


```
x.info()
```


```
y=df['left']
y
```


```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
```
```
x_train.shape
```


```
x_test.shape
```

```
y_train.shape
```

```
y_test.shape
```



```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion='entropy')
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
```



```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```


```
dt.predict([[0.5,0.8,8,9,200,6,0,1,1]])
```

## Output:
![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/16a91699-c138-436a-a728-ff856cfcce0a)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/b201d728-2f3e-474e-bfdb-5ea2c3733f58)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/c878e2d0-4bdc-4747-bf4b-87943ec7b68d)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/1d435e48-d60a-4e1c-8957-06c8f4e033c5)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/2be85711-67d7-4c61-aae7-e937ab760372)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/ed9397d2-bd24-4446-adc1-555fbed64415)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/26bdd0cd-b033-42f8-ae21-9f8c3bf25d5b)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/f4c7cd07-87c1-4bb8-8b55-a55e9a50537e)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/83f12c43-d21b-4e98-9112-46ffc2b5fc95)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/590de63f-46e7-4e29-bb37-fac051e4742b)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/b45ecc21-075d-4190-9951-6099312b0a58)

![image](https://github.com/R-Guruprasad/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119390308/be2e03cf-aec8-436f-9f73-658c5e6e5127)

## Result:
  Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
