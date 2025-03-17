<H3>ENTER YOUR NAME : KEERTHIVASAN S</H3>
<H3>ENTER YOUR REGISTER NO : 212223220046</H3>
<H3>EX. NO.1</H3>
<H3>DATE : 17 / 03 / 2025</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:

Cell 1 :
```
import pandas as pd
import io
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```

Cell 2 :
```
d=pd.read_csv("Churn_Modelling.csv")
print(d.isnull().sum())
```

Cell 3 :
```
print(d.duplicated().sum())
```

Cell 4 :
```
plt.figure(figsize=(6,4))
sns.scatterplot(x='Age', y='Exited', data=d)
plt.title('Scatter plot of Age vs. Exited')
plt.show()
```

Cell 5 :
```
scaler = MinMaxScaler()
columns = ['CreditScore', 'Age', 'Tenure', 'Balance', 'NumOfProducts', 'EstimatedSalary']
d[columns] = scaler.fit_transform(d[columns])
```

Cell 6 :
```
print("NORMALIZED DATASET\n",d)
```

## OUTPUT:

Output 1 :

![Screenshot 2025-03-10 220021](https://github.com/user-attachments/assets/b234ac51-d822-430c-b888-b660c253bec0)

Output 2 :

![Screenshot 2025-03-10 220029](https://github.com/user-attachments/assets/3fe983e7-68ca-4f1a-b5d2-80a4ba4821dd)

Output 3 :

![Screenshot 2025-03-10 220036](https://github.com/user-attachments/assets/f2e9603b-7011-4aca-be53-8c45ea722597)

Output 4 :

![Screenshot 2025-03-10 220137](https://github.com/user-attachments/assets/24760874-b7ba-4f50-9a1c-dfbcf179b660)

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.
