# Stock Market Analysis Pipeline
## 21.7: Airflow Mini Project 

### Necessary Modules 

If you use `pip` installer:
* Yahoo Finance's Python Library: `pip install yfinance`
* Pandas: `pip install pandas`

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
On the command line:
1. `python3 project.py` runs the script
2. `airflow scheduler` schedules the DAG processes in Airflow
3. ` > execution.log` captures the command line execution log