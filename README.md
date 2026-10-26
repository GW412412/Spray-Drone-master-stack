# Spray Drone Master Stack

> **This repository has moved into [flight-stack](https://github.com/GW412412/flight-stack).** Please work there. Everything here was copied, unedited, into [flight-stack/reference/spray-drone-master-stack](https://github.com/GW412412/flight-stack/tree/main/reference/spray-drone-master-stack) (see [pull request #21](https://github.com/GW412412/flight-stack/pull/21)). This repository stays available so existing links keep working, and its files are kept for reference only. flight-stack's [docs/DECISIONS.md](https://github.com/GW412412/flight-stack/blob/main/docs/DECISIONS.md) is the master record.

Private project repository for the local-AI spot-spraying drone software stack.

## Project status

**Planning and validation stage.** This repository does not yet contain an operational flight-control or spray-control implementation. Do not connect it to a live vehicle or enable actuation on the strength of these documents alone.

## Start here

1. Read [the master reference](docs/MASTER_PLAN.md).
2. Follow [agent instructions](AGENTS.md) before changing files.
3. Review [architecture](docs/ARCHITECTURE.md), [requirements](docs/REQUIREMENTS.md), [interfaces](docs/INTERFACES.md), and [safety case](docs/SAFETY_CASE.md).
4. Read the [MAVLink Router and MAVProxy setup guide](docs/MAVLINK_ROUTING.md) before adding telemetry endpoints.
5. Run the [software-only dry-run](simulation/README.md) before moving toward SITL.

The master reference preserves the project's existing decisions and explicitly identifies unresolved engineering questions. It is a planning document, not a certification or proof of safe operation.
