# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
# Step 1: Import necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
# Set visualization style
sns.set(style="whitegrid")
plt.rcParams['figure.figsize'] = (10, 6)
# Step 2: Load the Titanic dataset
df = sns.load_dataset("titanic") # Alternatively: pd.read_csv("your_path/titanic.csv")
print("Dataset Loaded Successfully!\n")
print(df.head())
# Step 3: Visualize missing values using a heatmap
plt.figure(figsize=(10, 6))
sns.heatmap(df.isnull(), cbar=False, cmap='viridis', yticklabels=False)
plt.title("Missing Values Heatmap")
plt.show()
# Step 4: Countplot - Number of passengers by gender
sns.countplot(x='sex', data=df, palette='Set2')
plt.title("Count of Passengers by Gender")
plt.xlabel("Sex")
plt.ylabel("Count")
plt.show()
# Step 5: Countplot - Survival status by passenger class
sns.countplot(x='survived', hue='pclass', data=df, palette='Set1')
plt.title("Survival Count by Passenger Class")
plt.xlabel("Survived (0 = No, 1 = Yes)")
plt.ylabel("Count")
plt.legend(title='Pclass')
plt.show()
# Step 6: Histogram - Distribution of passenger ages
sns.histplot(data=df, x='age', kde=True, bins=30, color='skyblue')
plt.title("Age Distribution of Passengers")
plt.xlabel("Age")
plt.ylabel("Frequency")
plt.show()
# Step 7: Boxplot - Age vs Passenger Class
sns.boxplot(x='pclass', y='age', data=df, palette='pastel')
plt.title("Age Distribution Across Passenger Classes")
plt.xlabel("Passenger Class")
plt.ylabel("Age")
plt.show()
# Step 8: Pairplot - Relationships among numerical features
sns.pairplot(df[['age', 'fare', 'pclass', 'survived']], hue='survived', palette='coolwarm')
plt.suptitle("Pairwise Relationships", y=1.02)
plt.show()
# Step 9: Correlation heatmap
corr = df.corr()
sns.heatmap(corr, annot=True, cmap='Blues', linewidths=0.5)
plt.title("Correlation Matrix Heatmap")
plt.show()


<img width="808" height="404" alt="image" src="https://github.com/user-attachments/assets/6dbdf14a-cd2d-4137-8c69-3c1b51298c6b" />



<img width="998" height="759" alt="image" src="https://github.com/user-attachments/assets/8dfec744-ba5f-4a2d-ac1b-954f3e6132bc" />



<img width="1064" height="684" alt="image" src="https://github.com/user-attachments/assets/2d39df15-aafd-45ad-b777-75b0c261a960" />



<img width="1070" height="683" alt="image" src="https://github.com/user-attachments/assets/fc4c0059-61a2-4986-b2c3-e8f3a526c898" />



<img width="1055" height="681" alt="image" src="https://github.com/user-attachments/assets/65b9f592-e876-4e66-a700-add3481f35db" />



<img width="1028" height="905" alt="image" src="https://github.com/user-attachments/assets/02b6e1b3-ce2d-4bf1-beb7-b181d784ce52" />



<img width="967" height="663" alt="image" src="https://github.com/user-attachments/assets/1a675fb1-98a5-4cb2-8a16-7258805f4a79" />

# Result:
Hence Data Visualization was done on the given dataset using seaborn library in python.
