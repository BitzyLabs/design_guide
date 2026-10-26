# Claude Code — Project Working Agreement

> **Template:** Copy to your own repository root as \`CLAUDE.md\` for Claude Code. Replace placeholders and keep this file short. If you use both Claude Code and Codex, keep rules consistent with the corresponding \`AGENTS.md\` rather than writing contradictory policies.

## Project
- Name: [NAME]; goal: [ONE-SENTENCE PURPOSE].
- Start with \`docs/CURRENT_HANDOFF.md\` and current architecture/decision docs.
- For the detailed methodology, read locally copied \`project_mgmt.md\` (and \`human_friendly_design.md\` for UI work) when present. Do not assume external network access.
- Existing architecture, owner decisions, security invariants and approvals take precedence over generic templates.

## Working loop
1. First inspect repo status, relevant files, last known good SHA, current handoff and CI.
2. State one bounded task, impacted files, acceptance checks, risks and budget.
3. Implement a focused change, inspect diff, run cheap relevant tests first.
4. Require extra review for security, tenancy, payments, deletes, provider changes or migrations.
5. Report what is actually verified; mark unrun tests and unobserved deployments explicitly.
6. Update durable project documentation and next action after each approved chunk.

## Troubleshooting and cost
- No unchanged CI-run loops. For mysterious instant failures, inspect whether
  any job executed, logs/annotations, credentials, runner capacity and account
  budget/billing before modifying application code.
- Check Cloudflare, database, email and API quotas/limits when a provider error
  cannot be explained from code/config evidence.
- Treat tokens, tool calls, CI minutes and paid infrastructure as finite budgets.
- Vet new platforms using official current pricing, allowances, hard stops,
  security, scale, recovery and vendor exit cost before suggesting them.

## Permission boundaries
- Do not raise spending limits or create paid services without approval.
- Do not touch production, credentials, DNS, billing, customer data or
  destructive provider actions without explicit, scoped authorisation.
- External actions must be verified by readback; ambiguous writes must not be blindly retried.
- Keep tools/Composio/MCP scope to the minimum required.

## Commands and project conventions
- Build: [command]
- Focused test: [command]
- Lint/typecheck: [command]
- Integration tests: [command, prerequisites]
- Staging verification: [command/path]
- Recovery runbook: [path]
