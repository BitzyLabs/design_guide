# Human-Friendly Design Guide

### Practical UI/UX principles for founders building with AI

**Think complex. Present simple. Build for humans.**

A free, reusable product-design playbook from **[Bitzy Labs](https://github.com/BitzyLabs)**, developed through hands-on work on SaaS platforms, customer portals, operational dashboards, storefronts and onboarding experiences.

AI can produce screens incredibly quickly. Getting them to feel **intuitive, credible, accessible and genuinely useful** takes clearer instructions, better references, real journeys and repeated QA. This repository brings those lessons into one practical guide you can give to an AI coding agent or use in a human design review.

**[📖 Read the complete guide → human_friendly_design.md](human_friendly_design.md)**

---

## ✨ What you'll get

- **A product philosophy:** KISS — think complex, present simple; remove avoidable user effort.
- **Actionable UI standards:** no dead-end dashboard cards, confusing navigation or decorative controls masquerading as features.
- **Beautiful without the fluff:** deliberate layout, typography, hierarchy, density, brand consistency and restrained microinteractions.
- **Real user journeys:** onboarding, forms, multi-step tasks, saving, navigation, partial success and recovery.
- **Responsible design:** accessibility, trust, inclusive interaction, honest product states, privacy-aware feedback and safeguards.
- **Practical QA:** desktop/mobile checks, keyboard use, screenshot review, error states, acceptance checklists and release gates.
- **A copy-paste agent prompt:** a reusable starting point for coding agents, alongside concrete before/after examples.
- **References and credits:** direct links to the original external projects that helped shape the approach.

This is **framework-agnostic** and doesn't require subscriptions, packages, a particular design tool or a special AI model.

## 🚀 Use it in three ways

### 1. Give the link to your AI coding agent

Send the agent this instruction:

> Read https://github.com/BitzyLabs/design_guide/blob/main/human_friendly_design.md, inspect my existing design system and current UI, and apply the relevant human-friendly principles to **[screen or user journey]**. Preserve working behaviour and backend invariants. Test the rendered desktop and mobile journeys, keyboard accessibility, feedback, error states and recovery. Summarise what changed, what was verified and what remains untested.

The agent needs access to the URL or a pasted/local copy of the guide. Sharing a link alone does not automatically install any skill.

### 2. Add the Markdown file to your own project

Copy [human_friendly_design.md](human_friendly_design.md) into your repository and reference it from your project instructions (for example, your own AGENTS.md or other agent configuration). Keep your brand tokens and project-specific rules separate.

Example AGENTS.md snippet:

~~~md
## Product design and UX
For UI changes, read ./human_friendly_design.md before implementation.
Keep existing product tokens, branding, accessibility rules, security,
business logic and architectural invariants authoritative.
Audit the real journey and test the rendered result before claiming done.
~~~

The guide is advisory: adapt it to your product, users and constraints rather than enforcing every suggestion blindly.

### 3. Use the checklist for PRs and design reviews

Jump to the guide's [definition of done and acceptance checklist](human_friendly_design.md#16-definition-of-done-and-acceptance-checklist). It covers behaviour, states, accessibility, responsive layout, integrity and evidence.

## 🧭 The approach in one minute

1. **Identify the user and the task.** A screen's job matters more than a fashionable look.
2. **Design the full journey.** Entry → context → action → verified result → useful next step.
3. **Use a coherent visual language.** Typography, spacing, colour and interaction states should be deliberate.
4. **Reduce friction.** Eliminate unnecessary decisions, repetitive steps, hidden actions and excessive scrolling.
5. **Make every action work.** Tiles, rows, buttons, filters, Save/Discard and navigation must deliver what they promise.
6. **Be honest about status.** Loading, failure, partial completion and success must reflect reality.
7. **Audit on real screens.** Review desktop and mobile, keyboard use, long content, errors, recovery and typical browser zoom.
8. **Preserve engineering correctness.** Never trade data integrity, permissions, auditability or reliability for aesthetics.

## 📚 Repository contents

| File | Purpose |
| --- | --- |
| **[human_friendly_design.md](human_friendly_design.md)** | The complete reference guide, prompt, examples and acceptance checklist |
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

At Bitzy Labs, we iterated on product design through real usage, tough feedback, screenshots and countless small corrections. Across projects such as **[RoleRiff](https://roleriff.app)** and **[Tilfrd](https://tilfrd.dev)**, recurring lessons emerged: KISS, actionable interfaces, lower onboarding friction, better navigation, clear state feedback, responsive layouts and end-to-end testing.

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

This is a practical design guide—not a substitute for user research, security review, accessibility testing, legal advice or competent engineering judgment. A great design must still be tested in the product where it is used.

---

**Made with care in Melbourne by [Bitzy Labs](https://github.com/BitzyLabs).**

If this helps you build something less frustrating, use it, improve it and share it. 🚀
