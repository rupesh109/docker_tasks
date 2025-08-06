# 🐳 Docker Swarm Cronjobs – Task #13

## 📌 Introduction

Docker Swarm is a native clustering and scheduling tool for Docker containers. While Swarm lacks native support for cronjobs (like Kubernetes does), we can simulate scheduled tasks using:

- Linux cron and `docker service update --force`
- Third-party tools like [`crazy-max/swarm-cronjob`](https://github.com/crazy-max/swarm-cronjob)

This document demonstrates how to simulate cronjobs inside a Docker Swarm cluster using the Linux `cron` daemon.

---

## ⚙️ Environment Setup

### ✅ Platform Used:
- [Play with Docker](https://labs.play-with-docker.com)
- Alpine Linux environment
- Docker version: `Docker 24+`

---

## 🛠️ Step-by-Step Guide

### 🔹 1. Start Docker Swarm

```bash
docker swarm init --advertise-addr 192.168.0.19
