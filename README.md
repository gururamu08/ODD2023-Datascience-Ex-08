# Ex-08-Data-Visualization-
## AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

## Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## ALGORITHM
### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature generation and selection techniques to all the features of the data set

### STEP 4
Apply data visualization techniques to identify the patterns of the data.

## CODE and OUTPUT
```
import matplotlib.pyplot as plt
```
```
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label='line 1')
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label='line 2')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Two lines on same graph')
plt.legend()
plt.show()
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/6cdc5e57-9c36-4136-8469-ae44e61e037c)

```
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.xlim(1,8)
plt.ylim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('some cool customizations')
plt.show()
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/7d8663ef-f797-43dc-81d6-bd64aa9f7dea)

```
import seaborn as sns
```
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/7625cd3a-13e1-4599-9cbf-dabc3cc84b09)

```
df=sns.load_dataset("tips")
df
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/12623d04-caa2-4fdb-bef5-fc9fdf3b3600)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue='sex',linestyle='solid',legend='auto')
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/7dd27cac-e53e-476a-9741-4d9593a0f2ab)

```
height=[10,24,36,40,5]
names=['one','two','three','four','five']
c1=['red','green']
c2=['b','g']
plt.bar(names,height,width=0.8,color=c2)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My bar Chart!')
plt.show()
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/637961cc-3815-4bbe-9d2b-4d78f5576c81)

```
x=[0,1,2,3,5,8]
y=[3,5,2,6,8,9]
plt.scatter(x,y,s=30,color='blue')
```

```
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=df)
plt.xlabel('Total bill')
plt.ylabel('Tip amount')
plt.title('Scatter plot of Total bill vs Tip amount')
```

```
ages=[5,3,54,76,53,23,42,22,21,20,21,67,65,87,25,57,22]
bins=10
range=(0,100)
plt.hist(ages,bins,range,color='green',histtype='bar',rwidth=0.8)
plt.xlabel('ages')
plt.ylabel('No. of people')
plt.title('My histogram')
plt.show()
```

```
sns.violinplot(x="tip",data=df)
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/c3319771-18e7-417a-a3bd-9e17719c328a)

```
sns.kdeplot(x="tip", data = df,hue='time')
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/dc6df73f-16b6-439a-bc66-fdfe4ebe2ebd)

```
plt.boxplot(x="tip",data=df)
plt.show()
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/35070575-72d7-4403-aabc-0c990501a4bf)

```
sns.boxplot(x='tip',data=df)
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/b1a440bd-9d0d-434c-8f6d-a00a37282266)

```
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
![image](https://github.com/Pranav-AJ/ODD2023-Datascience-Ex-08/assets/118904526/22776a93-1450-4fc2-9bc6-150229cf8f82)


## RESULT

Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
