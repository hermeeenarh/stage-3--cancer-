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
