# Workflow Integrity and Accountability — Proposal

**Status:** Proposed; not approved or implemented.
**Canonical proposal:** https://github.com/KyleAlexanderSteen/GAIA-Documentation/blob/docs/alignment-attunement-self-improvement/GAIA-Documentation/GAIA-Universal-Principles-Integrity-Knowledge-and-Flourishing.md

## Candidate orchestration controls

- Track task intent, constraints, dependencies, owner, risk, and acceptance criteria through the full workflow.
- Preserve step-level status and evidence; do not mark a workflow complete when required steps are skipped, failed, or unverified.
- Distinguish parallel independent checks from correlated evaluations using the same model, data, or assumptions.
- Require explicit gates for high-impact operations, with authorization outside the proposing worker.
- Record retries, denials, partial results, compensating actions, and unresolved failures.
- Make dependency failure and stale evidence visible to downstream tasks.
- Prevent a workflow from silently changing its objective, acceptance criteria, permissions, or reviewer requirements to obtain a pass.
- Support pause, cancellation, escalation, and rollback for long-running tasks.

## Verification scenarios

Test partial completion, duplicate/replayed events, dependency failure, contradictory worker results, stale approval, permission denial, timeout, cancellation, and false completion claims. Evaluate whole task trajectories as well as final outputs.

These are candidate requirements only; contracts and implementation ownership must be approved first.