# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:KNOWKASH G 
RegisterNumber:212225230142

# Import libraries

import pandas as pd
import numpy as np
from sklearn.tree import DecisionTreeRegressor
import matplotlib.pyplot as plt

# Load the data

df = pd.read_csv('Salary.csv')

# Display the data

print("Salary Data:")

print(df)
print()

# Prepare data

X = df[['Level']]  # Feature (Level)
y = df['Salary']    # Target (Salary)

# Create and train the model

model = DecisionTreeRegressor()
model.fit(X, y)

# Make predictions for all levels

predictions = model.predict(X)

# Show predictions

print("Actual vs Predicted Salaries:")
for i in range(len(df)):
    print(f"Level {df.iloc[i]['Level']}: Actual=${df.iloc[i]['Salary']}, Predicted=${int(predictions[i])}")

# Calculate accuracy (R² score)

accuracy = model.score(X, y)
print(f"\nModel Accuracy (R² Score): {accuracy:.2f}")

# Predict salary for a new level

new_level = [[6.5]]
predicted_salary = model.predict(new_level)
print(f"\nPredicted Salary for Level 6.5: ${int(predicted_salary[0])}")

# Simple visualization

plt.figure(figsize=(8, 5))
plt.scatter(X, y, color='blue', label='Actual Data', s=100)
plt.plot(X, predictions, color='red', label='Decision Tree Predictions', linewidth=2)
plt.xlabel('Level')
plt.ylabel('Salary ($)')
plt.title('Salary Prediction using Decision Tree')
plt.legend()
plt.grid(True)
plt.show()

*/
```

## Output:
salary data:

<img width="348" height="237" alt="image" src="https://github.com/user-attachments/assets/fdebf381-192f-431a-89f1-7b359ddecd80" />

actual vs predicted:
<img width="1047" height="542" alt="image" src="https://github.com/user-attachments/assets/cf761f75-761c-4b0d-8c57-aeaf8ee709aa" />

Accuracy:
<img width="1055" height="162" alt="image" src="https://github.com/user-attachments/assets/3e9a33e5-f997-4a7d-a0a1-07de1d8901d3" />

Decision tree:
<img width="1037" height="693" alt="image" src="https://github.com/user-attachments/assets/e1e5e6a8-25b3-48ae-92ec-18844c3bb607" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
