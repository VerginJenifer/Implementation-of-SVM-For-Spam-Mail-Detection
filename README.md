# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import chardet for encoding detection.
2. Define CSV file path.
3. Read CSV into DataFrame, specifying detected encoding.
4. Display first few DataFrame rows and information.
5. Check for missing values in the DataFrame.
6. Split data into training and testing sets, train SVC model, predict labels, and calculate accuracy score.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: D Vergin Jenifer
RegisterNumber:  212223240174
import chardet
file='/content/spam.csv'
with open(file,'rb')as rawdata:
  result=chardet.detect(rawdata.read(100000))
result
import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows-1252')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:

![328517341-67dfcd3e-f9db-4edb-ac46-fde4e725bb8e](https://github.com/VerginJenifer/Implementation-of-SVM-For-Spam-Mail-Detection/assets/136251012/8c5738eb-ca19-4810-ab26-9d2ed478cc42)
![328517376-8f522455-f021-4d66-a38d-038a35c3190d](https://github.com/VerginJenifer/Implementation-of-SVM-For-Spam-Mail-Detection/assets/136251012/cb28421f-0888-4e62-9390-a70091fc312a)
![328517408-d7cb6c36-522c-473d-94d0-1ba1d7add137](https://github.com/VerginJenifer/Implementation-of-SVM-For-Spam-Mail-Detection/assets/136251012/f9ee048a-6a21-4968-a97a-05edde0cb940)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
