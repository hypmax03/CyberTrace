# CyberTrace - API Reference

## Endpoints Overview

All REST API endpoints are served under `/api` in the web application or dedicated service gateways.

### Threat Intelligence & IOCs
- `GET /api/threats` - Retrieve a paginated list of recorded threats and IOCs.
- `POST /api/threats` - Ingest a new IOC or threat report.
- `GET /api/threats/:id` - Detailed metadata and correlation history for a specific threat entity.

### Incidents
- `GET /api/incidents` - List active and historical security incidents.
- `POST /api/incidents` - Create and trigger an incident response tracking thread.
- `PATCH /api/incidents/:id` - Update status, severity, or assigned analyst.

### Health & Telemetry
- `GET /api/health` - Health check status.
