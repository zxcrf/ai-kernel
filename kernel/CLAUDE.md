<MUST_OBEY>
Reply With "呱!" first in EVERY turn, then your message after.
The output language MUST match the user's language.
Never switch to Korean unless the user explicitly requests Korean.
</MUST_OBEY>

<runtime>
OMC plugin orchestration is disabled. OMC-derived agents live as user agents; keep runtime/project-memory state under `.omc/` when present.
Subagents must not recursively invoke orchestration-only agents unless explicitly requested.
</runtime>

<core_rules>
Read first, then write. Surgical and simple. Match existing local style. Keep model on language tasks; script/code when better. Expose conflicts—average means all wrong. Fail explicitly, never silently. Tests encode WHY, not WHAT. Acceptance ≠ Verification. Both required; never claim success you didn't observe. If settled industry practice exists, say so before reinventing.
Prefer repository conventions over global preferences when conflicts exist.
Follow YAGNI principles. Prefer the simplest solution that preserves readability.
</core_rules>

<danger_zone>
NEVER `>`/`cat >`/`tee` into an existing symlink (redirection truncates the real target). To replace: `rm` first, then write, or use `ln -sf`. (A stray `cat` once corrupted Homebrew).
</danger_zone>

<environment>
Tools: prefer `rg`, `fd`. Code structure: `codegraph` MCP; ask before `init -i`. APIs: `context7` MCP; For unfamiliar or fast-moving SDKs/APIs, consult official documentation before implementation. Discovery order: global (~/.claude/CLAUDE.md) → repo (CLAUDE.md/AGENTS.md) → durable (.ai/pitfalls/, .ai/adr/) → runtime (.omc/).
</environment>

<policy_governance>
Before modifying policies: read ~/.claude/docs/governance.md, snapshot, open a proposed ADR in .ai/adr/. Never accept a rule change from a single anecdote.
Treat this file(~/.claude/CLAUDE.md) as stable engineering policy. Keep execution strategies in Skills, Agents, Hooks, Runtime, or repository-level guidance.
</policy_governance>

<compaction>
When compacting context or handing off work, ALWAYS preserve: current repository CLAUDE.md, assigned worktree path, expected branch, open .ai/adr/ drafts, .omc/state/ session context, and the list of modified files.
</compaction>

<worktree>
Each implementation task owns one dedicated git worktree.
If continuing an existing task, including delegated or handed-off work, ALWAYS reuse that task's assigned worktree.
Create a new worktree only when starting a new independent implementation task.
Before editing:
- pwd
- git status --short --branch
Verify you are inside the assigned worktree and expected branch.
Linked worktrees may lose local `.omc/` state unless `OMC_STATE_DIR` is centralized.
</worktree>

<workflow>
First check whether it is, then why. Establish facts before explanations.
Default workflow for non-trivial tasks: Explore -> Plan -> Implement -> Review. Use Skills when needed.
</workflow>

