# pg_enterprise_views
A free plugin that enables standard PG to have the operation and maintenance capabilities of enterprise level databases.


**Official website: http://pev.catinfo.com.cn**


**PG official website listing address: https://www.postgresql.org/download/products/6-postgresql-extensions/**

## 1. About PEV
In short, PEV is an enterprise level operation and maintenance plugin developed based on standard PG. A total of dozens of system tables are provided, covering load metrics from the OS to the DB, wait events, session information, client information, timeout locks, long transactions, SQL, SQL execution plans, database objects(database, tables, indexes, sequences and functions,etc.), write processes, and archive processes.And a GUI program is provided for more intuitive use of this data, if you don't want to manually write SQL statements.
![image](https://user-images.githubusercontent.com/106410663/237043291-82e89d8b-6f55-4827-b26a-02aa8f501a45.png)
![image](https://user-images.githubusercontent.com/106410663/237043212-f1f4cccf-dfda-45cc-98fa-a23effd62a14.png)

## 2. Installation steps
1. Download the compressed package corresponding to your PG version and unzip it.
2. Place the pg_enterprise_views.so file in the directory /usr/local/pgsql/lib (This path is actually your PG installation path, You need to check it yourself).
3. Place the pg_enterprise_views--1.0.sql and pg_enterprise_views.control file in the directory /usr/local/pgsql/share/extension (This is also related to your PG installation path).
4. Modify your PG configuration file postgresql.conf: shared_preload_libraries = 'pg_enterprise_views' 
5. Restart PG.
6. Execute in psql: create extension pg_enterprise_views; (Note that this must be installed in the postgres database).

## 3. Usage
Download pev.exe and run on a Windows computer that can connect to your PG server.
Alternatively, if you do not require a graphical interface, you can choose to write your own SQL for querying, but this requires a thorough understanding of the structure and meaning of PEV system tables. It is recommended that you still use PEV GUI tools.

## 4. About Free
We have launched PEV as freeware on PG's official website, you can use the trial edition normally until May 1, 2024 (supporting 24-hour historical data backtracking). If you have any requirements for the Enterprise Edition, please contact: pev@catinfo.com.cn

## 5. About the Activation of the Enterprise Edition
Check version: select pev.pev_register_info(); (There is your exclusive registration code, and if you have any needs, you can contact us to activate it)

Registration code activation: select pev.pev_register('......');
