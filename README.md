# Bot

Some reference code for a FastAPI + React / Typescript project.

## Getting Started

Install the package (backend + worker):

```bash
pip install -e '.[dev]'
```

Build a local config file:

```bash
python configs/build.py local ~/.config/bot.yaml
```

Start the frontend and backend processes:

```bash
make start-frontend
make start-backend
```

## Infrastructure

- Frontend
  - Web: React
  - Mobile: React Native
- Backend: FastAPI
  - Database: PostgreSQL (Aurora Serverless on AWS)
  - Model inference: The FastAPI endpoint queues samples through SQS, which are then processed by ECS tasks.
