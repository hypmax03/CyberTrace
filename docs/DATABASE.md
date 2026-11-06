# CyberTrace - Database Design

## Schema Overview

### Entities
1. **ThreatEntity / IOC**
   - `id`: UUID (Primary Key)
   - `type`: `ip` | `domain` | `hash` | `cve` | `url`
   - `value`: String
   - `reputation_score`: Float
   - `first_seen`: Timestamp
   - `last_seen`: Timestamp

2. **Incident**
   - `id`: UUID (Primary Key)
   - `title`: String
   - `description`: Text
   - `severity`: `low` | `medium` | `high` | `critical`
   - `status`: `open` | `investigating` | `mitigated` | `closed`
   - `created_at`: Timestamp
   - `updated_at`: Timestamp

3. **IncidentThreatRelation**
   - `incident_id`: Foreign Key
   - `threat_id`: Foreign Key
   - `association_type`: String (e.g., `observed_source`, `c2_node`, `payload`)
