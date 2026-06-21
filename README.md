# 🐳 Docker Network Segmentation

A hands-on cybersecurity project demonstrating secure network segmentation using Docker, Flask, Nginx, PostgreSQL, and Redis.

## 📌 Overview

This project simulates a secure multi-tier application architecture using Docker containers. It demonstrates how frontend and backend services can be isolated on separate Docker bridge networks while communicating through a reverse proxy.

## 🚀 Features

- Multi-container Docker application
- Reverse proxy using Nginx
- Flask web application
- PostgreSQL database
- Redis cache
- Frontend and backend Docker bridge networks
- Network segmentation for improved security

## 🛠 Technologies

- Docker
- Python
- Flask
- Nginx
- PostgreSQL
- Redis

## 📁 Project Structure

```
docker-network-segmentation/
│
├── README.md
├── services/
│   ├── api/
│   │   ├── app.py
│   │   ├── Dockerfile
│   │   └── requirements.txt
│   │
│   └── nginx/
│       └── nginx.conf
│
├── docs/
└── scripts/
```

## 🏗 Architecture

```
                Internet
                    │
                    ▼
              +-----------+
              |   Nginx   |
              +-----------+
                    │
             frontend_net
                    │
                    ▼
              +-------------+
              |  Flask API  |
              +-------------+
                    │
             backend_net
              ┌──────────┐
              ▼          ▼
        PostgreSQL     Redis
```

## ▶️ How to Run

1. Build the Flask image.
2. Create the Docker bridge networks.
3. Start PostgreSQL and Redis containers.
4. Start the Flask API container.
5. Start the Nginx reverse proxy.
6. Open **http://localhost**.

## 🎯 Skills Demonstrated

- Docker containerization
- Docker networking
- Network segmentation
- Reverse proxy configuration
- Flask application deployment
- PostgreSQL and Redis integration
- Cybersecurity architecture principles
