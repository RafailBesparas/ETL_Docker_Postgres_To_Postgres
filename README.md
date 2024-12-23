# ETL_Docker_Postgres_To_Postgres
The ETL process involves transferring data between two databases, source_db and destination_db, both hosted within Docker containers. The process is automated using a Python-based batch script

Project Workflow
Docker Compose:
Using the docker-compose.yaml file, three Docker containers are launched:

A source PostgreSQL database populated with sample data.
A destination PostgreSQL database for storing the transferred data.
A Python environment that executes the ELT (Extract, Load, Transform) script.
ELT Process:
The elt_script.py waits for the source PostgreSQL database to be ready. Once the database is available, the script utilizes pg_dump to create a SQL dump of the source database. It then uses psql to load the SQL dump into the destination PostgreSQL database.

Database Initialization:
The init.sql script initializes the source database with sample data. It creates multiple tables and populates them with test data for use in the ELT process.
