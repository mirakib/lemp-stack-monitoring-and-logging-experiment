<div style="display: flex; align-items: center; gap: 10px;">
  <img src="https://skillicons.dev/icons?i=linux,nginx,mysql,php,docker,prometheus,grafana" style="height: 40px;"/>
</div>

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

## Features
- Full observability over a Dockerized LEMP application.
- Real-time monitoring and alerting.
- Centralized logging for easier troubleshooting.
- Pre-configured Grafana dashboards for quick insights.
- Easy setup with Docker Compose.
- Modular architecture for easy customization and extension.

## Setup Instructions 
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/mirakib/lemp-stack-monitoring-and-logging-experiment.git
      ```
2. **Navigate to the Project Directory**:
    ```bash
    cd lemp-stack-monitoring-and-logging-experiment
    ```
3. **Start the Docker Containers**:
   ```bash
   docker-compose up -d
   ```
4. **Access the Services**:
   - LEMP Application: `http://localhost:80`
   - Grafana Dashboard: `http://localhost:3000` (credentials: Look in the .env file)
   - Prometheus UI: `http://localhost:9090`
   - Loki UI: `http://localhost:3100`
   - cAdvisor UI: `http://localhost:8081`

## Screenshots

**Web Page**  

![Web Page](/Images/web-page.png)

**Prometheus UI**

![Prometheus UI](/Images/prom-ui.png)

**MySQL Exporter**

![MySQL Exporter](/Images/mysql-exporter.png)
**CAdvisor**

![CAdvisor](/Images/cadvisor.png)

**Node Exporter**

![Node Exporter](/Images/node-exporter.png)

**Nginx**

![Nginx](/Images/nginx-exporter.png)