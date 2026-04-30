# Mlimport numpy as nm 
import matplotlib.pyplot as pl
import pandas as pd
import seaborn as ss
df =pd.read_csv(r"C:\Users\Mo\Desktop\Data set\emplye\tech_mental_health_burnout.csv")
print(df.columns)
print('#'*30)
print(df.info())
print('#'*30)
print(df.describe())
print('#'*30)
ss.boxenplot(data=df,x="gender",y='age',hue='gender')
pl.show()
# balanced
ss.barplot(data=df,y='age',x="gender",hue='gender')
pl.show()
ss.scatterplot(data=df,x='sleep_hours',y='physical_activity_days',hue="gender",style='gender')
pl.show()

#duplicate
print(df.duplicated().sum())
print('#'*30)
# null
print(df.isna().sum())