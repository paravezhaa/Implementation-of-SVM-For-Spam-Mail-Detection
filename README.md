# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: PARAVEZHAA M
RegisterNumber:212225220070

import chardet
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import LinearSVC
from sklearn.pipeline import Pipeline
from sklearn import metrics

file = 'spam.csv'
with open(file, 'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))

data = pd.read_csv('spam.csv', encoding='Windows-1252')
x = data["v2"].values
y = data["v1"].values

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=0)

model = Pipeline([
    ('tfidf', TfidfVectorizer()),
    ('clf', LinearSVC())
])

model.fit(x_train, y_train)
y_pred = model.predict(x_test)

accuracy = metrics.accuracy_score(y_test, y_pred)
print(accuracy)
print(metrics.classification_report(y_test, y_pred))
print(metrics.confusion_matrix(y_test, y_pred))

*/
```

## Output:

<img width="850" height="280" alt="image" src="https://github.com/user-attachments/assets/f595a0d5-fa6e-4256-b06b-b09531dee55e" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
