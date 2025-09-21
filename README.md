# docker-aide-image
This repo contains the docker image that support packages of AI/ML, data engineering, data analyst and model training.


# 🐳 AI/ML + Data Engineering Docker Environment

This repository provides a **lightweight but powerful Docker environment** for
AI/ML research and Data Engineering projects. It includes:

- Python 3.10 (slim base)
- JupyterLab
- AI/ML libraries (TensorFlow, PyTorch, scikit-learn, XGBoost, LightGBM, OpenCV)
- Data Engineering tools (dbt, SQLAlchemy, Snowflake, PyArrow)
- Cloud SDKs (AWS boto3, Azure Blob, Databricks CLI, GCP Storage)

---

## ⚡ Prerequisites

- Install [Docker](https://docs.docker.com/get-docker/) on your system
- (Optional) Install [Docker Compose](https://docs.docker.com/compose/)

Check Docker is running:
On terminal run ->
docker --version
docker system info


### Download or clone this repository on your local machine

## Run the docker image
docker build -t ai-de-env:latest .

## Run the container
docker run -it -p 8888:8888 -v $(pwd):/workspace ai-de-env:latest
