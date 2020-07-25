# Infrastructure

Running clickhouse and kafka with default settings: `docker-compose -f docker-compose-infrastructure.yml up`

# App

Please put all the necessary apps(client, api, exporter) on the same folder as infrastructure. Then run `docker-compose up`. Be sure that you've run kafka and clickhouse before starting applications.

*Note*: supported systems - linux only bacause of issues with Docker for Mac and host network mode.