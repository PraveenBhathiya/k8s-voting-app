# 🗳️ Voting App on Kubernetes

This project demonstrates how to deploy a simple microservices-based **Voting App** on a Kubernetes cluster. The app consists of multiple components like frontend, backend, Redis, PostgreSQL, and a worker service — all containerized and orchestrated with Kubernetes.

## 📦 Tech Stack

- Docker
- Kubernetes
- Redis (Queue)
- PostgreSQL (Database)
- Python, Node.js
- KubeCTL (CLI)

## 🧱 App Architecture

- `voting-app` – Frontend for users to vote between two options
- `redis` – Message broker to queue votes
- `worker` – Backend processor to read from Redis and store in Postgres
- `postgres` – Stores the final vote counts
- `result-app` – Frontend to display the voting results

## 📁 Project Structure

```bash
.
├── postgres-deploy/
│   ├── postgres-pod.yaml
│   └── postgres-service.yaml
├── redis-deploy/
│   ├── redis-pod.yaml
│   └── redis-service.yaml
├── voting-app-deploy/
│   ├── voting-app-pod.yaml
│   └── voting-app-service.yaml
├── result-app-deploy/
│   ├── result-app-pod.yaml
│   └── result-app-service.yaml
├── worker-app-deploy/
│   ├── worker-app-pod.yaml
└── README.md
