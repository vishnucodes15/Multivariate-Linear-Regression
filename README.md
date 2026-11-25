# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the Pandas package to process the dataset, sklearn package for creating the model
<br>

### Step2
Read and store the contents in the csv dataset using the function read_csv(()
<br>

### Step3
Getting the required inputs for the prediction model and store it as X,Y
<br>

### Step4
Creating the model using linear_model.LinearRegression and passing X,Y as inputs
<br>

### Step5
Thus , the model is created successfully and now can predict using the function .predict()
<br>

## Program:
# Dataset Setup - Run this cell before starting the experiment
```python
''' 
Program to Load the Dataset using Pandas
Developed by: Sre Vishnu Priyar L N
RegisterNumber: 26009605
'''
import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")
```
# Prediction Model Setup
```python
''' 
Program to form the prediction model
Developed by: Sre Vishnu Priyar L N
RegisterNumber: 26009605
'''
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:

### Insert your output
<img width="928" height="580" alt="image" src="https://github.com/user-attachments/assets/b3de2171-73c0-4501-9452-879f081fe812" />

<br>
<img width="928" height="580" alt="image" src="https://github.com/user-attachments/assets/ac279f20-7a64-428e-b160-1e116e906bd7" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
