# Kernel Documents

This directory contains stable policy documents for AI coding assistants.

The kernel is intentionally small. It should define long-lived behavior that
improves correctness, safety, and handoff continuity across projects. It should
not become a workflow manual.

## Contents

- `CLAUDE.md`: a production-ready global prompt template.
- `governance.md`: rules for changing stable policy.
- `handoff-worktree.md`: task-scoped worktree and handoff continuity guidance.

## Boundary

Keep these in the kernel:

- stable engineering principles
- high-cost safety constraints
- environment discovery order
- policy governance
- handoff and compaction invariants

Keep these outside the kernel:

- project-specific conventions
- model routing
- execution strategies
- planner/reviewer/verifier internals
- temporary runtime state
- agent or hook implementation details

