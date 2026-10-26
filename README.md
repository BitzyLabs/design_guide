# Bitzy Labs — Design & Development Playbooks

### Human-friendly UX and continuity-first AI development for founders

**Think complex. Present simple. Build in small, verifiable steps.**

A free, reusable collection of practical design and AI-assisted development lessons from **[Bitzy Labs](https://github.com/BitzyLabs)**, developed while building SaaS products, customer portals, admin tools and connected infrastructure.

AI can generate code and screens quickly. Getting something **intuitive, reliable, recoverable and affordable to operate** takes clearer instructions, continuous documentation, real testing and practical oversight. This repository turns our hard-won lessons into two standalone guides that founders can give to coding agents or use for their own reviews.

**Choose your guide:**

- **[🎨 Human-Friendly Design → human_friendly_design.md](human_friendly_design.md)** — UI/UX, accessible interactions, onboarding, navigation, error states, visual QA and a copy-paste design prompt.
- **[🛠️ AI Development & Project Management → project_mgmt.md](project_mgmt.md)** — GitHub/Notion continuity, long-chat handovers, bounded chunks, agent roles, Composio, CI/provider budgets, troubleshooting, platform evaluation and agent prompts.

**A candid note:** I'm not a professional developer, project manager or UI/UX designer. These are practices I've developed as a founder through experiments, mistakes, AI collaboration and fixing real problems—not a substitute for qualified engineering or security review.

---

## ✨ What you'll get

### Human-Friendly Design

- **A product philosophy:** KISS — think complex, present simple; remove avoidable user effort.
- **Actionable UI standards:** no dead-end dashboard cards, confusing navigation or decorative controls masquerading as features.
- **Beautiful without the fluff:** deliberate layout, typography, hierarchy, density, brand consistency and restrained microinteractions.
- **Real user journeys:** onboarding, forms, multi-step tasks, saving, navigation, partial success and recovery.
- **Responsible design:** accessibility, trust, inclusive interaction, honest product states, privacy-aware feedback and safeguards.
- **Practical QA:** desktop/mobile checks, keyboard use, screenshot review, error states, acceptance checklists and release gates.
- **A copy-paste agent prompt:** a reusable starting point for coding agents, alongside concrete before/after examples.
- **References and credits:** direct links to the original external projects that helped shape the approach.

### Project Management & Development

- **Durable project memory:** GitHub code/docs + Notion Project Control, decision logs and one Current Handoff.
- **Clean chat continuation:** structured handovers before context drift, followed by independent state verification in the new session.
- **Small, sealed chunks:** scope, tests, reviews, exact commit evidence, updates and next actions.
- **Multiple coding agents without chaos:** explicit ownership, separate branches/worktrees, review and release boundaries.
- **Tool integrations:** use native connectors or Composio with least-privilege access and provider-side verification.
- **Cost-aware engineering:** manage model/tool budgets, GitHub Actions minutes, Cloudflare/DB allowances and escalation policy.
- **Root-cause troubleshooting:** inspect logs, runner allocation, credentials, billing and limits before repeated blind retries.
- **Evidence-based platform selection:** compare actual pricing, included usage, reliability, scaling, security, reversibility and total cost.

Both guides are **framework-agnostic** and require no special installation or paid service. Linked tools and optional third-party skills may have their own terms.

## 🚀 Use it in three ways

### 1. Give the guides to your AI coding agent

For **UI/UX work**, send the agent this instruction:

> Read https://github.com/BitzyLabs/design_guide/blob/main/human_friendly_design.md, inspect my existing design system and current UI, and apply the relevant human-friendly principles to **[screen or user journey]**. Preserve working behaviour and backend invariants. Test the rendered desktop and mobile journeys, keyboard accessibility, feedback, error states and recovery. Summarise what changed, what was verified and what remains untested.

For **project/development work**, use this instruction:

> Read https://github.com/BitzyLabs/design_guide/blob/main/project_mgmt.md, inspect the latest GitHub and Notion project-control records, and reconcile actual source/CI/provider state before making changes. Execute one bounded chunk, choose budget-conscious tests and tools, investigate unexplained failures without blind retries, and finish with evidence, durable checkpoint updates and one exact next action. Do not merge, spend money, change credentials or deploy to production without authorisation.

The agent needs access to the URLs or a pasted/local copy. Sharing links does not automatically install any skill or grant connected-app permissions.

### 2. Add the Markdown file to your own project

Copy [human_friendly_design.md](human_friendly_design.md), [project_mgmt.md](project_mgmt.md), or both into your repository and reference them from your project's own instructions (for example, AGENTS.md). Keep brand tokens, architecture and project-specific permissions authoritative.

Example AGENTS.md snippet:

~~~md
## Product design and UX
For UI changes, read ./human_friendly_design.md before implementation.

## AI development and continuity
For implementation and project changes, read ./project_mgmt.md.
Check GitHub/Notion/current provider state, work in bounded chunks,
validate before promotion, and update durable handoff records.

Keep existing product tokens, branding, accessibility rules, security,
business logic and architectural invariants authoritative.
Audit the real journey and test the rendered result before claiming done.
~~~

The guide is advisory: adapt it to your product, users and constraints rather than enforcing every suggestion blindly.

### 3. Use the checklist for PRs and design reviews

For interface changes, use the [design acceptance checklist](human_friendly_design.md#16-definition-of-done-and-acceptance-checklist). For coding and release work, use the [project management gates](project_mgmt.md#11-manage-branches-reviews-and-release-gates), [honest status vocabulary](project_mgmt.md#13-verification-and-honest-status-reporting) and [handover templates](project_mgmt.md#16-reusable-templates).

## 🧭 The design approach in one minute

1. **Identify the user and the task.** A screen's job matters more than a fashionable look.
2. **Design the full journey.** Entry → context → action → verified result → useful next step.
3. **Use a coherent visual language.** Typography, spacing, colour and interaction states should be deliberate.
4. **Reduce friction.** Eliminate unnecessary decisions, repetitive steps, hidden actions and excessive scrolling.
5. **Make every action work.** Tiles, rows, buttons, filters, Save/Discard and navigation must deliver what they promise.
6. **Be honest about status.** Loading, failure, partial completion and success must reflect reality.
7. **Audit on real screens.** Review desktop and mobile, keyboard use, long content, errors, recovery and typical browser zoom.
8. **Preserve engineering correctness.** Never trade data integrity, permissions, auditability or reliability for aesthetics.

## 🔁 The development approach in one minute

1. **Keep memory durable.** GitHub holds executable truth; Notion tracks current scope, decisions and handoffs.
2. **Start by verifying reality.** Inspect branch, commit, CI, provider state and current control records.
3. **Work in small chunks.** Scope, implement, test, review, checkpoint, then continue safely.
4. **Roll over long chats deliberately.** Maintain structured, versioned handovers; rehydrate from sources of truth, not chat guesses.
5. **Use connected tools carefully.** Direct connectors or Composio with scoped permissions and readback after mutations.
6. **Treat budgets as constraints.** AI tokens, tool calls, GitHub Actions, Cloudflare usage and DB capacity all matter.
7. **Diagnose before retrying.** Check whether jobs ran, logs, config, quotas, billing and provider limits.
8. **Evaluate vendors properly.** Compare actual costs, reliability, included usage, failure-at-limit behaviour, and exit strategy.

## 📚 Repository contents

| File | Purpose |
| --- | --- |
| **[human_friendly_design.md](human_friendly_design.md)** | Human-centred UI/UX playbook, agent prompt, examples and acceptance checklist |
| **[project_mgmt.md](project_mgmt.md)** | AI development workflow, GitHub/Notion continuity, agents, tools, budgets, incident triage and handover templates |
| **[README.md](README.md)** | Overview, quick-start, provenance, contribution guidance |
| **[LICENSE](LICENSE)** | MIT licence for original Bitzy Labs contributions |

## 🙏 Inspiration, references and original creator credits

This guide is an **independent synthesis of Bitzy Labs' own hands-on product practice**. It is **not a fork, derivative package, rehosted skill, or reproduction** of the projects below. We encourage readers to explore and support their original maintainers.

| External repository | Credit | What to explore |
| --- | --- | --- |
| **[VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md)** | **VoltAgent** | Agent-readable DESIGN.md examples, visual systems and design tokens |
| **[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill)** | **Leonxlnx / Leon Lin** | Better agent-driven visual judgment, layouts and frontend polish |
| **[anthonyfuar/ux-knowledge](https://github.com/anthonyfuar/ux-knowledge)** | **anthonyfuar** | UX laws, humane-design principles, usability patterns and evidence |

**Licensing note:** VoltAgent/awesome-design-md and Leonxlnx/taste-skill publish MIT licences. Independently check the licence/terms of any third-party project before installing, copying or distributing its content. **No third-party skill files are bundled here.** Linking to an external project doesn't imply an endorsement, partnership or permission to relicense its material.

### Additional research and standards

- **[W3C — WCAG 2.2](https://www.w3.org/TR/WCAG22/)** — accessibility requirements and conformance criteria.
- **[Nielsen Norman Group — 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)** — foundational interaction-design review principles.
- **[Google web.dev — Web Vitals](https://web.dev/articles/vitals)** — real-world loading, interaction and layout-stability metrics.

Stripe, Shopify and Linear are useful **quality benchmarks**, not code, visual assets or layouts to reproduce. They do not sponsor or endorse this project.

## 🏗️ Where this came from

At Bitzy Labs, we've iterated through real usage, tough feedback, screenshots, CI failures, provider decisions and countless small corrections. Across projects such as **[RoleRiff](https://roleriff.app)** and **[Tilfrd](https://tilfrd.dev)**, recurring lessons emerged: KISS, actionable experiences, lower friction, GitHub/Notion continuity, bounded chunks, disciplined reviews and cost-aware infrastructure.

Instead of keeping those lessons buried in project-specific conversations, we're sharing an adaptable public reference for other founders and builders.

No private source code, staging hosts, credentials or proprietary business logic is included in this repository.

## 🤝 Contributing

Suggestions, corrections and small improvements are welcome.

- [Open an issue](https://github.com/BitzyLabs/design_guide/issues) with a concrete UX problem, evidence or a proposed improvement.
- Submit a pull request that is concise, testable and useful beyond one framework or project.
- Clearly credit original creators and sources when adding new references.
- **Don't copy third-party manuals, skills, artwork, private designs or proprietary source code into this repository.**
- Avoid unsupported claims of accessibility compliance or guaranteed conversion improvement.
- Prefer real before/after behaviour and reproducible acceptance criteria over vague design adjectives.

This repo intentionally remains lightweight: **no dependency or installation is required**.

## 📄 License and disclaimer

Original material in this repository is available under the **[MIT License](LICENSE)**, permitting commercial and personal reuse subject to its terms. External references, third-party materials, brand names and trademarks remain with their respective owners.

These are practical guides—not professional qualifications or replacements for user research, threat modelling, security reviews, accessibility testing, operations engineering or legal advice. Every adopted practice and implementation still needs appropriate verification.

---

**Made with care in Melbourne by [Bitzy Labs](https://github.com/BitzyLabs).**

If this helps you build something less frustrating, use it, improve it and share it. 🚀
