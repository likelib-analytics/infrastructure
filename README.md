# Infrastructure

Running only clickhouse and kafka with default settings: `docker-compose -f docker-compose-infrastructure.yml up`

# Full project setup

Please put all the necessary apps(client, api, exporter, migrations) into the same folder as the infrastructure project. 

1. Run Kafka and Clickhouse DB: 
  - `cd ../infrastructure`
  - `docker-compose -f docker-compose-infrastructure.yml up`
2. Run migrations in a new termnial session: 
  - `cd ../etl`
  - `CH_HOST='localhost:8123' python run_migrations.py`
3. Run client, api and metrics exporter:
  - `cd ../infrastructure`
  - `docker-compose up`

*Note*: supported systems - linux only bacause of issues with Docker for Mac and host network mode.
