# 2. Secured and Monitored Web Infrastructure

## Components Added
- **3 Firewalls**: One per server to filter incoming/outgoing traffic.
- **1 SSL Certificate**: Enables secure HTTPS traffic to www.foobar.com.
- **3 Monitoring Agents**: One per server for performance and health tracking.

## Why These Additions
- **Firewalls**: Prevent unauthorized access, reduce attack surface.
- **HTTPS (SSL)**: Encrypts user data and protects against MITM attacks.
- **Monitoring**: Tracks server health, detects outages and performance issues.

## Monitoring Details
- **Monitoring Tool**: (e.g., Sumo Logic)
- **Data Collected**: CPU, memory, disk usage, logs, web requests
- **Use Case**: To monitor QPS (Queries Per Second), use Nginx access logs or app metrics.

## Infrastructure Issues
- **SSL Termination at Load Balancer**: If traffic is not encrypted to backend, it's a security risk.
- **Single MySQL Write Node**: If it fails, app cannot write data.
- **Identical Servers**: Difficult to scale specific services independently.

## Diagram
![Secured and Monitored Web Infra](./img/secured-monitored-infra.png)
