# Stock Market Analysis Pipeline
## 21.7: Airflow Mini Project 

### Necessary Modules 

If you use `pip` installer:
* Yahoo Finance's Python Library: `pip install yfinance`
* Pandas: `pip install pandas`

This project also utilizes:
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

## Running the code
1. Ensure `project.py` in `/airflow/dags` directory
2. Run `docker run --platform linux/amd64 -d -p 8081:8081 -v <location of /airflow/dags folder> puckel/docker-airflow webserver` on command line, which runs the DAGs in the folder. 

*Note*: I've included the `--platform` flag because my Macbook has the M1 processing chip
*Note*: I've run the entire folder, as this DAG was the only one present at the time of this project