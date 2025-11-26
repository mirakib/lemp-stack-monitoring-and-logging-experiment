# lemp-stack-monitoring-and-logging-experiment

This project demonstrates a production-grade strategy for achieving full observability over a Dockerized LEMP application. The architecture is built on the modern P-G-L stack:

  - Monitoring: Prometheus scrapes system and service metrics exposed by cAdvisor (for container health).

  - Visualization: Grafana serves unified dashboards for analyzing application performance and resource utilization.

  - Logging: Loki stores raw logs shipped by Promtail, allowing engineers to correlate metrics alerts with detailed log events, drastically reducing Mean Time To Resolution (MTTR). This setup ensures robust performance tracking and simplified troubleshooting.
