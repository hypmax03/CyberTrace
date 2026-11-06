# CyberTrace - Architecture

## System Overview
CyberTrace is structured as a monorepo containing web applications, services, and shared libraries.

```mermaid
graph TD
    Client["Next.js Web Frontend (apps/web)"]
    API["Next.js Server Actions / Route Handlers"]
    DB[(Database / Cache)]
    Ingest["Telemetry & IOC Ingestion Engine"]

    Client --> API
    API --> DB
    Ingest --> DB
```

## Components
- **apps/web**: Next.js (App Router) modern web application styled with Tailwind CSS.
- **Data Layer**: Relational/Document storage for telemetry logs and graph associations.
- **Analysis Pipeline**: Pattern matching and correlation algorithms for threat tracing.
