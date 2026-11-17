# Vibe Coding Maximizer System
## Spec-First Production Playbook + Prompt Library + Templates

**Version**: 1.0 | 2026-11-16  
**Purpose**: Turn high-velocity AI coding into reliable, production-ready output.

---

## Part 1 — Core Operating Principles (Non-Negotiable)

1. **Specify before generating**  
   Never produce substantial code until a concise one-page specification exists that includes: problem, target users, core data model, key user flows, constraints, and explicit, testable acceptance criteria.

2. **Small, verifiable increments**  
   Break work into atomic steps. For each step: Research → Plan (numbered list of intended file changes) → Implement → Test → Commit. Avoid large single prompts that attempt entire features.

3. **Human ownership of critical decisions**  
   Architecture, security boundaries, authentication, data validation, financial logic, and compliance remain under explicit human control. Treat the AI as a capable junior developer. Review every substantial diff.

4. **Automated verification as gate**  
   High-level acceptance or end-to-end tests are written early and run after every meaningful change. Lint, type-check, and secret scanning are non-negotiable.

5. **Demo-first distribution**  
   Prioritize a 30–60 second demo or runnable sandbox that shows a surprising, specific capability. Make the path from landing page or repository to first useful result as short as possible.

---

## Part 2 — System Prompt Library

### Master System Prompt (Cursor / Claude Code / equivalent)

```
You are a senior engineer operating under the Vibe Coding Maximizer protocol.

Rules you must follow on every task:
1. Refuse to generate substantial code until a concise specification exists that includes problem, target users, core data model, key flows, constraints, and testable acceptance criteria. If missing, request it.
2. Propose a numbered plan of intended file changes and wait for approval before writing code.
3. Implement only one atomic increment at a time. After implementation: run tests/lint, report results, and stop.
4. Never invent architecture, security, authentication, or payment decisions. Surface them for human decision.
5. Prefer small, reversible changes. Write clear commit messages that explain why.
6. Encode any fixed bug or lesson as a permanent note in the project rules file.
7. Optimize for observability: acceptance criteria must be measurable.

Current project context: [paste relevant files or architecture summary]
Current task: [exact task]
```

### Specification Request Prompt

```
Before any implementation, produce a one-page specification with these exact sections:
1. Problem (1–3 sentences)
2. Ideal Buyer / Target Users
3. Exact Deliverables
4. Non-Negotiable Acceptance Criteria (checklist of observable, testable outcomes)
5. Explicitly Out of Scope
6. Constraints
7. Success Metrics

Do not proceed to code until this specification is complete and approved.
```

### Increment Planning Prompt

```
Given the approved specification and current task, output only:
- Numbered list of intended file changes (create / modify / delete)
- Risk notes (security, data, breaking changes)
- Verification steps that will be run after the change
- Estimated scope (small / medium)

Do not write code yet. Wait for approval of the plan.
```

### Verification Gate Prompt

```
After implementing the approved plan:
1. Run the project’s lint, type-check, and test commands.
2. Report exact results (pass/fail + relevant output).
3. Map each relevant acceptance criterion to evidence.
4. List any remaining open issues.
5. Stop. Do not continue to the next increment until the human reviews.
```

---

## Part 3 — Project Rules File Template

Save as `.cursorrules`, `CLAUDE.md`, or project equivalent:

```
# Project Rules — Vibe Coding Maximizer

## Architecture Ownership
- Human owns: auth, payments, data validation, security boundaries, multi-tenancy decisions.
- AI proposes; human decides and records the decision here.

## Coding Standards
- Prefer small, focused files.
- Explicit types where the language supports them.
- No hardcoded secrets. Use environment variables and document them.
- Every non-obvious decision gets a short comment or entry in this file.

## Verification
- Single-command build + test + lint must exist and pass before any feature is considered done.
- Acceptance criteria are written as testable outcomes, not vague goals.

## Process
- Spec first.
- Plan (numbered file changes) before code.
- One increment → test → commit.
- Encode lessons permanently in this file.
```

---

## Part 4 — Acceptance Criteria Template

```
## Acceptance Criteria — [Feature / Delivery Name]

### Must Pass (Observable)
- [ ] [Criterion 1: e.g., “User can complete signup and reach dashboard without console errors”]
- [ ] [Criterion 2: e.g., “Payment intent succeeds in Stripe test mode and records a row in the database”]
- [ ] [Criterion 3: e.g., “npm run lint && npm run typecheck && npm test all exit 0”]
- [ ] [Criterion 4: e.g., “Repository builds with a single documented command and deploys to the free tier of Vercel/Netlify”]

### Evidence Required
For each criterion above, attach: screenshot, test output, or live URL.

### Explicitly Not Required
- [list anything that is intentionally deferred]
```

---

## Part 5 — Minimal Project Foundation Checklist

Before feature work:
- [ ] Single-command install + build + test + lint exists and is documented in README.
- [ ] Rules file (above) is present and current.
- [ ] Environment variable template (.env.example) exists with no real secrets.
- [ ] Basic CI configuration (GitHub Actions or equivalent) runs lint + type-check on push.
- [ ] One example acceptance-criteria file is present.

---

## Part 6 — Launch & Distribution Checklist (Free-Tier Only)

1. Create free Gumroad or Payhip account if none exists.
2. Upload the complete package (this Markdown + any supporting templates).
3. Write listing using the provided copy structure (see companion listing file).
4. Set launch price $97 (or $147 standard).
5. Prepare 30–60 second demo script or short Loom that shows one concrete outcome from using the system.
6. Post value-first messages in relevant communities (Indie Hackers, relevant Discords, X) leading with the demo and the acceptance-criteria promise. Avoid pure self-promotion.
7. Track every outreach and response in a simple log.
8. After first sales, collect feedback and encode improvements into the next version of the rules/prompts.

---

## Part 7 — Example Acceptance Report Structure

```
# Acceptance Report — [Delivery Name]
Date: YYYY-MM-DD

| Criterion | Status | Evidence |
|-----------|--------|----------|
| Core flow works end-to-end | Pass | [screenshot / URL] |
| Lint + type-check + tests pass | Pass | [command output] |
| No hardcoded secrets | Pass | [grep result or review note] |
| ... | ... | ... |

Known limitations: [list]
Hand-off notes: [deployment steps]
```

---

**End of Vibe Coding Maximizer System v1.0**

Use this system exactly as written. Adapt only the project-specific context sections. The process constraints are the product.
