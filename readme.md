#  DevOps Internship Assignment – NGINX Reverse Proxy with Docker Compose

This project sets up a Docker-based system with two backend services and an NGINX reverse proxy. It uses Docker Compose to orchestrate all services, with logging, path-based routing, and health checks.


##  Setup Instructions

###  Prerequisites:
- Docker
- Docker Compose

###  Start All Services:

```bash
docker-compose up --build
```

## Access the Services
## Once running, access them via browser or curl:

# Route	Description
# http://localhost:8080/service1/ping	Ping endpoint (Go app)
# http://localhost:8080/service1/hello	Hello from Service 1
# http://localhost:8080/service2/ping	Ping endpoint (Flask app)
# http://localhost:8080/service2/hello	Hello from Service 2

# Bonus Implemented
#  Path-based routing via NGINX

#  Request logging with timestamp and user-agent in access.log

#  Health checks defined in docker-compose.yml.

#  Modular Docker setup with separate Dockerfiles per service.

#  Bridge networking used.

# Logs
# You can view logs using:

 #bash


```bash
docker-compose logs nginx
```

**Example NGINX log format:**
```
127.0.0.1 - [23/Jun/2025:10:45:21 +0000] "GET /service1/ping" 200 39 "curl/7.68.0"
```