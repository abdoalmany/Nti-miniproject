# Nti-miniproject
# Mini Project: Deploying Prometheus on Cloud

## Objective

Deploy a monitoring setup using Prometheus on cloud infrastructure with Terraform and Ansible.

---

## Infrastructure Setup (Terraform)

* Provision 3 virtual machines:

  1. Prometheus server
  2. Container registry host
  3. Application host

* Configure VM specifications as required.

* Open necessary ports for:

  * Prometheus
  * Node Exporter

* Retrieve the IP addresses of the machines:

  * Preferred: Automated method (script, CI/CD, dynamic inventory)
  * Alternative: Manual retrieval

---

## Prometheus Architecture Setup (Ansible)

### VM 1: Prometheus Server

* Install Prometheus
* Install Node Exporter

### VM 2: Container Registry

* Install Docker
* Install cAdvisor
* Install Nginx
* Install Apache (httpd)

### VM 3: Application Host

* Deploy an application of choice
* Integrate Prometheus client library to expose application metrics

---

## Monitoring Configuration

* Configure Prometheus to monitor:

  * Containers on VM 2
  * Application on VM 3

* Secure communication between Prometheus and exporters using:

  * Authentication
  * SSL certificates

---

## Validation and Monitoring

### Prometheus Explorer

* Execute metric queries to confirm successful installation and data collection

### Grafana Dashboards

* Create custom dashboards based on user roles

### Alerts

* Define alert rules:

  * Alert if the application is down for more than 15 seconds
  * Notify through selected communication channel (e.g., Microsoft Teams, Slack)

---
