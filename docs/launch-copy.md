# AI Kernel Launch Copy

Ready-to-post copy for launching AI Kernel.

Repository: https://github.com/zxcrf/ai-kernel

## Positioning

Stable policies. Evolvable capabilities.

Your global AI coding prompt should be a kernel, not a workflow manual.

## Short X Post

```text
I started treating my global AI coding prompt as a kernel:

- stable policies stay global
- repo conventions stay in the repo
- skills/agents/hooks carry execution strategy
- runtime state stays ephemeral

This fixed a real multi-agent handoff bug where agents kept creating new
worktrees instead of continuing the assigned task worktree.

Repo: https://github.com/zxcrf/ai-kernel
```

## X Thread

```text
1/ I think global AI coding prompts should be kernels, not workflow manuals.

Stable policies. Evolvable capabilities.

Repo: https://github.com/zxcrf/ai-kernel
```

```text
2/ The failure mode is familiar:

You start with a useful CLAUDE.md / AGENTS.md.

Then it accumulates engineering rules, workflow details, model routing,
agent internals, repo-specific conventions, and one-off incident fixes.
```

```text
3/ The prompt gets longer, but the policy gets less clear.

The assistant has more text to obey and more ways to conflict with itself.
```

```text
4/ The split that helped me:

Global prompt = stable policy kernel
Repository prompt = local project conventions
Skills/agents/hooks = execution capabilities
Runtime state = ephemeral task context
```

```text
5/ The real bug that made this obvious:

I told agents to always create a new worktree.

After handoff, the next agent obeyed perfectly and created another worktree.
```

```text
6/ The bug was not the agent.

The bug was my policy model.

Worktrees should be task-scoped, not agent-scoped:

task -> assigned worktree -> multiple agents
```

```text
7/ AI Kernel is my small repo for this pattern:

- stable global policy template
- policy governance
- task-scoped worktree handoff rules
- clear boundary between policy and capabilities

https://github.com/zxcrf/ai-kernel
```

## Hacker News

Title:

```text
Show HN: AI Kernel - stable policies for AI coding agents
```

Post:

```text
I built a small repo around a pattern that has been helping my AI coding
workflow: treat the global prompt as a kernel, not a workflow manual.

The idea:

- stable engineering policy belongs in the global prompt
- project conventions belong in the repository
- skills, agents, hooks, and scripts carry execution strategy
- runtime/session state stays ephemeral

The motivating bug was a multi-agent handoff issue. I had told agents to always
create a new worktree. After handoff, the next agent obeyed perfectly and
created another worktree, splitting one task across multiple worktrees.

The fix was not "better wording". It was a better policy model:

task -> assigned worktree -> multiple agents

Repo: https://github.com/zxcrf/ai-kernel
```

## Reddit

Title options:

```text
I started treating my global AI coding prompt as a kernel
```

```text
Stop writing giant CLAUDE.md files
```

```text
Task-scoped worktrees for AI coding agents
```

Post:

```text
I put together a small repo for a pattern that has made my Claude Code / Codex /
OpenCode-style workflows easier to maintain:

Stable policies. Evolvable capabilities.

The main idea is that the global prompt should stay small and stable:

- stable engineering policy
- safety constraints
- discovery order
- handoff invariants

Project-specific conventions stay in the repo. Execution strategy lives in
skills, agents, hooks, scripts, or runtime state.

The real bug that pushed me here was worktree handoff. I had a global rule that
all changes should happen in a newly created worktree. After a handoff, the next
agent obeyed perfectly and created another worktree, losing continuity with the
original task.

The corrected model is:

task -> assigned worktree -> multiple agents

Repo: https://github.com/zxcrf/ai-kernel

Curious if others have run into the same failure mode with long global prompts
or multi-agent handoffs.
```

## Discord Or Slack

```text
I published a small repo for a pattern that has helped my AI coding workflows:

AI Kernel - stable policies, evolvable capabilities
https://github.com/zxcrf/ai-kernel

The core idea is to keep the global prompt as a small stable kernel, then move
repo conventions, skills, agents, hooks, and runtime state out to the right
layer.

The practical bug it fixed for me: handoff between agents kept creating new
worktrees because my policy was agent-scoped instead of task-scoped.
```

## Article Draft

# Stop Writing Giant CLAUDE.md Files

Most AI coding workflows start with a simple global prompt.

Then the prompt grows.

It collects engineering principles, tool preferences, workflow details, model
routing, agent orchestration internals, project-specific rules, and one-off
incident fixes. The assistant has more instructions, but the policy becomes less
clear.

I have started treating the global prompt as a kernel.

Stable policies stay global. Repository conventions stay in the repository.
Skills, agents, hooks, and scripts carry execution strategy. Runtime state stays
ephemeral.

The distinction became obvious after a real handoff failure.

I had told agents that all changes must happen in a newly created worktree.
After one agent handed off to another, the receiving agent obeyed perfectly and
created another worktree. One task was now split across two worktrees.

The bug was not the agent. The bug was my policy model.

Worktrees should be task-scoped, not agent-scoped:

```text
task -> assigned worktree -> multiple agents
```

That rule belongs in stable policy because it protects task continuity across
agents and context compaction. The implementation details around tools,
subagents, and runtime memory do not belong there.

AI Kernel is a small repo for this model:

- a production-ready global prompt template
- policy governance rules
- task-scoped worktree handoff guidance
- a clear boundary between stable policy and evolvable capabilities

Repo: https://github.com/zxcrf/ai-kernel

