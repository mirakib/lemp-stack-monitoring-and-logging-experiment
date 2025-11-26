# LEMP Stack Monitoring and Logging Experiment

This project demonstrates a production-grade strategy for achieving full observability over a Dockerized LEMP application. The architecture is built on the modern `P-G-L` stack:

  - **Monitoring:** `Prometheus` scrapes system and service metrics exposed by `cAdvisor` (for container health).

  - **Visualization:** `Grafana` serves unified dashboards for analyzing application performance and resource utilization.

  - **Logging:** `Loki` stores raw logs shipped by Promtail, allowing engineers to correlate metrics alerts with detailed log events, drastically reducing Mean Time To Resolution (MTTR). This setup ensures robust performance tracking and simplified troubleshooting.
  
## Components
- **Docker**: Containerization platform to run the LEMP stack and monitoring tools.
- **LEMP Stack**: Consists of Linux, Nginx, MySQL, and PHP.
- **Prometheus**: Monitoring system that collects metrics from cAdvisor.
- **Grafana**: Visualization tool for creating dashboards based on Prometheus data.
- **Loki**: Log aggregation system that stores logs collected by Promtail.
- **cAdvisor**: Container Advisor that provides container resource usage and performance characteristics.
- **Promtail**: Log shipping agent that collects logs from Docker containers and sends them to Loki.
- **Docker Compose**: Tool for defining and running multi-container Docker applications.
