# Superset-tutorial:
Superset Repository for the YouTube Tutorial.

Follow the link provided below to watch the tutorial.

https://www.youtube.com/watch?v=Sb_At33QPfw

## Possible Errors Faced:

`No module named MySQLdb`

## Solution:

1: `sudo apt-get install python3-dev libmysqlclient-dev`

2: `pip install mysqlclient`

3: `pip freeze` just to crosscheck if mysqlclient module now exists

Check:

https://stackoverflow.com/questions/55490201/command-python-setup-py-egg-info-failed-with-error-code-1-in-tmp-pip-build-tu


## MSSQL Connection

1: `pip install pyodbc`

Read Word Document for Extra Steps to allow MSSQL Server Connection Ports i.e for example 1433

2: Connection string:

`mssql+pyodbc://server_name/database_name?driver=SQL Server?Trusted_Connection=yes`

Example:

`mssql+pyodbc://127.0.0.1,1433\SQL2014/AdventureWorks2014?driver=SQL Server?Trusted_Connection=yes` 

Take note of how we put the Port number soon after the IP Address, we used a comma i.e `127.0.0.1,1433`. Also we put our MSSQL instance name having a backslash soon after the port number.


## Reading Links

Python SQL Driver:
https://docs.microsoft.com/en-us/sql/connect/python/python-driver-for-sql-server?view=sql-server-ver15

Microsoft SQL Server - SQL Alchemy:
https://docs.sqlalchemy.org/en/13/dialects/mssql.html#module-sqlalchemy.dialects.mssql.base

https://docs.sdl.com/LiveContent/content/en-US/SDL%20Tridion%20Docs-v1.1.2/GUID-CF5C89EA-0918-4002-8391-80CBEDE0BB5E

MSSQL Connection Strings:

https://www.connectionstrings.com/sql-server/

### WHY pyodbc AND NOT pymssql

`pymssql` was discontinued in November 2019, it can still work but you might need to install FreeTDS first and as well explicitly specify the `pymssql` version . Microsoft is in support of `pyodbc` for connections between MSSQL Server and Python.

https://github.com/pymssql/pymssql

https://github.com/pymssql/pymssql/issues/668



