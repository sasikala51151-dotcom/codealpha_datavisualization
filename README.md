# codealpha_datavisualization
# Import libraries
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd

# Sample Data
data = {
    'Month': ['Jan', 'Feb', 'Mar', 'Apr', 'May'],
    'Sales': [120, 150, 170, 200, 250],
    'Profit': [20, 30, 35, 40, 50]
}

df = pd.DataFrame(data)

# Set Seaborn Style
sns.set(style="whitegrid")

# -------------------------------
# 1. Line Chart
# -------------------------------
plt.figure(figsize=(6,4))
plt.plot(df['Month'], df['Sales'], marker='o', color='blue')
plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.show()

# -------------------------------
# 2. Bar Chart
# -------------------------------
plt.figure(figsize=(6,4))
plt.bar(df['Month'], df['Sales'], color='green')
plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.show()

# -------------------------------
# 3. Pie Chart
# -------------------------------
plt.figure(figsize=(6,6))
plt.pie(df['Sales'], labels=df['Month'], autopct='%1.1f%%', startangle=90)
plt.title("Sales Distribution")
plt.show()

# -------------------------------
# 4. Histogram
# -------------------------------
plt.figure(figsize=(6,4))
plt.hist(df['Sales'], bins=5, color='orange', edgecolor='black')
plt.title("Sales Histogram")
plt.xlabel("Sales")
plt.ylabel("Frequency")
plt.show()

# -------------------------------
# 5. Scatter Plot
# -------------------------------
plt.figure(figsize=(6,4))
sns.scatterplot(x='Sales', y='Profit', data=df, s=100)
plt.title("Sales vs Profit")
plt.show()

# -------------------------------
# 6. Box Plot
# -------------------------------
plt.figure(figsize=(4,5))
sns.boxplot(y=df['Sales'])
plt.title("Sales Box Plot")
plt.show()