# kubernetes-tui

A Pi AI-powered terminal user interface for operating large groups of remotely controlled AI sessions on Kubernetes.

## Vision

`kubernetes-tui` provides a graphical console for Pi sessions that are detached from the operator's local hardware and `/etc` environment. It is intended to make it possible to:

- Spawn and manage roughly 25 to 10,000 Pi AI sessions on a Kubernetes cluster.
- Control sessions remotely through a terminal-native graphical interface.
- Construct, name, organize, and operate groups of sessions.
- Use the same system for software development, incident triage, and parallel investigation.
- Observe session state, workloads, logs, and group-level activity without requiring direct access to each worker's host.

The project is currently a starting point for architecture, interfaces, and implementation. Scale targets are design goals and require staged testing before they can be considered supported deployment sizes.

## Core concepts

- **Session** — an isolated Pi AI runtime with its own lifecycle, workspace, model configuration, and event stream.
- **Group** — a user-defined collection of sessions that can share commands, context, tasks, or operational state.
- **Graphical console** — a TUI presentation layer for session and group control, monitoring, navigation, and triage.
- **Kubernetes control plane** — scheduling, scaling, placement, health, and lifecycle orchestration for session workloads.
- **Hardware-detached runtime** — sessions run independently of the operator's local machine and filesystem, including the local `/etc` configuration.

## Intended uses

- Parallel development and code review
- Fleet-wide debugging and triage
- Reproducible agent workspaces
- Coordinated investigation by session groups
- Remote operation from a laptop, workstation, or terminal-only environment

## Status

Early design and implementation phase. APIs, workload isolation, persistence, authentication, authorization, model-provider integration, and the supported scale envelope are not finalized.

## Future target repositories

These are planned companion or integration targets, not current dependencies:

- [`incoming-specs-aka_specifications_for_agentic_coding`](https://github.com/webdawg/incoming-specs-aka_specifications_for_agentic_coding) — incoming specifications for agentic coding work.
- `oag-space_telemetry` — planned repository for space-telemetry data about satellite constellations. The repository has not been created or located yet.
- `oag-challenges` — foundational delivery tests that exercise the entire OAG stack end to end. These tests are intended to force the stack to work as a real integrated system, rather than validating isolated components only. The repository has not been created or located yet.

## License

Licensed under the [GNU Affero General Public License v3.0 or later](LICENSE) (`AGPL-3.0-or-later`).
