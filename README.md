# n8n Setup on Mac

Production-style local n8n development environment using:

- Docker Compose
- PostgreSQL
- Redis
- macOS (Apple Silicon / M1)
- VSCode

This repository documents the setup process, infrastructure configuration, and local development workflow for running n8n professionally on macOS.

---

# Project Goal

This project aims to create a scalable and reproducible local n8n environment for:

- AI workflow development
- automation engineering
- API integrations
- webhook testing
- client demonstrations
- infrastructure experimentation

The setup is designed to mimic a lightweight production architecture while remaining fully local for development and testing.

---

# Technology Stack

| Layer                   | Technology            |
| ----------------------- | --------------------- |
| Workflow Automation     | n8n                   |
| Containerization        | Docker                |
| Container Orchestration | Docker Compose        |
| Database                | PostgreSQL 16         |
| Queue / Cache           | Redis 7               |
| Development Environment | VSCode                |
| Runtime                 | Node.js 20 LTS        |
| Operating System        | macOS (Apple Silicon) |

---

# Architecture

```text
macOS
│
├── Docker Desktop
│
├── n8n Container
│
├── PostgreSQL Container
│
├── Redis Container
│
└── Persistent Docker Volumes
```

---

# Project Structure

```text
n8n-setup-mac/
│
├── docker/
│   └── docker-compose.yml
│
├── scripts/
│   └── check-n8n-readiness.sh
│
├── screenshots/
│
├── docs/
│
├── workflows/
│
├── diagrams/
│
└── README.md
```

---

# Features

- Local n8n setup using Docker Compose
- PostgreSQL database integration
- Redis integration
- Persistent Docker volume storage
- macOS Apple Silicon support
- Infrastructure documentation
- GitHub version-controlled setup
- Scalable local development environment

---

# Pre-flight Check

Before starting the project, run:

```bash
./scripts/check-n8n-readiness.sh
```

This verifies:

- Git
- Node.js
- npm
- Docker
- VSCode CLI
- n8n compatibility

---

# Recommended Requirements

| Requirement    | Version                   |
| -------------- | ------------------------- |
| Node.js        | 20 LTS                    |
| Docker Desktop | Latest                    |
| macOS          | Apple Silicon recommended |
| RAM            | 16GB recommended          |

---

# Getting Started

## Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/n8n-setup-mac.git
cd n8n-setup-mac
```

---

## Run Environment Check

```bash
./scripts/check-n8n-readiness.sh
```

---

## Start Docker Infrastructure

```bash
docker compose -f docker/docker-compose.yml up -d
```

---

## Verify Containers

```bash
docker ps
```

Expected containers:

- ai-training-n8n
- ai-training-postgres
- ai-training-redis

---

## Open n8n

```text
http://localhost:5678
```

---

## Stop Infrastructure

```bash
docker compose -f docker/docker-compose.yml down
```

---

# Docker Services

## PostgreSQL

Used as the primary persistent database backend for n8n.

Stores:

- workflows
- execution history
- credentials
- user data
- settings

---

## Redis

Prepared for queue-mode and scalable workflow execution.

Used for:

- queue handling
- temporary memory
- scalable execution architecture

---

## n8n

Main workflow automation platform.

Runs:

- API workflows
- webhook automations
- AI integrations
- scheduling systems
- automation pipelines

---

# Screenshots

## n8n Login Screen

![n8n Login](screenshots/n8n-login.png)

---

## n8n Dashboard

![n8n Dashboard](screenshots/n8n-dashboard.png)

---

# Current Progress

## Core Environment Setup

- [x] GitHub repository setup
- [x] Local project structure created
- [x] VSCode development environment configured
- [x] Docker installed
- [x] Node.js 20 installed
- [x] n8n Docker image installed

---

## Infrastructure Stack

- [x] Docker Compose multi-container setup
- [x] PostgreSQL database integration
- [x] Redis integration
- [x] Persistent Docker volumes configured
- [x] n8n running locally with PostgreSQL backend
- [x] Local development architecture established

---

## Documentation & Version Control

- [x] README documentation created
- [x] Git workflow established
- [x] Progress tracking system created
- [x] Screenshots documented
- [x] Infrastructure setup committed to GitHub

---

# Planned Future Integrations

- Telegram Bot integration
- OpenAI API integration
- Google Calendar integration
- AI workflow orchestration
- Cloudflare Tunnel setup
- Remote webhook testing
- Client demo deployment

---

# Author

Created by Juzantino Junadi
