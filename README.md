# Ex03-Univariate-Analysis
# AIM:
To read the given data and perform the univariate analysis with different types of plots.

# EXPLAINATION:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# ALGORITHM:
Step1:Read the given data set using standard libraries.

Step2:Get the information about the data.

Step3:Remove the null values from the data.

Step4:Mention the datatypes from the data.

Step5:Count the values from the data.

Step6:Do plots like sepallength,species,sepalwidth.

# PROGRAM:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/iris.csv")

df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()

for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")

sns.countplot(x='species',data=df)

dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')

dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_width","sepal_width").add_legend();
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_length","sepal_length").add_legend();
plt.show()

sns.pairplot(df,hue="species",size=3)

# OUPTUT:
![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/4c27156e-423b-40d2-91cb-0abbee8950f4)

![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/0a4871a5-a8dc-4bbc-b4cd-e63170f63c91)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/16a5e492-aa8d-4811-a215-4f4735c65f25)

![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/37fff205-9a92-4afc-bd8a-8f137ba7bc29)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/3c628b6b-7e27-41e9-bcd4-8a569c9d3e8c)

![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/03934e51-01ae-4089-bb8c-367b6c45401a)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/621f0eb2-8793-44b7-9c34-6b7c54228d0b)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/3d7cd4e7-02db-4e5e-b74d-d4f3822a3526)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/7b4ed800-5e03-4143-9756-f24f5b04d8b3)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/5d537dfd-264e-4184-929b-88ff692e91f9)


![image](https://github.com/vishnupriya20052004/DataSciene_Exp3/assets/133640291/93000703-e954-4178-a280-4b04dbff7d1f)


# RESULT:
Thus we have read the given data and performed the univariate analysis with different types of plots are created and verified succesfully.
