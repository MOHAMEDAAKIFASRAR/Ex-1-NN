<H3>ENTER YOUR NAME : MOHAMED AAKIF ASRAR S</H3>
<H3>ENTER YOUR REGISTER NO : 212223240088</H3>
<H3>EX. NO.1</H3>
<H3>DATE : 24-07-2026</H3>
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

```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

df = pd.read_csv("Churn_Modelling.csv")
df

df.isnull().sum()

df.fillna(0)
df.isnull().sum()

df.duplicated()

df['EstimatedSalary'].describe()

scaler = StandardScaler()
inc_cols = ['CreditScore', 'Tenure', 'Balance', 'EstimatedSalary']
scaled_values = scaler.fit_transform(df[inc_cols])
df[inc_cols] = pd.DataFrame(scaled_values, columns = inc_cols, index = df.index)
df

x = df.iloc[:, :-1]
y = df.iloc[:, -1]

print("X Values")
x

print("Y Values")
y

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size = 0.2, random_state = 42)

print("X Training data")
x_train

print("X Testing data")
x_test

```
## OUTPUT:


# Read the dataset from drive


<img width="1067" height="396" alt="image" src="https://github.com/user-attachments/assets/99dee771-ff13-43e6-8fbf-b3f0929f2b4c" />


# Finding Missing Values


<img width="208" height="468" alt="image" src="https://github.com/user-attachments/assets/86bc010d-6031-4559-b174-2d7939548a75" />


# Handling Missing values

<img width="248" height="495" alt="image" src="https://github.com/user-attachments/assets/21eb5da1-096e-4adc-9be3-d8689fea7a1a" />





# Check for Duplicates

<img width="260" height="416" alt="image" src="https://github.com/user-attachments/assets/bcf5ab9d-257a-4466-9183-b7520fb79627" />

# Detect Outliers


<img width="313" height="310" alt="image" src="https://github.com/user-attachments/assets/f8768679-8e87-4888-9471-d37f40c2447c" />



# Normalize the dataset




<img width="1081" height="450" alt="image" src="https://github.com/user-attachments/assets/f0758aee-c056-4f5a-bcc0-6e0363fc014b" />




# Split the dataset into input and output




<img width="1030" height="477" alt="image" src="https://github.com/user-attachments/assets/301c158c-8099-4e7e-8784-2bcb9f575c16" />




<img width="273" height="457" alt="image" src="https://github.com/user-attachments/assets/c8d1a087-617a-463d-8699-8ae9cea3929c" />

# Print the training data and testing data




<img width="1043" height="473" alt="image" src="https://github.com/user-attachments/assets/ab7a61dc-73b3-4ea7-bf0c-8d6ef9b47f2e" />




<img width="1022" height="427" alt="image" src="https://github.com/user-attachments/assets/a2b0ce0a-5815-4e3e-9ce3-33c13f24c8bf" />




## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


