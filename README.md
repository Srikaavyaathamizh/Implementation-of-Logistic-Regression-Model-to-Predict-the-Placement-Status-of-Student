# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
Step 1: start the program

Step 2: Load and preprocess the dataset: drop irrelevant columns, handle missing values, and encode categorical variables using LabelEncoder.

Step 3: Split the data into training and test sets using train_test_split.

Step 4: Create and fit a logistic regression model to the training data.

Step 5: Predict the target variable on the test set and evaluate performance using accuracy, confusion matrix, and classification report.

Step 6:Display the confusion matrix using metrics.ConfusionMatrixDisplay and plot the results.

Step 7:End the program.
```

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: DURGA V
RegisterNumber: 212223230052 
*/

import pandas as pd 
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
df=pd.read_csv("Placement_Data_Full_Class (1).csv")
df.head()
```

## Output:
![Screenshot 2024-10-16 172910](https://github.com/user-attachments/assets/ec2b07ed-22fb-4975-9a48-36fe92051341)

```
df.tail()
```

![Screenshot 2024-10-16 172949](https://github.com/user-attachments/assets/05d3bb91-0bc4-49df-8314-6ba43a069e6e)


```
df.drop('sl_no',axis=1)
```

![Screenshot 2024-10-16 173053](https://github.com/user-attachments/assets/09562447-a2b7-4508-8035-cdc254102c3a)

```
df.drop('sl_no',axis=1,inplace=True)


df["gender"]=df["gender"].astype('category')
df["ssc_b"]=df["ssc_b"].astype('category')
df["hsc_b"]=df["hsc_b"].astype('category')
df["degree_t"]=df["degree_t"].astype('category')
df["workex"]=df["workex"].astype('category')
df["specialisation"]=df["specialisation"].astype('category')
df["status"]=df["status"].astype('category')
df["hsc_s"]=df["hsc_s"].astype('category')
df.dtypes
```

![image](https://github.com/user-attachments/assets/5bb0387b-2b10-4eb2-8b6e-4ff8fd6ac8a2)


```
df["gender"]=df["gender"].cat.codes
df["ssc_b"]=df["ssc_b"].cat.codes
df["hsc_b"]=df["hsc_b"].cat.codes
df["degree_t"]=df["degree_t"].cat.codes
df["workex"]=df["workex"].cat.codes
df["specialisation"]=df["specialisation"].cat.codes
df["status"]=df["status"].cat.codes
df["hsc_s"]=df["hsc_s"].cat.codes

df.info()

df.head()

```

![Screenshot 2024-10-16 173243](https://github.com/user-attachments/assets/7fe5f905-8852-4a79-9dc8-982f3156bae2)

```
X = df.iloc[:, :-1].values
Y = df.iloc[:, -1].values

Y
```

![Screenshot 2024-10-16 173328](https://github.com/user-attachments/assets/05ffc403-1b87-4c8d-86e6-c2192e988979)

```
X
```

![Screenshot 2024-10-16 173417](https://github.com/user-attachments/assets/3ee274af-32e7-41a2-b83f-3bf0b03f7dd2)


![Screenshot 2024-10-16 173542](https://github.com/user-attachments/assets/33bb8779-582c-4210-b5ee-e25b07d3900a)

![Screenshot 2024-10-16 173551](https://github.com/user-attachments/assets/99690210-63a5-40fe-9967-29d063437a16)

![Screenshot 2024-10-16 173600](https://github.com/user-attachments/assets/e6c433da-88fe-47e1-bf90-fe4cf4a1b3fe)

![Screenshot 2024-10-16 173751](https://github.com/user-attachments/assets/badc05c5-66f3-4e21-a178-fc077dff98f5)

![Screenshot 2024-10-16 173807](https://github.com/user-attachments/assets/3c4a4fdc-97f4-4cb5-a3c8-a180e9b2b454)

![Screenshot 2024-10-16 173819](https://github.com/user-attachments/assets/911e04a2-d794-43a9-a510-7a96ad62a841)

![Screenshot 2024-10-16 173824](https://github.com/user-attachments/assets/4883df5e-aa25-4f4c-b15d-1bb8da0b9f86)

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
