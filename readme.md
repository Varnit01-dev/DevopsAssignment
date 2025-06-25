# 🚀 DevOps Internship Assignment – NGINX Reverse Proxy with Docker Compose

This project sets up a Docker-based system with two backend services and an NGINX reverse proxy. It uses Docker Compose to orchestrate all services, with logging, path-based routing, and health checks.

---

## 📁 Project Structure
.
├── docker-compose.yml
├── nginx/
│ ├── nginx.conf
│ └── Dockerfile
├── service_1/ # Go application
│ ├── main.go
│ ├── Dockerfile
│ └── README.md
├── service_2/ # Python Flask application
│ ├── app.py
│ ├── Dockerfile
│ └── README.md
└── README.md # This file


---

## ⚙️ Setup Instructions

### 🔧 Prerequisites:
- Docker
- Docker Compose

### 🔥 Start All Services:

```bash
docker-compose up --build

## Access the Services
## Once running, access them via browser or curl:

# Route	Description
# http://localhost:8080/service1/ping	Ping endpoint (Go app)
# http://localhost:8080/service1/hello	Hello from Service 1
# http://localhost:8080/service2/ping	Ping endpoint (Flask app)
# http://localhost:8080/service2/hello	Hello from Service 2

# Bonus Implemented
# ✔️ Path-based routing via NGINX

# ✔️ Request logging with timestamp and user-agent in access.log

# ✔️ Health checks defined in docker-compose.yml

# ✔️ Modular Docker setup with separate Dockerfiles per service

# ✔️ Bridge networking used (default in Docker Compose)

