# AI Coding Agent — Project Working Agreement

> **Template:** Copy to your own repository root as \`AGENTS.md\` for Codex and other agents that read this convention. Replace placeholders and adjust tools/commands. The filename by itself does not enforce permissions or grant tool access.

## Product and reference documents
- Project: [NAME] — [ONE-SENTENCE PURPOSE].
- Read local \`docs/CURRENT_HANDOFF.md\` or \`docs/CHAT_CONTINUATION.md\` before substantial work.
- Apply \`project_mgmt.md\` and \`human_friendly_design.md\` **if those files are copied into this project**. Otherwise read the original sources only if online access is available and explicitly authorised.
- Product-specific architecture, business logic, API contracts, and security controls remain authoritative.

## Before editing
1. Read owner instruction, current handoff, relevant ADRs and tests.
2. Check working tree, remote HEAD/branch, open PR and relevant CI; inspect provider state if needed and allowed.
3. Call out mismatches, limits, unknowns and the next single bounded task.
4. Define scope, exclusions, tests, budget and approval gates before changes.

## During work
- Implement one coherent chunk. Avoid unrelated refactors.
- Preserve auth, tenants, secrets, payment, audit and data integrity.
- Use a reviewable branch/worktree. Don't force push.
- Prefer local/static/focused tests before expensive CI/integration calls.
- Use tool integrations with least privilege and readback after external writes.
- On repeated failures, check if steps ran and inspect logs, config,
  provider health, GitHub budget/billing, quotas and Cloudflare/database limits.
- Never blindly replay ambiguous payment, email, DNS or provision writes.
- Compare official current pricing/quotas and alternatives before proposing a provider switch.

## Release authority
- No production deployment, paid service, budget increase, destructive action,
  DNS/auth/secret change or new broad privilege without owner approval.
- Passing tests do not imply merge, staging, owner acceptance or production permission.
- Do not claim unrun tests passed.

## End each chunk
Report [DONE / PARTIAL / BLOCKED], branch and commit, tests and CI, provider
readback, risks and unverified items. Update GitHub docs and Notion checkpoint
**when authorised and tools are available**. Record one exact next action.

## Project-specific commands
- Install: [command]
- Lint/typecheck: [command]
- Focused tests: [command]
- Full test suite: [command; run only when justified]
- Staging smoke check: [command]
- Rollback/recovery doc: [path]
