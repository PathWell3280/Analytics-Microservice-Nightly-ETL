# Analytics & ETL Service

## Overview
This service ingests raw health-event data, computes nightly aggregated statistics (Spark ETL), ensures k-anonymity (k ≥ 15) for PHIPA §13 compliance, and exposes those aggregates via a FastAPI HTTP API.

## Prerequisites
- Python 3.12
- Java 8+ (for PySpark)
- Apache Spark 3.5 installed or available via `pyspark`
- Access to input data source (e.g., S3, HDFS, or local filesystem)

## Installation
```bash
git clone <repo-url>
cd <repo>
python3.12 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
