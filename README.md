# ETL Pipeline for Weather Data 🌦️

## Project Overview

This project demonstrates how to build a scalable **ETL (Extract, Transform, Load) pipeline** using **Apache Airflow**, **Astro CLI**, **Pandas**, and **SQLite**.  
The pipeline extracts weather data from a public API, transforms the raw data into structured formats, and loads it into a local SQLite database for easy access by internal analytics teams.

It was developed to replicate real-world orchestration, task scheduling, and data engineering workflows in a **Dockerized environment**.

## Key Features

- **Extraction**: Pulls weather data from a public API
- **Transformation**: Cleans and structures data using **Pandas**
- **Loading**: Stores the transformed data into a **SQLite database**
- **Orchestration**: Workflow managed and scheduled using **Apache Airflow**
- **Deployment**: Runs seamlessly inside a **Docker container** using **Astro CLI**
- **Modularity**: Designed using a modular **DAG (Directed Acyclic Graph)** structure for scalability and maintainability

## Technologies Used

- **Apache Airflow**  
- **Astro CLI**  
- **Docker**  
- **Python (Pandas, Requests)**  
- **SQLite**  
- **Public Weather API**

## Project Structure

```
etl-weather-airflow-astro/
│
├── dags/
│   ├── weather_etl_dag.py    # DAG definition and task orchestration
│
├── include/
│   ├── scripts/
│       ├── extract.py        # Extract weather data from API
│       ├── transform.py      # Transform and clean data
│       ├── load.py           # Load data into SQLite database
│
├── plugins/
│   └── __init__.py           # (Reserved for future Airflow plugins)
│
├── Dockerfile                # Docker setup (Astro CLI handles orchestration)
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation
```

## How to Run Locally

1. **Install Astro CLI**  
   Follow the [Astro CLI Installation Guide](https://docs.astronomer.io/astro/cli-installation) based on your OS.

2. **Clone this repository**

```bash
git clone https://github.com/GayatriKshirsagar/ETLWeatherAirflowAstro.git
cd ETLWeatherAirflowAstro
```

3. **Start Astro project**

```bash
astro dev start
```

4. **Access the Airflow UI**  
   Navigate to [http://localhost:8080](http://localhost:8080) in your browser.  
   You can trigger the `weather_etl_dag` manually or set it to run on a schedule.

## Learning Highlights

- Building a production-like ETL workflow in a local environment
- Using **Airflow Operators** for task management and dependency handling
- Designing modular scripts for better code organization and reuse
- Handling API data, data cleaning, and efficient loading into databases
- Deploying and orchestrating workflows inside Docker containers

## Acknowledgments

A huge thank you to **Krish Naik** for inspiring and simplifying complex concepts around ETL and Data Engineering.

## License

This project is open-source and free to use for learning purposes. Feel free to fork and customize!

---
