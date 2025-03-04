# stage-3--cancer-
Anatomy and Physiology(cancer)


Learning Solutions


import pandas as pd
# Load the dataset
df_link = 'https://raw.githubusercontent.com/HackBio-Internship/2025_project_collection/refs/heads/main/Python/Dataset/cpg_methylation_age_data.csv'
df = pd.read_csv(df_link)
print(df.head())
from sklearn.model_selection import train_test_split
X = df.drop(columns=['Age'])  # Features
y = df['Age']  # Target
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42) #split 
from sklearn.feature_selection import RFE
from sklearn.linear_model import LinearRegression

import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error

# Example dataset
data = pd.DataFrame({
    'feature1': np.random.rand(100),
    'feature2': np.random.rand(100),
    'target': np.random.rand(100)
})

# Define X (features) and y (target variable)
X = data[['feature1', 'feature2']]  # Selecting features
y = data['target']  # Target variable

# Split data into training and testing sets
X_train_selected, X_test_selected, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Initialize and train the model
linear_model = LinearRegression()
linear_model.fit(X_train_selected, y_train)

# Predict on the test set
y_pred_linear = linear_model.predict(X_test_selected)

# Calculate Mean Squared Error
mse_linear = mean_squared_error(y_test, y_pred_linear)

print("Mean Squared Error:", mse_linear)
