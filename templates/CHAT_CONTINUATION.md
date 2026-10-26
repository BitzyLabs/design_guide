# Chat-First Project Continuation Template

> Copy this file into **your own** project as \`docs/CHAT_CONTINUATION.md\`, or paste its sections into a Notion page or another persistent document. Replace bracketed placeholders. **Don't leave secrets, tokens or private customer data in public repositories.**

**Read alongside:** [Bitzy Labs Project Management Guide](../project_mgmt.md) — **Track A: Chat-first development**.

## Project and authority
- **Product:** [name, one-sentence purpose]
- **Current objective:** [one narrow user outcome]
- **Owner-approved boundaries:** [what can/cannot be changed]
- **GitHub repository / default branch:** [URL / branch]
- **Current working branch / commit SHA:** [branch / SHA]
- **Notion Project Control / decision log:** [link or "not used"]
- **Current environment:** [local / staging / production; no private URL]
- **Authoritative provider state:** [what was actually read back]

## Current verified checkpoint
- **Status:** [NOT STARTED / PARTIAL / BLOCKED / COMPLETE]
- **Last completed chunk:** [ID and scope]
- **Exact implementation evidence:** [commit/PR/files]
- **Tests actually run:** [commands, outcomes, relevant CI run]
- **Deployment check:** [NOT DEPLOYED / staging readback / production readback]
- **Owner/browser acceptance:** [DONE / PENDING / NOT APPLICABLE]
- **Known gaps and defects:** [...]

## Next bounded chunk
- **Task:** [...]
- **Why it matters:** [...]
- **In scope:** [...]
- **Explicitly out of scope:** [...]
- **Acceptance tests:** [...]
- **Risk / budget / tools:** [...]
- **Requires my approval:** [...]
- **Stop conditions:** [...]

## What to paste into the next chat

Act as the next-session project assistant for [PRODUCT]. You are **continuing**
work rather than restarting. First read this project's current checkpoint,
GitHub docs and, when connected, Notion Project Control. Verify the actual
branch/commit, CI and provider state before treating earlier summaries as true.

Work in one bounded chunk at a time. Update the durable checkpoint after
milestones. Use tool integrations when available; otherwise tell me exactly
which evidence you need and don't pretend to have checked it. Don't guess
about budgets or provider limits. On repeated unexplained failures, inspect
logs, whether a job actually ran, permissions, account quotas, CI spending
limits, and Cloudflare/database allowances before changing code again.

Use low-cost targeted tests first. Avoid blind retries or unnecessary tool
calls. Obtain my approval for destructive, paid, production, DNS, credential
or security-sensitive actions.

At each meaningful update distinguish IMPLEMENTED, TESTED, STAGED, ACCEPTED,
LIVE and BLOCKED. End with the exact next action and what remains unverified.

**First action:** reconcile the checkpoint with real state, flag mismatches,
and proceed only within the approved next chunk.

## Practical rollover routine

1. Close or clearly mark the active chunk **PARTIAL**.
2. Verify GitHub HEAD, CI runs and relevant provider state.
3. Update this file (or its Notion equivalent) with **actual facts**, risks and next step.
4. Ask the outgoing chat for a comprehensive, **evidence-based** starter prompt.
5. Start a fresh chat and paste the prompt or provide this file/link.
6. Require the new chat to independently reconcile the current sources.
7. Archive the old chat; don't rely on it as the sole project memory.

### No connectors yet?

Maintain the checkpoint manually. Paste or upload the relevant changed files,
git log/commit hash, CI error and provider console evidence when necessary. Do not
invent a “GitHub checked” result merely because an agent says it probably passed.
