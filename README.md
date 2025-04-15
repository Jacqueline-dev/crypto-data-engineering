# ₿  Crypto ETL Pipeline with Airflow, PostgreSQL, Docker, and Power BI


## 📌 Overview

This project is a data engineering pipeline focused on cryptocurrency. It extracts data from the public CoinGecko API, transforms it using Python and Pandas, stores it in SQLite, orchestrates processes with Apache Airflow, and provides interactive dashboards via Power BI.

The entire solution is containerized using Docker to ensure portability and consistency across different environments.

## 🔧 Technologies Used

- **Python** – ETL scripting and automation
- **Pandas** – Data cleaning and transformation
- **CoinGecko API** – Public crypto market data
- **PostgreSQL** – Relational database for storage
- **Apache Airflow** – Pipeline orchestration and scheduling
- **Docker** – Containerization of the whole stack
- **Power BI** – Data visualization
- **VS Code + WSL (Ubuntu)** – Development environment

## 🔁 Pipeline Architecture

- **Ingestion:** Python scripts call the CoinGecko API to fetch real-time crypto data.
- **Transformation:** Data is cleaned and shaped using Pandas.
- **Loading:** Transformed data is loaded into a PostgreSQL database.
- **Orchestration:** Apache Airflow schedules and monitors ETL jobs.
- **Visualization:** Power BI connects to the database to create dashboards.

## 📂 Project Structure

```bash
crypto-etl-pipeline/
├── README.md                     # Project documentation
├── requirements.txt              # Python dependencies
├── .gitignore                    # Git ignored files and folders
├── docker-compose.yml            # File to spin up containers
├── .env                          # Environment variables 
├── src/                          # ETL scripts
│   ├── extraction.py             # Extracts data from CoinGecko API
│   ├── transform.py              # Cleans and transforms data
│   ├── load.py                   # Loads data into PostgreSQL
│   ├── config.py                 # Configurations and variable reading
│   └── utils.py                  # Auxiliary functions
├── dags/                         # Apache Airflow DAGs
│   └── crypto_dag.py             # DAG that orchestrates the ETL pipeline
└── docs/                         # Documentação e diagramas
    ├── arquitetura.pdf           # Architecture diagram
    ├── fluxo_de_dados.png        # Data flow diagram
    └── setup_ambiente.md         # Environment setup guide

