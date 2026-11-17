# 30–60 Second Demo Script Outline

**Goal**: Show one concrete, surprising capability of the process — the AI refusing to generate code and instead producing a clean numbered plan + acceptance mapping.

**Recommended format**: Screen recording (Loom or equivalent) of a live Cursor / Claude Code session. No voice-over required if on-screen text is clear; short voice-over is better.

## Script Structure (45–55 seconds ideal)

**0–8s — Hook**
Show a messy or incomplete brief on screen.
Text overlay or spoken: “Most AI coding sessions jump straight into generating large diffs. Here’s what happens when you enforce the Vibe Coding Maximizer rules.”

**8–25s — Spec Enforcement**
Paste or show the Master System Prompt + a deliberately incomplete task.
Show the AI response: it refuses to write code and instead outputs (or requests) the one-page specification structure, or produces a clean numbered plan of file changes.

**25–40s — Increment + Verification**
Show a short approved plan.
Implement one small change.
Immediately run lint / type-check / test.
Show the clean pass and a one-line acceptance mapping.

**40–55s — Close**
Text overlay:
“Spec first. Numbered plans. Verification after every increment. Human owns architecture and payments.
Full system + templates: https://github.com/kmkirk83/vibe-coding-maximizer
24-hour scoped delivery with the same standard: see SERVICE_PRD.md in the repo”

**End card (2–3s)**: Product name + price + “Acceptance criteria are non-negotiable.”

## Alternative Public Sandbox Version
If a live recording is not immediately available:
- Create a public GitHub Gist or small repo that contains:
  - The master system prompt
  - An example incomplete brief
  - The AI’s structured response (plan + acceptance criteria request)
- Link the Gist in all outreach as the “demo.”

## Production Notes
- Keep the recording under 60 seconds.
- Use a clean, readable font size.
- Highlight the refusal to generate code and the numbered plan — those are the differentiating moments.
- Record once, reuse across X, Indie Hackers, Discord, and listing page.
