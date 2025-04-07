# ₿  Crypto ETL Pipeline with Airflow, PostgreSQL, Docker, and Power BI

![Architecture](https://github.com/user-attachments/assets/890fe7ea-d484-4240-9665-d661556c59bb)

## 📌 Overview

This project is a data engineering pipeline focused on cryptocurrency. It extracts data from the public CoinGecko API, transforms it using Python and Pandas, stores it in PostgreSQL, orchestrates processes with Apache Airflow, and provides interactive dashboards via Power BI.

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
├── .gitignore                    # Files and folders ignored by Git
├── src/                          # ETL scripts and utilities
│   ├── extraction.py             # Extracts data from the CoinGecko API
│   ├── transform.py              # Cleans and transforms the data
│   ├── load.py                   # Loads data into PostgreSQL
│   ├── config.py                 # Configuration (no secrets)
│   └── utils.py                  # Utility functions (e.g., logging)
├── dags/                         # Apache Airflow DAGs
│   └── crypto_dag.py             # Main DAG for orchestrating the ETL
└── docs/                         # Documentation and architecture diagrams
    ├── arquitetura.pdf           # Architecture overview (PDF)
    ├── fluxo_de_dados.png        # Data flow diagram
    └── setup_ambiente.md         # Environment setup guide
