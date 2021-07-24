# Importing Data into SQL

As a data analyst, you may have data in file formats like `xlsx`, `csv`, or `txt`. You are able to import these files into SQL for your use! 

## CSV
```sql
IMPORT CSV 'file_path' INTO table_name;
```
This will import all the columns from a `csv` file into a table. Then you can move forward with your analysis! 

Not sure how to move forward? Try taking a look at these [basics](https://bjm009.github.io/HealthAnalyticsToolkit/SQL/sql_basics) or this [example](https://bjm009.github.io/HealthAnalyticsToolkit/SQL/sql_covid_ex)!

## TXT
```sql
IMPORT TXT 'file_path' INTO table_name;
```
Same as with the `csv`, this will create a table with all the data from the file. 
