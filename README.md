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
 ```
import seaborn as sns
import matplotlib.pyplot as plt

df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/9c3860ab-3865-4c5f-8b72-43ee02550cbf)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue='sex',linestyle='solid',legend='auto')
```
![image](https://github.com/user-attachments/assets/21088dd2-07c3-4999-9d70-4b4d107b27b0)

```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/8e8585a3-f43e-44f3-9f1e-31fe5224b451)

```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/3ff7d317-6e59-4005-a895-aba8b07adb9b)
```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
```
![image](https://github.com/user-attachments/assets/a4a1628e-907b-4193-a209-0175026b3a9e)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/af44794a-34c3-4cc3-a3a7-6503601beb09)



# Result:
 Include your result here
