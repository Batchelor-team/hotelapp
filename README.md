# hotelapp

A .NET 8 web application containerized with Docker. Built from the ASP.NET template and deployed via Docker Compose.

## Architecture

```
┌────────────────────┐
│  Docker Compose    │
│  ┌──────────────┐  │
│  │  .NET 8 App  │  │
│  │  :8080       │──┼──▶ http://localhost:8081
│  └──────────────┘  │
└────────────────────┘
```

The app runs as a single service behind a port mapping (8081 → 8080).

## Quick Start

```sh
docker compose up --build
```

Open http://localhost:8081.

## Deployment

An Azure DevOps pipeline is configured in `deploy.yml` for CI/CD to Azure.
