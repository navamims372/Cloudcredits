# Cloudcredits
import pandas as pd  
df = pd.read_csv("covid_data.csv")  
df.head()  

df['date'] = pd.to_datetime(df['date'])
df.fillna(0, inplace=True)


import matplotlib.pyplot as plt  
import seaborn as sns  

plt.figure(figsize=(10,5))  
sns.lineplot(x="date", y="cases", data=df, label="Cases")  
sns.lineplot(x="date", y="deaths", data=df, label="Deaths")  
plt.legend()
plt.show()  



