# Rsyslog Server Deployment with Docker Compose

This repository contains a simple Docker Compose setup for deploying an Rsyslog server with Telegraf and InfluxDB.

InfluxDB is used as a datasource for grafana.

<details>
<summary>How configure grafana</summary>

### Add a data source
- Hover over the settings cog in the sidebar and click Data sources
- Click "Add new data source"
- Find influxDB from the list
- Basic Configuration Parameters:
    - Name: whatever you want
    - Query Language: InfluxQL
    - URL: http://\<IP ADDRESS OF COMPUTER HOSTING CONTAINERS\>:8086/
- Custom HTTP Headers:
    - Header: Authorization
    - Value (make sure you enter this value **EXACTLY, including Token**): Token veryverysecuretoken
- InfluxDB Details:
    - Database: GOLDENBYTE-BUCKET
</details>


Rsyslog is a powerful logging system used for managing and forwarding log messages in a network.

The initial concept dervied from here: https://nwmichl.net/2020/03/15/telegraf-influxdb-grafana-as-syslog-receiver/
