# docker_etl PROJECT 4 

1. Generate BigQuery Service Account and paste value to service_account.json
2. Install docker and docker compose
3. Run `docker-compose up`



Tools
Docker: https://docs.docker.com/desktop/install/windows-install/
Python
How to
Open and start your Docker

Create the docker-compose.yml and create MySQL and Postgres Container declaratively

Run this command to make MySQL and Postgres Image run as a Container detached mode: docker-compose up -d run in background non-detached mode: docker-compose up run in foreground

Login to container db-mysql terminal using command without docker desktop docker exec -it <container_id> bash

Login to MySQL database: mysql --local-infile=1 -uroot -pmysql operational < /docker-entrypoint-initdb.d/init.sql

If error Loading local data is disabled; this must be enabled on both the client and server sides Run this query: SET GLOBAL local_infile=1; inside mysql database then re-run LOAD DATA LOCAL INFILE query.

Go to script directory and setup python virtual environment using python3 -m venv env

Activate env using source env/bin/activate in Windows we can use env/Scripts/activate

Install python requirements.txt using python3 -m pip install -r requirements.txt or pip install -r requirements.txt

Create database in postgresql:

docker exec -it <postgres_container_id> bash
login to postgres db using root user: psql -Upostgres
list databases run: \l
create database named data_warehouse using: create database data_warehouse; query
Choose database using \c data_warehouse
List tables inside database: \d




![Screenshot (1216)](https://github.com/felix11736/docker_etl-main/assets/111951543/ec5e3cc9-43fc-49cf-b006-b7115fa0c698)


![Screenshot (1217)](https://github.com/felix11736/docker_etl-main/assets/111951543/3b20bc60-83ee-4480-86cf-52b8961310dd)
