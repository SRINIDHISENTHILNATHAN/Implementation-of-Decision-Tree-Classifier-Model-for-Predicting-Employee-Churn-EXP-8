# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## EQUIPMENT REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## ALGORITHM:
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5. Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## PROGRAM:
### DATA SET
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: 212222230148
RegisterNumber:  SRINIDHI SENTHIL
import pandas as pd
df=pd.read_csv('Employee.csv')
df
```
### HEAD
```
df.head()
```
### DATA FRAME
```
df.isnull().sum()
```
### COUNTING THE LEFT VALUES
```
df["left"].value_counts()
```
### LABEL ENCORDER 
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["salary"]=le.fit_transform(df["salary"])
df.head()
```
### SEPERATING X DATA
```
x=df[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
```
### SEPERATING Y DATA
```
y=df[["left"]]
y.head()
```
### TRAINING DATA SET
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
```
### DECISION TREE CLASSIFIER
```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```
### ACCURACY 
```
from sklearn import metrics
accuracy= metrics.accuracy_score(y_test,y_pred)
accuracy
```
### PREDICT
```
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```
## OUTPUT:

### DATA SET
![image](https://github.com/user-attachments/assets/cc6e40d8-1d6e-4f77-8ff6-5210daa16551)

### HEAD
![image](https://github.com/user-attachments/assets/4160546e-d85a-458a-9179-55e3982cbef1)

### DATA FRAME
![image](https://github.com/user-attachments/assets/7cbda442-01b1-4228-8996-8939995771a7)

### COUNTING THE LEFT VALUES
![image](https://github.com/user-attachments/assets/384f77f6-4b2a-461b-a03a-aeca2a7f3bcd)

### LABEL ENCORDER 
![image](https://github.com/user-attachments/assets/13fb3265-0335-4793-8edf-28a0df9e193f)

### SEPERATING X DATA
![image](https://github.com/user-attachments/assets/ac238200-c2ac-4c53-b53a-df7a6e08e379)

### SEPERATING Y DATA
![image](https://github.com/user-attachments/assets/2df08a77-23f9-4291-9b79-59bcb1eb43a2)
### ACCURACY 
![image](https://github.com/user-attachments/assets/2fcbbc2c-bb56-4b03-86c8-12c7dec27347)

### PREDICT
![image](https://github.com/user-attachments/assets/f2993780-e75a-4956-a745-f578cd6c4513)



## RESULT:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
