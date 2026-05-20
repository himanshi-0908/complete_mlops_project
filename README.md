# Vehicle Insurance Prediction - End-to-End MLOps Project

## Overview

This project is a complete production-grade Machine Learning pipeline built using modern MLOps practices.
The system predicts whether a customer is interested in vehicle insurance based on historical customer data.

The project covers the entire ML lifecycle:

* Data Ingestion from MongoDB Atlas
* Data Validation
* Data Transformation
* Model Training
* Model Evaluation
* Model Deployment
* AWS S3 Model Registry
* Docker Containerization
* CI/CD Automation using GitHub Actions
* Deployment on AWS EC2 using Self-Hosted Runner

The goal of this project was not only to train a machine learning model but also to build a scalable and deployable ML system similar to real-world industry workflows.

---

# Tech Stack

## Languages & Libraries

* Python
* Scikit-learn
* Pandas
* NumPy
* Flask

## Database

* MongoDB Atlas

## Cloud Services

* AWS S3
* AWS ECR
* AWS EC2
* AWS IAM

## DevOps & MLOps

* Docker
* GitHub Actions
* CI/CD Pipeline
* Self Hosted Runner

---

# Project Architecture

```text
Data Source (MongoDB Atlas)
        ↓
Data Ingestion
        ↓
Data Validation
        ↓
Data Transformation
        ↓
Model Training
        ↓
Model Evaluation
        ↓
AWS S3 Model Registry
        ↓
Docker Containerization
        ↓
CI/CD using GitHub Actions
        ↓
Deployment on AWS EC2
```

---

# Features

* Modular production-level code structure
* Custom logging and exception handling
* MongoDB integration
* Automated training pipeline
* Model versioning using AWS S3
* Dockerized application
* Automated deployment pipeline
* Real-world MLOps workflow implementation
* End-to-end deployment on AWS cloud

---

# Project Workflow

## 1. Project Initialization

The project structure was generated using a template-based setup.

```bash
python template.py
```

The following files were configured:

* `setup.py`
* `pyproject.toml`

These files help in:

* creating local packages
* dependency management
* clean module imports

---

# Virtual Environment Setup

## Conda Environment

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Verify Installed Packages

```bash
pip list
```

---

# MongoDB Atlas Setup

MongoDB Atlas was used as the cloud database service.

## Steps Performed

* Created MongoDB Atlas project
* Created M0 free cluster
* Configured database user
* Enabled network access
* Generated MongoDB connection string

## Network Access

```text
0.0.0.0/0
```

This allows external access to the database.

---

# Data Upload to MongoDB

The dataset was uploaded using Jupyter Notebook.

## Notebook Tasks

* Load dataset
* Convert dataset into dictionary format
* Push records to MongoDB collection

---

# Logging & Exception Handling

Custom logging and exception handling modules were implemented for better debugging and production monitoring.

## Implemented Files

* `logger/__init__.py`
* `exception/__init__.py`

---

# Exploratory Data Analysis

Performed:

* Data Cleaning
* Missing Value Analysis
* Feature Engineering
* Feature Selection

---

# Data Ingestion Pipeline

The ingestion pipeline performs:

* MongoDB connection
* Data fetching
* Conversion to Pandas DataFrame
* Train-test split
* Artifact generation

## Components Used

* `mongo_db_connection.py`
* `proj1_data.py`
* `data_ingestion.py`

---

# Environment Variable Setup

## MongoDB URL

### Bash

```bash
export MONGODB_URL="your_mongodb_connection_string"
```

### PowerShell

```powershell
$env:MONGODB_URL="your_mongodb_connection_string"
```

---

# Data Validation

The validation pipeline checks:

* Dataset schema
* Missing columns
* Data drift
* Data consistency

## Files Used

* `schema.yaml`
* `main_utils.py`

---

# Data Transformation

Transformation pipeline includes:

* Missing value handling
* Feature encoding
* Feature scaling
* Data preprocessing

---

# Model Training

Implemented:

* Model selection
* Hyperparameter tuning
* Training pipeline
* Model saving

Algorithms were evaluated using:

* Accuracy
* Recall
* Precision
* F1-score

---

# AWS Integration

AWS services were used for model storage and deployment.

## Services Used

### AWS S3

Used as:

* Model Registry
* Artifact Storage

### AWS ECR

Used to:

* Store Docker images

### AWS EC2

Used to:

* Deploy application

---

# Dockerization

The application was containerized using Docker.

## Files

* `Dockerfile`
* `.dockerignore`

## Build Docker Image

```bash
docker build -t vehicle-project .
```

## Run Docker Container

```bash
docker run -p 5080:5080 vehicle-project
```

---

# CI/CD Pipeline

Implemented complete CI/CD automation using:

* GitHub Actions
* Self Hosted Runner
* AWS EC2

## Workflow

```text
Code Push
    ↓
GitHub Actions Trigger
    ↓
Docker Image Build
    ↓
Push Image to AWS ECR
    ↓
Pull Image on EC2
    ↓
Deploy Updated Container
```

---

# Self Hosted Runner Setup

GitHub self-hosted runner was configured on EC2 instance.

This enables:

* automatic deployment
* continuous integration
* continuous delivery

---

# Deployment

The application is deployed on AWS EC2.

## Application Access

```text
http://<EC2-PUBLIC-IP>:5080
```

## Training Endpoint

```text
/training
```

This route triggers the complete training pipeline.

---

# Project Structure

```text
├── artifacts
├── config
├── notebook
├── src
│   ├── components
│   ├── configuration
│   ├── constants
│   ├── data_access
│   ├── entity
│   ├── exception
│   ├── logger
│   ├── pipeline
│   ├── utils
├── templates
├── static
├── app.py
├── demo.py
├── Dockerfile
├── requirements.txt
├── setup.py
├── pyproject.toml
```

---

# Key Learnings

Through this project, I gained hands-on experience in:

* Production-level ML system design
* End-to-end MLOps workflow
* Cloud deployment using AWS
* CI/CD automation
* Docker containerization
* MongoDB integration
* Model lifecycle management

---

# Future Improvements

* Kubernetes deployment
* MLflow integration
* Automated monitoring
* Drift detection
* Model retraining automation
* Unit & integration testing

---

# Author

## Himanshi Rana

Machine Learning & MLOps Enthusiast focused on building scalable AI systems and production-grade ML pipelines.
