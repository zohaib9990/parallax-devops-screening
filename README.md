# Parallax Labs DevOps Screening Task

## Overview

This project demonstrates a simple multi-container application using Docker Compose.

- Nginx acts as a reverse proxy.
- Python Flask acts as the backend.
- Requests sent to Nginx are forwarded to the backend.
- The backend returns:

Hello from Backend

## Architecture

Browser
↓
Nginx
↓
Flask Backend

## Network

Docker Compose automatically creates a shared bridge network.

Nginx communicates with the backend using the service name:

backend:5000

## Run

```bash
docker compose up --build
```

Open:

```
http://localhost
```

Expected output:

```
Hello from Backend
```

Stop:

```bash
docker compose down
```
