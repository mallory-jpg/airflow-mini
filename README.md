# Stock Market Analysis Pipeline
## Analysis

### Necessary Modules 

If you use `pip` installer:
* Yahoo Finance's Python Library: `pip install yfinance`
* Pandas: `pip install pandas`

This project also utilizes the following built-in Python libraries:
* os
* datetime (date)

### Goals
* Orchestrate a pipeline with Airflow
* Execute in parallel on different datasets
* Query datasets

### Source Data Schema

|Column    | Type   |
|----------|--------|
|date time |STRING  |
|open      |DECIMAL |
|high      |DECIMAL | 
|low       |DECIMAL | 
|close     |DECIMAL |  
|adj close |DECIMAL |
|volume    |DECIMAL |

* *high* : highest price within the time interval
* *low* : lowest price within the time interval
* *close* : the last price of the time interval

### Running the code
1. Ensure `project.py` in `/airflow/dags` directory
2. Run `docker run --platform linux/amd64 -d -p 8081:8081 -v <location of /airflow/dags folder> puckel/docker-airflow webserver` on command line, which runs the DAGs in the folder. 

*Note*: I've included the `--platform` flag because my Macbook has the M1 processing chip which necessitates a linux/amd64 platform

## Project Log Analysis
Analyze log files for Airflow workflow.
### Necessary Libraries
* Path: `from pathlib import Path`
* os: `import os`
### Running the Code
1. Ensure `log_analyzer.py` in `/airflow/dags` directory
2. Run `docker run --platform linux/amd64 -d -p 8081:8081 -v <location of /airflow/dags folder> puckel/docker-airflow webserver`
