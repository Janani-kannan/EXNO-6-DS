## EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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

<img width="650" height="456" alt="image" src="https://github.com/user-attachments/assets/7411cb90-07df-404f-ac63-43805357b1d6" />

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto",palette="Set1")

```

<img width="939" height="589" alt="image" src="https://github.com/user-attachments/assets/eaaf5387-214e-4594-94e3-1ee53886d030" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')

```

<img width="949" height="616" alt="image" src="https://github.com/user-attachments/assets/57808cd7-8b50-4332-b84e-c874b03c9023" />


```
import seaborn as sns
import matplotlib.pyplot as plt

tips = sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")["total_bill"].mean()
avg_tip = tips.groupby("day")["tip"].mean()  

plt.figure(figsize=(8,6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill")
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip")
plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()

```

<img width="1116" height="695" alt="image" src="https://github.com/user-attachments/assets/203eea33-da41-4aec-befa-2acc3d58b5a3" />

```
import seaborn as sns
import matplotlib.pyplot as plt

tips = sns.load_dataset("tips")
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()

plt.figure(figsize=(8,6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill", width=0.4)  
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip", width=0.4) 
plt.xlabel("Time of the day")
plt.ylabel("Amount") 
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
plt.show()

```
<img width="1114" height="709" alt="image" src="https://github.com/user-attachments/assets/0737d856-98fd-42dd-bb6f-cda0a44874a1" />

```
import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")
plt.figure(figsize=(8,6))
sns.barplot(x="day", y="total_bill", hue="sex", data=df, palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
plt.show()
```

<img width="1142" height="705" alt="image" src="https://github.com/user-attachments/assets/31620885-37a1-426c-a984-3b663228132f" />

```

import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")  
plt.figure(figsize=(8,6))
sns.scatterplot(x="total_bill", y="tip", hue="sex", data=df, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
plt.show()

```

<img width="1072" height="685" alt="image" src="https://github.com/user-attachments/assets/bef8a45c-003c-4548-a80d-8ec181132fed" />

```

import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")
plt.figure(figsize=(8,6))
sns.histplot(data=df, x="total_bill", hue="smoker", kde=True, palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Smoker Status")  
plt.show()

```

<img width="1024" height="687" alt="image" src="https://github.com/user-attachments/assets/41bbdf54-9311-4472-9ec1-496a2fca2214" />

```

import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset('tips')
plt.figure(figsize=(8,6))
sns.boxplot(x='day', y='total_bill', hue='sex', data=df, palette='Set2')
```

<img width="996" height="713" alt="image" src="https://github.com/user-attachments/assets/906c7898-0907-4970-bddf-1792587d83f0" />

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
            whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})

```

<img width="868" height="582" alt="image" src="https://github.com/user-attachments/assets/047f73a4-f376-4f0c-a4e4-b6f6477615da" />

```

sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, 
               palette="Set1", linewidth=2, inner="quartile") 
plt.xlabel("Day of the week") 
plt.ylabel("Total Bill")  
plt.title("Violin Plot of Total Bill by Day and Smoker Status") 
plt.show()
```

<img width="1112" height="580" alt="image" src="https://github.com/user-attachments/assets/b4553990-7fd6-43eb-ad7e-5885837b4170" />

```

import seaborn as sns
sns.set(style="whitegrid")
tips = sns.load_dataset('tips')  
sns.violinplot(x='day', y='tip', data=tips, palette="Set2") 
```

<img width="893" height="601" alt="image" src="https://github.com/user-attachments/assets/32537604-2a84-4695-8315-55029991b1f4" />

```

import seaborn as sns
sns.set(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"],palette="Set1")

```
<img width="899" height="604" alt="image" src="https://github.com/user-attachments/assets/cbaee6bb-a044-4c40-9ac7-b1ce98c9ecee" />

```

import seaborn as sns
sns.set(style='whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")

```

<img width="960" height="595" alt="image" src="https://github.com/user-attachments/assets/433ca51b-f1d4-4e72-a43e-9ce4a3b21f29" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='layer',linewidth=3,palette='Set2',alpha=0.8)
```

<img width="1000" height="595" alt="image" src="https://github.com/user-attachments/assets/2386a60d-381a-49e5-a02f-cb9ee869836f" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='stack',linewidth=3,palette='Set1',alpha=0.8)
```

<img width="1011" height="594" alt="image" src="https://github.com/user-attachments/assets/2b8b7cb9-5b4b-40f9-9deb-b262d611af71" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)

```

<img width="915" height="604" alt="image" src="https://github.com/user-attachments/assets/f56fa795-b360-45f0-8fc7-0c7e171be19f" />

```
import seaborn as sns
tips=sns.load_dataset('tips')
nums=tips.select_dtypes(include=['float64','int64']).columns
corr=tips[nums].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidth=0.5)

```

<img width="816" height="579" alt="image" src="https://github.com/user-attachments/assets/4e6f9929-332f-46df-8312-09f0879c459a" />

```
sns.heatmap(corr,cmap="YlGnBu")

```

<img width="885" height="570" alt="image" src="https://github.com/user-attachments/assets/3891d414-7f30-4344-9c8e-d26722e01d3e" />


# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
