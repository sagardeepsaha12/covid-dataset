# covid-dataset
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv(r"C:\Users\sagar\Downloads\4. covid_19_data.csv")
df.head()
df.count()
df.value_counts
df.isnull().sum()
sns.heatmap(df.isnull())
plt.show()
df.groupby('Region').sum()
df.groupby('Region')['Deaths'].sum().sort_values(ascending=False)
df.groupby('Region').Deaths.sum().sort_values(ascending=False)
df=df[~(df['Confirmed']<10)]
df.groupby('Region').Confirmed.sum().sort_values(ascending=False)
df.groupby('Region').Deaths.sum().sort_values(ascending=True)
df[df.Region=='India']
