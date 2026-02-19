# Setting up Airflow, Hadoop, Kafka, and Spark using Docker for Data Engineering (NaQT)

This repository contains Docker configurations for setting up and running Airflow, Hadoop, Kafka, and Spark in a containerized environment. Follow the steps below to get started.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Folder Structure

```
.
├── airflow-docker/
│   ├── docker-compose.yaml
│   ├── config/
│   │   └── airflow.cfg
│   ├── dags/
│   ├── logs/
│   └── plugins/
├── hadoop-docker/
│   └── docker-compose.yml
├── kafka-docker/
│   └── docker-compose.yml
├── spark-docker/
│   └── docker-compose.yml
└── README.md
```

## Services Overview

### 1. Airflow

Apache Airflow is a platform to programmatically author, schedule, and monitor workflows.

- **Configuration**: The Airflow configuration file is located at `airflow-docker/config/airflow.cfg`.
- **DAGs**: Place your DAG files in the `airflow-docker/dags/` directory.
- **Logs**: Logs are stored in the `airflow-docker/logs/` directory.
- **Plugins**: Custom plugins can be added to the `airflow-docker/plugins/` directory.

#### Steps to Set Up Airflow:

1. Navigate to the `airflow-docker` directory:
   ```bash
   cd airflow-docker
   ```
2. Start the Airflow services using Docker Compose:
   ```bash
   docker-compose up -d
   ```
3. Access the Airflow web interface at [http://localhost:8080](http://localhost:8080).

### 2. Hadoop

Apache Hadoop is a framework for distributed storage and processing of big data.

#### Steps to Set Up Hadoop:

1. Navigate to the `hadoop-docker` directory:
   ```bash
   cd hadoop-docker
   ```
2. Start the Hadoop services using Docker Compose:
   ```bash
   docker-compose up -d
   ```
3. Access the Hadoop web interface at [http://localhost:9870](http://localhost:9870).

### 3. Kafka

Apache Kafka is a distributed event streaming platform.

#### Steps to Set Up Kafka:

1. Navigate to the `kafka-docker` directory:
   ```bash
   cd kafka-docker
   ```
2. Start the Kafka services using Docker Compose:
   ```bash
   docker-compose up -d
   ```
3. Kafka will be running on the default port `9092`.

### 4. Spark

Apache Spark is a unified analytics engine for large-scale data processing.

#### Steps to Set Up Spark:

1. Navigate to the `spark-docker` directory:
   ```bash
   cd spark-docker
   ```
2. Start the Spark services using Docker Compose:
   ```bash
   docker-compose up -d
   ```
3. Access the Spark web interface at [http://localhost:8081](http://localhost:8081).

## Stopping the Services

To stop any of the services, navigate to the respective directory and run:

```bash
docker-compose down
```

## Notes

- Ensure that the required ports (e.g., 8080, 9870, 9092) are not being used by other applications on your system.
- You may need to adjust the configurations in the respective `docker-compose.yml` and configuration files to suit your environment.

## License

This project is licensed under the MIT License.
