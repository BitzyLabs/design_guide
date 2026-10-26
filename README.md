# Bitzy Labs — Design & Development Playbooks

### Human-friendly UX, continuity-first AI development and product naming for founders

**Think complex. Present simple. Build in small, verifiable steps.**

A free, reusable collection of practical design and AI-assisted development lessons from **[Bitzy Labs](https://github.com/BitzyLabs)**, developed while building SaaS products, customer portals, admin tools and connected infrastructure.

AI can generate code and screens quickly. Getting something **intuitive, reliable, recoverable and affordable to operate** takes clearer instructions, continuous documentation, real testing and practical oversight. This repository turns our hard-won lessons into three standalone guides that founders can give to coding agents or use for their own reviews.

**Choose your guide:**

- **[🎨 Human-Friendly Design → human_friendly_design.md](human_friendly_design.md)** — UI/UX, accessible interactions, onboarding, navigation, error states, visual QA and a copy-paste design prompt.
- **[🛠️ AI Development & Project Management → project_mgmt.md](project_mgmt.md)** — GitHub/Notion continuity, long-chat handovers, bounded chunks, agent roles, Composio, CI/provider budgets, troubleshooting, platform evaluation and agent prompts.
- **[✨ Product Naming → product_naming.md](product_naming.md)** — [one-shot AI research prompt](product_naming.md#start-here-one-prompt-with-the-ai-doing-the-research), real direct/adjacent competitor mapping, connected Composio/registrar lookups, ASIC and IP Australia checks, naming pivots, brand voice and decision records.

**A candid note:** I'm not a professional developer, project manager or UI/UX designer. These are practices I've developed as a founder through experiments, mistakes, AI collaboration and fixing real problems—not a substitute for qualified engineering or security review.

---

## Fork or copy before connecting an AI agent

**[BitzyLabs/design_guide](https://github.com/BitzyLabs/design_guide) is the public *upstream reference*, not your application's working repository.** It is there for you to read and reuse. **Do not instruct an AI agent to create branches, change files, push commits, change settings, or open automatic pull requests against the Bitzy Labs repository.**

**Recommended setup:**

1. **[Fork this repository into your own GitHub account or organisation](https://github.com/BitzyLabs/design_guide/fork)** if you want your own complete, editable copy. Open the **fork**, not the Bitzy Labs upstream, in Codex, Claude Code or your other write-capable agent. Confirm its full `owner/repo` name before starting any work.
2. **If you already have an application repository**, copy the relevant Markdown files from your fork (or copy individual upstream files read-only) into **your application's repository**, e.g. `docs/human_friendly_design.md`, `docs/project_mgmt.md`, `docs/product_naming.md`, `AGENTS.md` or `CLAUDE.md`. You **do not need to fork merely to read or copy** a guide.
3. **Connect your AI agent to *your own* repository and tools.** Tell it which `owner/repo`, branch and environment it may edit. Make upstream **read-only**. Check `git remote -v` when working locally: the writable `origin` should be your own repo/fork, not `BitzyLabs/design_guide`.
4. **Adapt the examples to your actual project.** Replace placeholders, configure real test commands, set explicit tool budgets and approval rules, then review the proposed changes before any push or deployment.
5. **Want to contribute an improvement upstream?** Work in your fork and submit an **intentional, separately reviewed pull request**. That is a contribution process—not permission for an agent to autonomously modify the original repository.

> **Copy this instruction into your chat/agent prompt:**  
> “Treat `BitzyLabs/design_guide` as a **read-only upstream reference**. First confirm my writable project repository or fork. If I have not provided one, ask me to fork the guide or copy its Markdown files into my own repository. Apply changes **only to my repository**, never to `BitzyLabs/design_guide`. Do not push, create a PR against upstream, or alter any other account/project without my explicit approval.”

**There are two different jobs:** *customising this guide* → work in your **fork**; *building your own product with the guide* → work in **your application repo** using a copied guide or an authorised read-only reference.

---

## 🛣️ Two ways to use the development guide

Not every founder uses AI in the same way. **Choose the workflow that matches how you build**—both use the same project-management principles.

### 💬 Track A — Chat-first builders

**Fork or copy the template into a workspace you own; direct the chat to your own project records and give upstream only read access.**

For people developing through ChatGPT or similar ongoing conversations. Keep your project state in GitHub/Notion (or a persistent Markdown checkpoint), break work into chunks, keep milestone updates and restart long chats with verified handovers instead of trying to remember everything.

- **[Read Track A](project_mgmt.md#track-a--if-you-build-your-project-through-chats)**
- **[Copy the Chat Continuation .md template](templates/CHAT_CONTINUATION.md)** into your project or Notion workspace

### 🤖 Track B — Full coding agents (Codex / Claude Code)

**Open your own application repo (with copied Markdown instructions), or your own fork if customising the guide. Set your agent's writable target explicitly; never run write-capable agents against upstream.**

For people using agents that read/edit repositories, execute tests and connect to services. Keep concise repo-specific instructions, point agents to the detailed guide, enforce scope and permissions, check CI/provider budgets and seal each chunk with real evidence.

- **[Read Track B](project_mgmt.md#track-b--if-you-use-full-coding-agents-codex--claude-code)**
- **[Codex: AGENTS.md starter](templates/AGENTS.md)** — copy into your repo root as \`AGENTS.md\`
- **[Claude Code: CLAUDE.md starter](templates/CLAUDE.md)** — copy into your repo root as \`CLAUDE.md\`

These templates **do not install plugins, grant access or bypass approvals**. You still need to configure your tools and review changes. Codex and Claude Code automatically recognise their respective project instruction conventions where supported; see the [Codex reference](https://developers.openai.com/cookbook/examples/codex/iterating-development-workflows-with-codex) and [Claude Code reference](https://support.claude.com/en/articles/14553413-claude-code-cheatsheet).

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

### Product Naming

- **A proper brief:** audience, product value, desired personality, market, budget and exclusions.
- **Distinct naming territories:** fewer generic AI names and better reasons behind each candidate.
- **Real competitive intelligence:** map direct, aligned/adjacent and substitute products, plus confusing existing names, with actual source links and evidence.
- **Human and legal pre-screening:** spoken/spelling tests, negative meanings, ASIC business-name availability and separate IP Australia trade mark checks.
- **AI-powered registrar research:** use supported direct integrations and Composio to batch real availability and initial/renewal checks; mark unsupported TLDs or inaccessible sites as unknown.
- **Brand-pack stress testing:** tagline, voice, wordmark, palette, light/dark app icons, landing pages and pricing.
- **Pivots and brand fit:** recheck product scope, competitors and naming territory when a product changes direction.
- **Durable decisions:** shortlist, rejected/do-not-recycle list, evidence and explicit purchase/registration approval.

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

**First: [fork or copy the guides into a repo you own](#fork-or-copy-before-connecting-an-ai-agent), then explicitly name your writable repository. The upstream Bitzy Labs repo stays read-only.**

For **product naming and brand research**, use the [full one-shot prompt in product_naming.md](product_naming.md#start-here-one-prompt-with-the-ai-doing-the-research). It asks connected agents to handle competitor, registrar and registry research **without** putting that manual burden back on the founder. It must not claim a name legally cleared or purchase anything without approval.

For **UI/UX work**, send the agent this instruction:

> Treat **BitzyLabs/design_guide as read-only**. Confirm that your writable target is **[MY_ACCOUNT/MY_APP_REPO]**, not the guide's original repository. Read my local/forked `human_friendly_design.md` (or the [upstream reference](https://github.com/BitzyLabs/design_guide/blob/main/human_friendly_design.md) read-only), inspect my app's design system and current UI, and apply the relevant principles to **[screen or user journey]**. Modify only my authorised app repo, preserve working behaviour and backend invariants, test desktop/mobile and accessibility, and report verified results. **No pushes or pull requests to Bitzy Labs upstream.**

For **project/development work**, use this instruction:

> Treat **BitzyLabs/design_guide as read-only**. Work only in **[MY_ACCOUNT/MY_PROJECT_REPO]**, after confirming the repository/branch and permissions. Read my local/forked `project_mgmt.md` (or the [upstream reference](https://github.com/BitzyLabs/design_guide/blob/main/project_mgmt.md) read-only), inspect my project's current GitHub/Notion checkpoint and real CI/provider state, then execute one bounded chunk with budget-conscious tests. Verify results, update **my project** handoff and report the exact next action. Never edit the Bitzy Labs repo or create an upstream PR; do not merge, spend, change credentials or deploy without authorisation.

The agent needs access to the URLs or a pasted/local copy. Sharing links does not automatically install any skill or grant connected-app permissions.

### 2. Add the Markdown file to your own project

First [fork the guide into your own account](https://github.com/BitzyLabs/design_guide/fork) if you want to maintain a complete copy; alternatively copy [human_friendly_design.md](human_friendly_design.md), [project_mgmt.md](project_mgmt.md), [product_naming.md](product_naming.md), or whichever guides you need **into a repository you own**. Reference your **local copies**, not an editable checkout of the Bitzy Labs upstream, from your project's own instructions (for example, AGENTS.md). Keep brand tokens, architecture and project-specific permissions authoritative.

Example AGENTS.md snippet:

~~~md
## Product design and UX
For UI changes, read ./human_friendly_design.md before implementation.

## Product naming and brand research
For product naming, read ./product_naming.md and run its research workflow.
Treat upstream as read-only. Do not purchase domains or claim legal clearance.

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

## ✨ The product naming approach in one minute

1. Define the customer, emotional promise and what the brand must not feel like.
2. Explore distinct naming directions before producing a manageable longlist.
3. Test pronunciation, spelling, memorability, potential double meanings and scope for growth.
4. Investigate actual **direct and aligned/adjacent competitors** as well as confusing name collisions; use official business-name/trade mark registers for separate checks.
5. Query available registrars through authorised tools/Composio; compare live first-year and renewal pricing, TLD support, eligibility and ASIC/IP Australia pre-screen results. Missing evidence is UNKNOWN.
6. Mock up serious finalists as real brands, not just logo concepts.
7. If the product pivots, revisit positioning and market overlap; preserve finalists/rejections and require founder approval before registration, payment or rebranding.

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
| **[project_mgmt.md](project_mgmt.md)** | Two workflows (chat-first and coding agents), GitHub/Notion continuity, budgets, incident triage, reviews and handovers |
| **[product_naming.md](product_naming.md)** | Automated naming research prompt, real direct/adjacent competition, Composio registrar checks, ASIC/IP Australia pre-screening, brand voice, pivots and decisions |
| **[templates/CHAT_CONTINUATION.md](templates/CHAT_CONTINUATION.md)** | Paste into a chat or keep as your ongoing project handover file |
| **[templates/AGENTS.md](templates/AGENTS.md)** | Copy-ready root project instructions for Codex |
| **[templates/CLAUDE.md](templates/CLAUDE.md)** | Copy-ready root project instructions for Claude Code |
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

No private source code, staging hosts, credentials, unreleased shortlists or proprietary business logic is included in this repository.

## 🤝 Contributing

Suggestions, corrections and small improvements are welcome.

- [Open an issue](https://github.com/BitzyLabs/design_guide/issues) with a concrete UX problem, evidence or a proposed improvement.
- If contributing to the upstream guide, submit an intentional pull request **from your own fork** that is concise, testable and useful beyond one framework or project. Do not direct an agent to push to the Bitzy Labs repository.
- Clearly credit original creators and sources when adding new references.
- **Don't copy third-party manuals, skills, artwork, private designs or proprietary source code into this repository.**
- Avoid unsupported claims of accessibility compliance or guaranteed conversion improvement.
- Prefer real before/after behaviour and reproducible acceptance criteria over vague design adjectives.

This repo intentionally remains lightweight: **no dependency or installation is required**.

## 📄 License and disclaimer

Original material in this repository is available under the **[MIT License](LICENSE)**, permitting commercial and personal reuse subject to its terms. External references, third-party materials, brand names and trademarks remain with their respective owners.

These are practical guides—not professional qualifications or replacements for user research, threat modelling, security reviews, accessibility testing, operations engineering or legal advice. Every adopted practice and implementation still needs appropriate verification.

---

**Made with ᥫ᭡. in Melbourne by [Bitzy Labs](https://github.com/BitzyLabs).**

If this helps you build something less frustrating, use it, improve it and share it. 🚀
