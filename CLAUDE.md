# CLAUDE.md

## Token budget — Claude Code (HARD RULE)

Owner rule 2026-10-25, mirrored from the user-level Claude Code config so cloud sessions, other machines and other accounts follow it. Planning stays at max effort; savings come from session and subagent hygiene.

1. New task = new session (/clear). New stage = new subagent; never wake an idle or finished subagent.
2. Plan once, at max effort, into one plan file. Update it at milestones, not after every step.
3. Subagents: implementation through subagent_type "worker" (`.claude/agents/worker.md`: Opus high, compacts at 250k); information gathering on Sonnet (pass model explicitly).

Settings behind this rule (`.claude/settings.json`): `autoCompactWindow` 500000 and `subagentPromptCacheTtl` "1h".
