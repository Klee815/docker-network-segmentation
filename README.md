# Docker Network Segmentation

A cybersecurity project demonstrating secure network segmentation using Docker, Flask, Nginx, PostgreSQL, and Redis.

## Features

- Multi-container Docker application
- Reverse proxy using Nginx
- Flask web application
- PostgreSQL database
- Redis cache
- Frontend and backend Docker bridge networks

## Technologies

- Docker
- Python
- Flask
- Nginx
- PostgreSQL
- Redis

## Architecture

Internet
↓
Nginx
↓
Frontend Network
↓
Flask API
↓
Backend Network
├── PostgreSQL
└── Redis