# Smart City Simulation System

## Overview

This project simulates a smart city environment, generating and processing real-time data from multiple sources such as vehicles, GPS trackers, traffic cameras, weather stations, and emergency services. It aims to provide insights into urban dynamics, facilitating efficient city management and planning.

## Features

- Simulate real-time data generation for vehicles, weather, traffic, GPS, and emergency incidents.
- Stream data processing using PySpark to analyze and store processed information.
- Kafka integration for real-time data messaging.
- Data storage and analysis using AWS S3 and potentially Redshift.

## Prerequisites

- Python 3.6 or higher
- Docker and Docker Compose (for container management)
- Access to an Apache Kafka cluster
- AWS account for S3 and Redshift services

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/dev7878/smart-city-data-pipeline.git
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Environment

Fill in the necessary AWS credentials and Kafka server details in `config.py`.

## Usage

### Starting the Simulation

Run the main script to start generating and processing data:

```bash
python main.py
```

### Processing Data with Spark

Execute the Spark job to process streaming data:

```bash
spark-submit spark-city.py
```

## Docker Setup

Use the `docker-compose.yml` file to set up the Kafka and Spark environments, ensuring a seamless integration for data processing.

```bash
docker-compose up -d
```

## Data Schema

Detailed data schemas for each domain (vehicle, GPS, traffic, weather, and emergency) are defined in `spark-city.py`.

## Security Considerations

Ensure that AWS credentials and Kafka connection details are securely stored and not exposed in public repositories.
