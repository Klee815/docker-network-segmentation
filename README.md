# 🐳 Docker Network Segmentation

A hands-on cybersecurity project demonstrating secure network segmentation using Docker containers, Nginx, Flask, PostgreSQL, and Redis.

---

## 📌 Overview

This project simulates a secure multi-tier web application using Docker networking. It demonstrates how frontend and backend services can be isolated using separate Docker bridge networks while allowing only authorized communication between containers.

The goal is to practice Docker networking concepts commonly used in cloud infrastructure and cybersecurity environments.

---

## 🚀 Features

- Multi-container Docker application
- Flask web application
- Nginx reverse proxy
- PostgreSQL database
- Redis cache
- Frontend and backend bridge networks
- Network segmentation for improved security
- Container-to-container communication
- Docker image creation using Dockerfile

---

## 🛠 Technologies

- Docker
- Python
- Flask
- Nginx
- PostgreSQL
- Redis

---

## 📁 Project Structure

```
docker-network-segmentation/
│
├── README.md
├── screenshots/
│   ├── docker-desktop.png
│   ├── docker-ps.png
│   ├── flask-app.png
│   └── project-structure.png
│
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

---

## 🏗 Network Architecture

```
                Internet
                    │
                    ▼
             +-------------+
             |    Nginx    |
             +-------------+
                    │
          Frontend Network
                    │
                    ▼
             +-------------+
             |  Flask API  |
             +-------------+
                    │
          Backend Network
              ┌───────────┐
              ▼           ▼
       PostgreSQL      Redis
```

---

## 📸 Screenshots

### Running Containers

![Docker Containers](screenshots/docker-ps.png)

---

### Flask Application

![Flask Application](screenshots/flask-app.png)

---

### Docker Desktop

![Docker Desktop](screenshots/docker-desktop.png)

---

### Project Structure

![Project Structure](screenshots/project-structure.png)

---

## ▶️ Running the Project

### Build the Flask image

```bash
docker build -t flask_api ./services/api
```

### Create Docker networks

```bash
docker network create frontend_net
docker network create backend_net
```

### Start PostgreSQL

```bash
docker run -d --name postgres_db --network backend_net postgres:16-alpine
```

### Start Redis

```bash
docker run -d --name redis_cache --network backend_net redis:7-alpine
```

### Start Flask

```bash
docker run -d --name flask_api_container -p 5000:5000 flask_api
```

### Start Nginx

```bash
docker run -d --name nginx -p 80:80 nginx:alpine
```

---

## 🎯 Skills Demonstrated

- Docker containerization
- Docker bridge networking
- Network segmentation
- Reverse proxy configuration
- Flask application deployment
- PostgreSQL integration
- Redis integration
- Cybersecurity network architecture
- Linux command line
- Git and GitHub workflow

---

## 📚 What I Learned

Through this project I learned how to:

- Build Docker images from a Dockerfile
- Connect containers using Docker bridge networks
- Configure an Nginx reverse proxy
- Deploy a Python Flask application in Docker
- Use PostgreSQL and Redis as backend services
- Apply network segmentation to improve security
- Publish projects using Git and GitHub

---

## 👩‍💻 Author

**Kayoung Lee**

Cybersecurity Student | Western Governors University

GitHub: https://github.com/Klee815
