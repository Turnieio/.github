# Turnieio

**Turnieio** is an interactive tournament scoreboard application designed for real-time updates by multiple users simultaneously. It supports climbing (Bouldering and Lead) and Teamfight Tactics (TFT) tournaments.

---

## Features

- **Real-time updates** using WebSockets
- **Supported tournaments:**
    - **Climbing (Bouldering & Lead):**
        - **Scoreboard:** displays players and their scoresheets; scores can be updated live
        - **Leaderboard:** tracks points gathered by players for each boulder and total points
    - **TFT (Teamfight Tactics):** single scoreboard, points updated per stage and day, sorted by highest points
- **Tournament management:**
    - Index page lists tournaments
    - `/create` endpoint allows creating new tournaments
- **Microservices architecture** using Kubernetes/Docker
- **Frontend:** Angular + Redux
- **Backend:** Spring Boot
- **Database:** MongoDB

---

## Project Components

Turnieio consists of 5 main components:

1. **MongoDB** – stores tournament and scores data
2. **turnieio-gateway** – routes all requests to the correct service
3. **turnieio-tournament** – handles tournament creation and management
4. **turnieio-scoreboard** – manages score updates and WebSocket connections
5. **turnieio-frontend** – Angular frontend for interacting with tournaments

---

## Deployment

Turnieio is ready for **Kubernetes deployment**:

1. Apply the deployment file (can be found in deployments repository):
   ```bash
   kubectl create -f turnieio-deployment.yaml

2. Access the application at: `http://localhost:30080`

---

## Tech Stack

- **Frontend:** Angular + Redux
- **Backend:** Spring Boot
- **Database:** MongoDB
- **Real-time updates:** WebSockets
- **Deployment:** Docker + Kubernetes

---

## Roadmap / TODO

- User accounts and logging
- Frontend visual improvements
- Add more tournament types
- Features like deleting tournaments or editing scoreboards
- Persistent Volume Claim (PVC) to keep DB data on redeployment

---

