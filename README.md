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
├── README.md                     # Documentação do projeto
├── requirements.txt              # Dependências Python
├── .gitignore                    # Arquivos e pastas ignoradas pelo Git
├── docker-compose.yml            # Arquivo para subir os containers
├── .env                          # Variáveis de ambiente (não versionar)
├── src/                          # Scripts de ETL
│   ├── extraction.py             # Extrai dados da API CoinGecko
│   ├── transform.py              # Limpa e transforma os dados
│   ├── load.py                   # Carrega os dados no PostgreSQL
│   ├── config.py                 # Configurações e leitura de variáveis
│   └── utils.py                  # Funções auxiliares (ex.: logging)
├── dags/                         # DAGs do Apache Airflow
│   └── crypto_dag.py             # DAG que orquestra o pipeline ETL
└── docs/                         # Documentação e diagramas
    ├── arquitetura.pdf           # Diagrama da arquitetura
    ├── fluxo_de_dados.png        # Diagrama do fluxo de dados
    └── setup_ambiente.md         # Guia de configuração do ambiente

