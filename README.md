# Data Observability & Lineage with OpenLineage + Marquez

## Overview
A comprehensive observability platform for data pipelines. Tracks data lineage end-to-end, monitors freshness and volume anomalies, and integrates quality metrics — all visualized in Grafana dashboards. The layer that makes pipelines production-grade.

## Architecture
- **Lineage Tracking**: OpenLineage events emitted from Airflow, Spark, and dbt jobs captured by Marquez
- **Freshness Monitoring**: Custom Airflow sensors that track table update timestamps and alert on staleness
- **Volume Monitoring**: Row count tracking with anomaly detection (Z-score) for unexpected drops/spikes
- **Quality Integration**: Great Expectations results fed into the observability dashboard alongside lineage
- **Visualization**: Grafana dashboards showing lineage graphs, freshness SLAs, volume trends, and quality scores

## Tech Stack
- OpenLineage (lineage event standard)
- Marquez (lineage metadata store + UI)
- Apache Airflow 2.x (with OpenLineage integration)
- Great Expectations (quality metrics)
- Grafana (observability dashboards)
- PostgreSQL (metrics store)
- Docker & Docker Compose

## What This Demonstrates
- Data lineage implementation and visualization
- SLA-based freshness monitoring
- Volume anomaly detection
- Integration of quality, lineage, and monitoring into a single pane of glass
- Production-grade pipeline observability

## Status
🚧 In Development

## Project Structure
├── dags/
│   ├── observability_monitoring_dag.py
│   └── lineage_enrichment_dag.py
├── openlineage/
│   └── custom_extractors/
├── grafana/
│   └── dashboards/
├── monitoring/
│   ├── freshness/
│   └── volume/
├── tests/
├── docker-compose.yml
└── README.md
