# Human-Friendly Design
## A practical UI/UX field guide for founders, product teams, and AI coding agents

**Maintained by:** [Bitzy Labs](https://github.com/BitzyLabs)  
**Version:** 1.0 | **Updated:** 26 October 2026  
**Audience:** Founders, product owners, designers, developers, and AI-assisted builders  
**Scope:** SaaS products, customer portals, internal admin consoles, onboarding, commerce, and public-facing web experiences

> **North star:** Think complex. Present simple. Every visible control should help a person accomplish something meaningful.

This is an original, practical playbook distilled from building and reviewing products at Bitzy Labs. It is **not** a copied design system, a component library, a visual template, an accessibility certification, or a substitute for user research. It is a reusable set of expectations, patterns, review questions, and agent instructions.

Start with the **[copy-paste agent brief](#18-copy-paste-brief-for-ai-coding-agents)** if you want a quick result, or use the full guide as your quality bar.

---

## Contents

1. [The philosophy](#1-the-philosophy)
2. [Define people, jobs, and constraints](#2-define-people-jobs-and-constraints)
3. [Plan the journey before the screen](#3-plan-the-journey-before-the-screen)
4. [Build a coherent visual system](#4-build-a-coherent-visual-system)
5. [Navigation and information architecture](#5-navigation-and-information-architecture)
6. [Make interactions genuinely useful](#6-make-interactions-genuinely-useful)
7. [Forms, setup, and onboarding](#7-forms-setup-and-onboarding)
8. [Feedback, states, and recovery](#8-feedback-states-and-recovery)
9. [Accessible and inclusive by default](#9-accessible-and-inclusive-by-default)
10. [Mobile, density, and responsiveness](#10-mobile-density-and-responsiveness)
11. [Writing, trust, and humane defaults](#11-writing-trust-and-humane-defaults)
12. [Performance and engineering integrity](#12-performance-and-engineering-integrity)
13. [Different surfaces need different treatments](#13-different-surfaces-need-different-treatments)
14. [Patterns that repeatedly fail](#14-patterns-that-repeatedly-fail)
15. [The screenshot-to-shipping loop](#15-the-screenshot-to-shipping-loop)
16. [Definition of done and acceptance checklist](#16-definition-of-done-and-acceptance-checklist)
17. [Measure what actually improves](#17-measure-what-actually-improves)
18. [Copy-paste brief for AI coding agents](#18-copy-paste-brief-for-ai-coding-agents)
19. [Worked examples](#19-worked-examples)
20. [References, credits, and reuse](#20-references-credits-and-reuse)

---

## 1. The philosophy

**KISS is a product discipline, not permission to remove necessary capability.**

- **Think complex, present simple.** Do the difficult architecture and validation behind the scenes; expose only what the user needs at that moment.
- **One obvious next step.** At each point in a journey, people should be able to identify the primary action without deciphering the interface.
- **Every extra action is friction worth questioning.** Remove unnecessary clicks, typing, navigation, confirmations, and repeated decisions. Do not remove deliberate safety checks.
- **Useful beats decorative.** A beautiful chart that does not answer a question, or a clickable-looking tile that goes nowhere, is unfinished work.
- **Recognition beats memory.** Surface current state, recent context, relevant labels, and suitable defaults instead of asking users to remember them.
- **Trust is part of the interface.** Explain what will happen, what happened, what has not happened, and what can be undone.
- **Calm by default.** Use motion, colour, notifications, and urgency only where they communicate something.
- **System consistency, product personality.** Reuse interaction patterns, but let each product have its own brand, audience, tone, and purpose.
- **Polish follows correctness.** A visually impressive page that misrepresents status, loses data, or breaches permissions is not polished.
- **Keep judgment human.** AI can propose and implement. Founders and users still need to inspect, challenge, test, and decide.

### A simple decision rule

For each proposed UI element, ask:

1. What user question does it answer or what task does it advance?
2. Is this the most understandable place for it?
3. Could the system do this safely without asking?
4. What changes when the user activates it?
5. How will the user know it worked?
6. Can the user recover if it fails?

If an element cannot pass these questions, simplify it, redesign it, or remove it.

## 2. Define people, jobs, and constraints

Before writing CSS or generating screenshots, create a short brief:

| Question | What to record |
| --- | --- |
| Who is using this? | Beginner, frequent operator, administrator, customer, mobile-only user, etc. |
| Why are they here? | A concrete job-to-be-done, not a menu name |
| What is success? | The observable outcome and its correct backend state |
| What is high risk? | Payment, deletion, irreversible actions, identity, permissions, sensitive data |
| What is most common? | Prioritise the frequent path without trapping power users |
| What can be automated? | Safe prefills, suggestions, background validations, reconciliation |
| What are the constraints? | Existing design system, supported devices, accessibility, deadlines, performance |
| What must not change? | Domain logic, state machines, API contracts, auth boundaries, audit trails |

Document assumptions instead of inventing them. For example, do not guess that users prefer a three-step wizard over a single screen without considering task complexity and feedback.

For new products, define a small set of design tokens. For established products, inspect the existing tokens and reuse them rather than creating a parallel system.

## 3. Plan the journey before the screen

Design the **end-to-end path**, not a set of attractive isolated pages.

A useful flow:

~~~text
Entry point / notification / search
  -> relevant overview or filtered queue
  -> specific item or task
  -> next valid action
  -> authoritative state change
  -> clear feedback
  -> updated state wherever it appears
~~~

Map the **happy path**, then map at least these exceptions:

- no data yet;
- filtered search with zero matches;
- partial completion;
- validation failure;
- slow request or failed network;
- expired session or permission denied;
- duplicate submission;
- stale data from another device or tab;
- an operation that succeeds server-side but the UI misses the response;
- cancellation, back navigation, and retry.

**A feature is complete only when a person can discover it, understand its state, finish the intended task, and confirm the real result without unnecessary detours.**

### Progressive disclosure

Keep the primary task visible and defer optional information:

- show the headline result before technical logs;
- put advanced settings behind clearly named expansion points;
- group long edit pages into meaningful sections or tabs;
- keep critical warnings, actions, and identity visible above secondary panels;
- never bury a required action in a tab that looks optional.

Do not create a wizard or tabs merely to make a short form look sophisticated. Use them when they reduce comprehension burden.

## 4. Build a coherent visual system

**Good visual design is a system of decisions, not a collection of effects.**

### Establish tokens

Record at minimum:

- surface and background colours, text and muted text, border, focus, danger, warning, success;
- font families and a deliberate type scale;
- spacing and layout increments;
- border radii, shadows, and elevation roles;
- button/input/table states;
- responsive widths and container rules;
- motion durations and reduced-motion alternatives.

Prefer semantic token names such as **text-primary**, **surface-raised**, **border-subtle**, and **action-danger** over ad hoc page-specific values. Ensure accessible contrast; do not assume a palette is compliant because it looks tasteful.

### Visual hierarchy

- Give **one primary call to action** priority per decision area.
- Make headings describe what users can do or learn.
- Use spacing, alignment, type weight, and grouping before adding borders or coloured cards.
- Avoid having all cards equally loud: highlight genuine priority.
- Match visual density to the job: public marketing can breathe; operations consoles need efficient scanning.
- Use real content lengths and edge cases in design, not only tidy placeholder data.
- Make icon meaning understandable with text where needed; do not rely on ambiguous icons alone.
- Give numbers meaningful labels, units, and useful follow-through.

### When borrowing visual inspiration

Study a product's **principles**—hierarchy, interaction, proportions—not its proprietary artwork, branding, source code, or literal page layout. A polished UI must still belong to your own product.

## 5. Navigation and information architecture

Users should know **where they are, what they can do here, and where to go next**.

- Put work where its responsibility belongs: overview, resource management, operations, settings, account, and help should have distinct jobs.
- Use stable navigation labels in human language.
- Make active location apparent and page titles meaningful.
- Keep navigation responsive: full sidebar when useful, compact navigation for narrow viewports.
- Provide search/command navigation when complexity justifies it, not as a substitute for coherent IA.
- Preserve context on navigation: an **Active reservations** tile should open reservations filtered to **Active**, not an unfiltered index.
- Make entire cards/rows clickable when they represent one destination and contain no competing interactive controls.
- Preserve browser Back/Forward behaviour, scroll/focus expectations, and deep links.
- On single-page route changes, update the page title and manage focus to the new page heading when appropriate.
- Avoid menu items that are cosmetic, dead, or permission-incompatible.

### Dense operational pages

For large data sets, provide effective search, meaningful filters, sort, pagination or virtualisation, clear row actions, readable statuses, and recoverable errors. Keep essential information visible instead of overflowing horizontally without a cue. Do not hide operational work behind a decorative dashboard.

## 6. Make interactions genuinely useful

**Affordance creates a promise.** If something looks clickable, it should have meaningful behaviour.

| Surface | Expected behaviour |
| --- | --- |
| Metric card | Open the relevant destination, ideally prefiltered |
| Workflow row | Open its detail or primary action, preserving context |
| Status badge | Clearly communicate a state; navigate only if visibly interactive |
| Search result | Open the matching resource and preserve query context where useful |
| Save button | Validate, persist, explain success/failure, refresh authoritative state |
| Cancel/Discard | Return safely without accidentally saving or losing unexpected changes |
| Delete/irreversible action | State impact, require appropriate confirmation, enforce permissions |
| Retry | Retry safely without creating duplicate effects |
| Logout | End the intended session and land somewhere understandable |

Never hide the real action behind an unnecessarily tiny **View** button when the entire row represents that destination. Conversely, do not wrap an entire row in a link when it also contains checkboxes, menus, or other conflicting controls.

### Forms with unsaved changes

- Clearly mark dirty or changed state.
- Keep Save/Discard actions near the user's work; compact sticky save bars can help long forms.
- Guard against accidental loss on route changes, switching records, or browser navigation.
- Do not silently auto-save if the user was promised explicit saving.
- Return focus and context after saves or refreshes.
- Prefer transactional safety over clever UI shortcuts.

## 7. Forms, setup, and onboarding

The best onboarding feels like making progress, not completing paperwork.

### Default approach

1. Ask only what the next step requires.
2. Offer a sensible suggestion where reliable (for example, deriving a full domain from an entered root domain).
3. If the input changes, update dependent labels, examples, previews, and summaries consistently.
4. Explain unusual permissions or requirements in plain language at the point of need.
5. Validate near the field; preserve input after errors.
6. Give a useful **Back** button and a clear final review for consequential actions.
7. Mark optional steps unmistakably and allow safe skipping.
8. End with confirmation and an immediately useful next action.

### Wizard or one page?

Use a wizard when there are **distinct mental stages**, dependencies, or an important review step. Prefer one page when fields are few and closely related.

An overlay wizard can preserve user context, but must fit the viewport, support keyboard/focus management, scroll internally when needed, and not become an awkward full-screen imitation on desktop. On mobile, a full-height sheet or dedicated page may be more usable.

### Progressive setup

Show a preview or explanation before demanding integrations or DNS changes. Distinguish **suggested**, **configured**, **verifying**, **active**, and **failed** states. Never imply that a setup succeeded just because a form submitted.

## 8. Feedback, states, and recovery

Every important interactive surface should intentionally support:

- **initial/loading:** reasonable skeleton or progress where useful, without flickering;
- **success:** plain-language outcome and next step;
- **empty:** nothing exists yet, with a suitable creation path;
- **filtered-empty:** no matches to this query, with a clear reset;
- **validation error:** which field, why, and how to fix it;
- **network/server error:** what is known, whether changes were saved, and whether retry is safe;
- **permission/auth error:** distinguish missing access from service unavailability;
- **partial completion:** name completed and incomplete work without hiding risk;
- **stale state:** refresh or reconcile safely, without trampling other changes;
- **disabled/unavailable:** explain prerequisites where useful.

### Honest system language

Use human-facing stages that correspond to actual backend state. For example, **Imported to shipping provider** is not the same thing as **Shipped**. A payment request being sent is not evidence of settlement. An upload starting is not proof the file was verified.

Use toasts for transient feedback and in-context messages for errors that demand a decision. Important failures should not disappear before the user can read them. Avoid making colour the only carrier of meaning.

### Retry and duplicate safety

UX should match a safe persistence model. If an operation partly succeeds, the UI must make that visible, retain any resulting identifier, and retry only unfinished work where possible. For money, orders, uploads, and provisioning, use appropriate idempotency and server verification.

## 9. Accessible and inclusive by default

**Aim for WCAG 2.2 AA** on applicable web experiences, then validate actual conformance rather than claiming it from a visual inspection.

- Use native semantic buttons, links, inputs, labels, headings, tables, and dialog controls.
- Make functionality operable with a keyboard alone; test Tab, Shift+Tab, Enter, Space, Escape, and applicable arrow keys.
- Provide visible keyboard focus and sensible focus order.
- Meet relevant text and non-text contrast requirements; test actual combinations.
- Give fields programmatic labels, useful error association, and accessible names.
- Respect browser text zoom, reflow, orientation changes, and narrow viewports.
- Make pointer targets comfortable and avoid accidental adjacent taps.
- Announce important asynchronous state changes accessibly without overwhelming users.
- Respect reduced-motion preferences and avoid unexpected autoplay or forced animation.
- Supply alt text for meaningful imagery; mark decorative images appropriately.
- Do not assume that everyone sees colour, hears audio, uses a mouse, or has unlimited attention or bandwidth.

Run automated accessibility checks, **and** do manual keyboard, screen-reader, zoom and device testing. Automated scores are signals, not certifications.

Canonical standard: [W3C — WCAG 2.2](https://www.w3.org/TR/WCAG22/).

## 10. Mobile, density, and responsiveness

Design for the task at the size and input method a person actually uses.

**Review at minimum:** compact phone, larger phone, tablet and desktop; include long names, large text, sparse data, busy data and low bandwidth.

- Prefer responsive reflow over simply shrinking the desktop layout.
- Keep important buttons and bottom navigation visible; avoid controls stranded below the fold solely due to oversized spacing.
- Avoid clipped dialogs, forms, tables, toast messages and dropdowns at ordinary browser zoom.
- Use explicit overflow affordances for wide data tables.
- Ensure sticky headers/footers do not cover content, controls or the keyboard.
- Keep mobile navigation and logout/account controls findable and visually integrated.
- Review portrait and landscape when relevant.
- Do not overcompress dense operational screens: let users inspect details without tiny text.

**Density is contextual:** a luxury storefront and a shipping operations queue should not use identical spacing. Shared usability principles can produce different aesthetics.

## 11. Writing, trust, and humane defaults

Microcopy is part of functionality.

### Write for the person

Prefer **“Save changes”**, **“Ready to pack”**, and **“Try again”** over internal state-machine terms or raw error codes. Be concise, but do not conceal consequences.

Good error message:

> We couldn't save the new address. Your changes are still here. Check your connection and try again.

Weak error message:

> UPDATE_FAILED: 500

### Trust and ethics

- Do not use deceptive countdowns, fake urgency, hidden fees, forced opt-ins or confusing cancellation flows.
- Clearly distinguish recommendations from requirements.
- Give honest explanations for data collection, sign-up verification and deletion.
- Make opt-outs and account exits discoverable.
- Do not manipulate attention through endless notifications or surprise motion.
- Ask permission only when needed and describe the expected outcome.
- Do not leak technical internals, security-sensitive identifiers, or private account data through UI messages.

The goal is not maximum engagement at any cost. It is helping users complete their own goals confidently.

## 12. Performance and engineering integrity

A beautiful interface that freezes, loses data or misrepresents events does not feel premium.

### Performance expectations

- Measure real-user performance using [Core Web Vitals](https://web.dev/articles/vitals) when applicable.
- Avoid large layout shifts, blocking bundles, unnecessary client rendering and oversized assets.
- Lazy-load secondary media and noncritical screens thoughtfully.
- Show prompt acknowledgment for meaningful actions, even if the server operation takes longer.
- Avoid rapid skeleton flashes on fast connections.
- Test degraded bandwidth and intermittent connectivity.
- Design animation for clarity, not as a substitute for speed.

### Preserve invariants

- Frontend authorization cues do **not** replace server-side authorization.
- Changing tenant/store context in the browser never grants permissions.
- Keep real audit history and authoritative server state intact.
- Do not change data models, payments, security, fulfilment, or deletion semantics just to match a design concept.
- Design clear boundaries between staging, sandbox actions and production.
- Test failures without accidentally making live payments, dispatching parcels, or deleting actual customer data.
- Do not claim visual or operational acceptance without observing and verifying the result.

## 13. Different surfaces need different treatments

| Surface | Primary design goal | Typical priority |
| --- | --- | --- |
| Marketing / waitlist | Clarity, trust, conversion without manipulation | One message, one primary CTA, concise form, clear feedback |
| Customer portal | Self-service confidence | Obvious current state, next action, history, helpful recovery |
| SaaS onboarding | Fast, low-friction first value | Defaults, progressive setup, preview, review/confirmation |
| Operations admin | Efficient, accurate repeated work | Dense but scannable tables, context-preserving queues, power-user navigation |
| Commerce storefront | Discovery and purchasing confidence | Product media, specifications, price clarity, availability, checkout trust |
| Settings / billing | Transparency and predictability | Scope, consequences, explicit save, accessible cancellation paths |

Use the same standards of usability and accessibility across all surfaces. Do **not** give them all identical layouts.

## 14. Patterns that repeatedly fail

| Anti-pattern | Better alternative |
| --- | --- |
| “Make it more premium” with no specifics | State hierarchy, density, typography, brand and interaction goals |
| Fifteen identical dashboard cards | Prioritise urgent tasks and meaningful groupings |
| Dead-end clickable-looking metrics | Link to relevant filtered workspaces |
| Giant modal containing a complicated workflow | Dedicated task view or well-bounded staged flow |
| Wizard for three simple related fields | A compact single form |
| Long form with hidden Save button | Clear contextual Save/Discard and dirty-state protection |
| Generic “Something went wrong” | Actionable message with known state and recovery |
| Changing a domain input leaves old examples | Derive previews and labels from current source value |
| Mobile page truncated at 100% zoom | Reflow, cap dialogs to viewport, audit overflow |
| Notification says “done” before server verifies | Distinguish queued, processing, succeeded, and failed |
| Beautiful but unreadable contrast | Validate contrast and essential accessibility |
| Animation on every element | Restraint, consistent states, reduced-motion fallback |
| Rebuilding a design system per screen | Shared documented tokens and components |
| Copying another brand's exact layout/assets | Study principles, then create an original expression |
| Confusing Auth/403/500 errors | Distinct session, permissions and availability states |

## 15. The screenshot-to-shipping loop

This is the practical process that improved our own projects.

### Step A — Establish a baseline

Inspect the actual running interface, source, existing design conventions, and the journey. Record the viewport, populated data, empty states, browser zoom and any visible defects. Do not judge only from code or idealised mocks.

### Step B — Diagnose, don't just restyle

For every issue, record:

- **Observation:** What precisely is wrong?
- **Impact:** Why does it slow down, confuse, exclude, or mislead someone?
- **Cause:** Information architecture, layout, state, content, performance, or backend contract?
- **Minimum useful fix:** What correction preserves existing functionality?
- **Acceptance evidence:** How will we show that it works?

Example: “Customer logout is difficult to find and appears disconnected from the sidebar” is more actionable than “logout is ugly.”

### Step C — Make bounded changes

Prioritise the biggest user pain. Reuse components and tokens. Preserve business rules and APIs. Avoid turning a small polish task into an unnecessary redesign or architecture rewrite.

### Step D — Check the rendered result

Use actual viewport screenshots and real interactions. Test mouse and keyboard, navigation, scroll, hover, focus, save, retry, error states, responsiveness and text zoom.

### Step E — Test the whole journey

Verify source action -> destination -> mutation -> authoritative refresh. Check that a status change appears everywhere appropriate without a manual page refresh when the design promises live state.

### Step F — Capture learnings

Update the project's design notes, reusable component specification, regression coverage, and outstanding issue list. Repeating the same UX fix separately in five products is avoidable.

## 16. Definition of done and acceptance checklist

Use this as a PR checklist or final agent gate. **Critical items are blockers**, not points to average away.

### Product and journey

- [ ] Primary user/job and success state are documented.
- [ ] Primary action and page purpose are obvious.
- [ ] No decorative dead-end controls remain.
- [ ] Navigation preserves relevant search, filter and record context.
- [ ] Both normal and exceptional journeys have been exercised.
- [ ] Extra clicks, redundant fields and pointless decisions were challenged.

### Interaction and content

- [ ] Save/Discard, cancellation and destructive confirmations behave as promised.
- [ ] Loading, empty, filtered-empty, error, auth and partial-success states are intentional.
- [ ] Feedback reflects verified results, not guessed success.
- [ ] Labels, counts and statuses match authoritative business semantics.
- [ ] Forms preserve user input and support safe recovery.
- [ ] Copy uses the user's language and explains consequences honestly.

### Accessibility and responsiveness

- [ ] Keyboard controls, focus visibility, focus order and semantic labels were checked.
- [ ] Contrast, text zoom/reflow and important target sizes were checked.
- [ ] Reduced-motion handling and non-colour status cues exist.
- [ ] Phone, tablet, desktop, dense data and long text were reviewed.
- [ ] No important controls are clipped, obscured or inaccessible at typical zoom.
- [ ] Accessibility claims are scoped to actual tests, not assumed.

### Technical and release integrity

- [ ] Server-side permissions and tenant boundaries remain authoritative.
- [ ] No payment, deletion, fulfilment, audit or data-loss regression was introduced.
- [ ] Relevant automated tests pass.
- [ ] Rendered UI and real interactions were checked in a safe environment.
- [ ] No secrets, private URLs or unapproved staging details were exposed publicly.
- [ ] Remaining gaps are recorded honestly rather than marked as passed.

**Release rule:** A screen existing is not equivalent to a feature working. A visually polished screen with untested critical flows is not ready.

### Optional review scorecard

Rate each from **0 (missing)** to **3 (strong evidence)**: clarity, navigation, task friction, feedback/recovery, accessibility, responsive fit, visual consistency, and correctness. The score is a conversation aid, **not** certification or permission to ignore a critical failure.

## 17. Measure what actually improves

Use product-appropriate measures rather than relying entirely on aesthetic preference.

- **Task completion:** Can users finish the intended journey unaided?
- **Time and steps to value:** How much effort is required to reach the outcome?
- **Error and abandonment rate:** Where do people get stuck or quit?
- **Recovery success:** Can users resume after partial failure?
- **Support demand:** Does the same confusion repeatedly generate tickets?
- **Accessibility:** What barriers appear in manual and automated audits?
- **Real-user performance:** Where do loading, interactivity or shifting layouts cause pain?
- **Qualitative review:** Can a first-time user explain what this screen is for and what's next?

Segment data where helpful (new vs expert, mobile vs desktop). Avoid dark-pattern optimisation, vanity engagement and causality claims from tiny samples.

## 18. Copy-paste brief for AI coding agents

**How to use:** Place this guide in your project (or give your agent its GitHub URL), then paste the brief below into your AI tool. Adapt the bracketed fields to your product. You do not need to install someone else's skill to benefit from these principles.

~~~text
You are the product designer, accessibility reviewer, and frontend engineer
for [PRODUCT]. Improve [SCREEN/USER JOURNEY] for [TARGET USER].

Before changing code:
1. Read human_friendly_design.md and the project's existing design documents.
2. Inspect the actual UI, routes, shared components, UX states, and relevant
   backend contracts. Do not invent missing product requirements.
3. State the user job, most important friction, technical invariants, and
   bounded design direction.
4. Propose the smallest coherent improvement that produces genuine user value.

Design and implement using these rules:
- KISS: think complex, present simple.
- Every actionable-looking element must do something useful.
- Preserve filters, selection and workflow context during navigation.
- Prefer meaningful defaults, progressive disclosure and clear primary actions.
- Make Save/Discard, errors, retries and partial successes understandable.
- Use intentional loading, empty, filtered-empty, auth and permission states.
- Build an accessible, keyboard-operable, responsive experience.
- Keep the product's identity, tokens, components and tone consistent.
- Use tasteful, restrained motion; honour reduced-motion preferences.
- Never misrepresent payment, shipping, provisioning or security state.
- Preserve backend authorisation, tenant isolation, auditability, business
  logic and existing working flows.
- No unrelated refactor or production action without authorisation.

Review the rendered experience on mobile and desktop, with realistic content,
at ordinary browser zoom. Exercise the full critical journey, including
errors and recovery. Test keyboard interactions and focus. Run applicable
automated checks.

Deliver:
A. What changed and why it helps the user.
B. Evidence from rendering, functional checks and tests.
C. Accessibility/responsive verification and any known limitations.
D. What remains unverified or out of scope.

Do not claim a pass for a test you did not run. Do not copy brand assets,
private code or entire third-party design systems.
~~~

### Optional external references for a specific task

- Need a **documented design language**? Explore [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md).
- Need **stronger aesthetic judgment**? Explore [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill), following its own installation and licensing guidance if you choose to install it.
- Need **UX principles, patterns and humane-design review**? Explore [anthonyfuar/ux-knowledge](https://github.com/anthonyfuar/ux-knowledge); check the original repository's terms before copying its content.

Use these resources **selectively**. This guide is an independent set of instructions and does not install, mirror or incorporate their contents.

## 19. Worked examples

### Example A — A dashboard tile

**Before:** “17 Active Reservations” is visually styled as a button but clicking does nothing.

**After:** The whole tile opens Reservations with the **Active** filter selected; the visible count and target rows come from the same authoritative status rules. Loading and unavailable states are explicit. Keyboard focus is visible.

**Test:** Navigate from the tile, check filter state, open a reservation, return and confirm context is preserved.

### Example B — An onboarding domain suggestion

**Before:** A generated domain is shown once, but changing the root domain leaves the preview, DNS examples and confirmation text using the old value.

**After:** All dependent previews derive from the current value. Editable overrides are respected, validation runs on the resulting domain, and the final review states exactly what will be configured. Provisioning does not show success before verification.

**Test:** Edit domain, revert, paste unexpected characters, fail DNS verification and retry.

### Example C — A dense record editor

**Before:** Identity, media, evidence and metadata live in one enormous page; Save is out of view and navigation accidentally loses changes.

**After:** Core identity and current status stay visible; related secondary work sits in clear accessible sections or tabs. Contextual Save/Discard persists; switching tabs doesn't silently save. Keyboard navigation, state restoration and unsaved-change guards work.

**Test:** Edit an unsaved field, change sections, attempt route navigation, save, refresh, and verify the committed result.

### Example D — A multi-step creation wizard

**Before:** The wizard starts before users understand what evidence they need; a failed upload discards all progress.

**After:** Clearly named stages lead from details to attachments to review. The user sees prerequisites early. On partial failure, completed work is preserved; retry resumes unfinished work without duplicate creation or false success.

**Test:** Complete flow, missing file, server timeout, back navigation, mobile dialog sizing, and retry with an existing record identifier.

## 20. References, credits, and reuse

### Original projects that informed our practice

**Thank you to the maintainers of these independent projects.** They deserve credit for making their work publicly available. Our guide links to their ideas but **does not claim authorship of, copy, bundle, redistribute or supersede** their content.

| Project | Creator / maintainer | Why it is useful |
| --- | --- | --- |
| [Awesome DESIGN.md](https://github.com/VoltAgent/awesome-design-md) | **VoltAgent** | Practical examples of design-system documentation and agent-readable visual direction; source project publishes an MIT licence |
| [Taste Skill](https://github.com/Leonxlnx/taste-skill) | **Leonxlnx (Leon Lin)** | Design judgment and agent-driven art direction; source project publishes an MIT licence |
| [UX Knowledge](https://github.com/anthonyfuar/ux-knowledge) | **anthonyfuar** | Research-informed UX principles, humane-design checks and interface patterns; verify upstream terms before reproducing any of its files |

**Other recommended authoritative reading:**

- [W3C — Web Content Accessibility Guidelines 2.2](https://www.w3.org/TR/WCAG22/) — accessibility requirements and conformance criteria.
- [Nielsen Norman Group — 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — widely used usability review principles.
- [Google web.dev — Web Vitals](https://web.dev/articles/vitals) — user-centric performance measures.

**Product quality benchmarks (inspiration, not endorsements):** [Stripe](https://stripe.com), [Shopify](https://www.shopify.com), and [Linear](https://linear.app). Study their interaction quality; do not imply affiliation or copy protected assets.

### About Bitzy Labs

This approach evolved through hands-on building, screenshots, manual QA and repeated product refinement. Public-facing projects include [RoleRiff](https://roleriff.app) and [Tilfrd](https://tilfrd.dev). The websites are mentioned as project context, not as guaranteed examples of a fully certified design system.

### Attribution and licensing boundaries

This file is original Bitzy Labs guidance, not a fork of the referenced repositories. The local repository's [LICENSE](LICENSE) applies **only to original content contributed here**; it does not relicense or grant rights to third-party work linked above. Upstream resources have their own terms, which may change. If you install an external skill or copy its files, check and comply with that project's licence and notices.

Founders are welcome to **use, adapt, and improve this original guide** under its repository licence. Credit is appreciated; the goal is fewer frustrating interfaces and better human experiences.

---

**Final principle:** Don't ask an AI to “make it look pretty” and call it done. Give it a human outcome, design constraints, strong references, and a reliable way to prove the result actually works.
