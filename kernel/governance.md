# Policy Governance

Treat global assistant policy as stable engineering policy, not as a scratchpad
for recent incidents.

## Change Rule

Before changing global policy:

1. Read the current policy.
2. Take a snapshot of the existing version.
3. Open a proposed ADR for the change.
4. Identify whether the rule belongs in the global kernel, repository policy,
   a skill, an agent, a hook, or runtime state.

Do not accept a permanent rule change from a single anecdote.

## Kernel Acceptance Criteria

A rule belongs in the kernel when it is:

- likely to remain valid across projects and model versions
- high ROI for correctness, safety, or continuity
- independent of one tool implementation
- short enough to stay memorable under context pressure

Move a rule out of the kernel when it is:

- tied to a specific tool version
- a workflow implementation detail
- only relevant to one repository
- a model-routing preference
- temporary runtime state

## Priority

Repository conventions override global preferences when they conflict.

Stable policy should define boundaries. Skills, agents, hooks, and runtime should
carry execution strategies.

