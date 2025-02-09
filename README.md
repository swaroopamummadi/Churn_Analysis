# Churn_Analysis
### Overview:
This project can show the insights for customer churn analysis of a telecommunication company.
### Scenario:
The telecommunication company is trying to establish themselves in the USA. They are running a trial in Florida. New customers were able to use cellphones on the Teleconfia network at very low rates for one year. Not all customers stayed with Teleconfia for one year, many of them left. The company wants to tackle the problem of customer churn with marketing campaigns.
### used Libraries:
1. NumPy: For numerical computations.
2. Pandas: For data manipulation and analysis.
3. Matplotlib: For data visualization.
4. Seaborn: For statistical plotting in Python and provides dafault styles and color palettes to make statisstical plots more attractive

### Table inspecting:
```
Import pandas as pd
Import sqlalchemy as sa
Engine = sa.create_engine(‘sqllite://Telco_churn.db’)
Connection = engine.connect()
Churn_df = pa.read_sql(‘SELECT * FROM sqlite_master’,connection)
Inspectore = sa.inspect(engine)
Table_names = inspector.get_table_names()
```
### To Read Table:
```
Churn_df_col_names = pd.read_sql(‘SELECT * FROM churn_data’ connection)
Churn_df_col_names
```
### To Read Cities:
```
Churn_df_col_names = pd.read_sql(‘SELECT * FROM Cities’, connection)
Churn_df_col_names
```
### To combine 2 Tables need to perform a joins in SQL
```
Churn_df_inner = pd.read_sql(‘Select * FROM churn_data as cd
JOIN  cities as c
ON cd.local_area_code = c.area_code’)
```



