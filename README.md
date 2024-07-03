Readme:

I have Performed Data Analysis on the World Population Data from 1978-2022 of Seven continents of the World.
The EDA has been done on Jupyter Notebook using Python Language.

Codes Used in this Analysis are :

  IMPORT LIB

1.import pandas as pd
  import seaborn as sns
  import matplotlib.pyplot as plt

 READING THE CSV FILE

2. df = pd.read_csv(r"D:\EDA\world_population.csv")

3. pd.set_option('display.float_format', lambda x: '%.2f' %x)

4. df.info()

5. df.describe()

6. df.isnull().sum()

7. df.nunique()

8. df.sort_values(by="2022 Population" ,ascending = False).head(n=10)

9. df.sort_values(by="World Population Percentage" , ascending=False).head(n=10)

10. df.corr(numeric_only=True)

11. numeric_columns = df.select_dtypes(include=['float'])
    sns.heatmap(numeric_columns.corr(), annot=True)
    plt.rcParams['figure.figsize'] = (40, 7)
    plt.show()

12. df2 = df.groupby('Continent')[df.columns[5:13]].mean(numeric_only =True).sort_values(by="2022 Population",ascending=False)
    df2

13. df3 = df2.transpose()
    df3

14. df3.plot()

15. df.boxplot(figsize =(20,10))

16. df.select_dtypes(include='number')

17. df.select_dtypes(include='object')


 
