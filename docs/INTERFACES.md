# Interfaces

**Status:** Contract outline only. Concrete schemas and message definitions must be reviewed before implementation.

## Common envelope
Every internal request should carry:
- `request_id`: unique identifier.
- `created_at` and `expires_at`: timestamps with explicit clock basis.
- `source_component` and `schema_version`.
- `authority_generation`: generation captured when the request was authorized.
- `correlation_id`: trace identifier across components.

Reject expired, malformed, duplicate, replayed or wrong-generation requests. Do not rely on natural-language prompt instructions as authorization.

## Initial logical interfaces
- **Intent → mission manager:** structured proposal only; no direct actuation.
- **Telemetry → gateway/mission manager:** timestamped values plus validity, age and source.
- **Mission manager → gateway:** proposed action with bounded parameters and expiry.
- **Gateway → MAVLink adapter:** only validated, allowed commands with current authority.
- **Target servo → gateway:** bounded correction proposal; gateway rechecks mode, freshness and limits.
- **Spray request → onboard spray gate:** uniquely identified, expiring request; the gate independently verifies onboard conditions and permission.
- **All components → audit log:** state transitions, rejected requests, faults and outcomes without credentials.

This document does not yet define wire formats, units, MAVLink type masks, coordinate frames or timing thresholds. Those must be explicit before hardware actuation is permitted.
