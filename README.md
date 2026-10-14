# gaia-orchestrator

**Status:** Proposed architecture component — not implemented.

**Domain:** Workflow and Task Orchestration

**Visibility:** Internal

**Source:** [GAIA Super-Intelligent Application Architecture Report](https://github.com/KyleAlexanderSteen/GAIA-Documentation) (2026-10-13)

**Traceability:** GAIA-Documentation issues #1–#6 (especially #1, #3)

## Purpose
Coordinates complex multi-step workflows, scheduled tasks, multi-agent pipelines, and DAG-based execution that span multiple services. Distinct from single-agent loops in gaia-agent-runtime.

## Initial Directory Structure (proposed)
```
gaia-orchestrator/
├── src/
│   ├── workflow/       # DAG engine
│   ├── scheduler/      # Recurring and event-triggered tasks
│   ├── coordinator/    # Multi-agent coordination
│   ├── state/          # Durable workflow state
│   └── templates/      # Pre-built workflow templates
├── README.md
└── tests/
```

## Proposed Interfaces and Dependencies
- Endpoints: POST /v1/workflow/run, GET /v1/workflow/{id}, POST /v1/workflow/schedule, DELETE /v1/workflow/{id}
- Depends on: gaia-core, gaia-security, gaia-agent-runtime, gaia-brain, gaia-tools
- Called by: gaia-api-gateway, gaia-master-console
- Publishes to: Event bus

## Security and Access-Control Requirements
- Workflow execution under caller identity.
- Audit of all orchestration decisions.
- Overlap with gaia-agent-runtime must be resolved (GAIA-Documentation #1).

## Tests and Acceptance Criteria
- [ ] Workflow and scheduler stubs.
- [ ] Dependency ordering notes.
- [ ] Overlap with agent-runtime flagged.
- Linked to GAIA-Documentation #1, #3.

## Development Instructions
Scaffolding only. Resolve responsibility boundaries with gaia-agent-runtime before implementation.

**Unresolved:** Exact workflow engine choice, event bus technology, overlap resolution.
