# GPU Server Monitoring

## Overview
This guide is for setting up a monitoring system for a Sony server using Docker, Grafana, and Prometheus.

## Setup Instructions

### Step 1: Environment Configuration
- Copy the contents of `template.env` into a new file named `.env`.
- Ensure that all settings in `.env` are correctly configured.

### Step 2: Starting the Services
- Run the command: `docker-compose up -d`.
- This will start all required services in detached mode.

### Step 3: Accessing Grafana
- Access Grafana by navigating to `<ip>:3000` in your web browser.
- Login to Grafana with your credentials.

### Step 4: Setting up Dashboards
- Refer to `dashboard.txt` for the necessary dashboard IDs.
- Configure dashboards in Grafana using the following:
  - **Nvidia GPU Metrics**: [Nvidia GPU Metrics Dashboard](https://grafana.com/grafana/dashboards/14574-nvidia-gpu-metrics/)
  
  <img src="https://github.com/yspkm/metric/assets/71680670/b79b0846-c73c-4944-b796-30fc00220296" style="width: 50%; height: auto;">

  - **Node Exporter Full**: [Node Exporter Full Dashboard](https://grafana.com/grafana/dashboards/1860-node-exporter-full/)
  
  <img src="https://github.com/yspkm/metric/assets/71680670/fd61066e-5582-4fc9-80b2-326116cd1d12" style="width: 50%; height: auto;">

### Step 5: Teardown
- To stop and remove all containers, use the command: `docker-compose down`.

## Notes
- Ensure you have Docker and Docker Compose installed before beginning.
- Replace `<ip>` with the IP address of your server.

