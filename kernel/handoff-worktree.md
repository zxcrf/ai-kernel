# Handoff and Worktree Continuity

Worktrees should be scoped to tasks, not agents.

The failure mode this prevents:

1. Agent A starts a task in one worktree.
2. Agent A hands off to Agent B.
3. Agent B reads "create a new worktree" as an agent-level instruction.
4. Agent B creates a second worktree and loses continuity with Agent A's work.

The corrected model:

```text
task -> assigned worktree -> multiple agents
```

## Required Handoff State

Every compaction or handoff must preserve:

- current repository CLAUDE.md
- assigned worktree path
- expected branch
- open ADR drafts
- runtime/session context under `.omc/state/`, when present
- list of modified files

Without the assigned worktree path, a receiving agent cannot reliably distinguish
"continue this task" from "start a new independent task".

## Worktree Rule

Each implementation task owns one dedicated git worktree.

When continuing an existing task, including delegated or handed-off work, reuse
that task's assigned worktree.

Create a new worktree only when starting a new independent implementation task.

Before editing, verify location and branch:

```sh
pwd
git status --short --branch
```

The goal is not "always create a worktree". The goal is "never mix independent
tasks in the same working tree, and never split one task across accidental
worktrees".

