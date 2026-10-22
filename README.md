# ADA Security Lab

A small, deliberately vulnerable local demo built to test a TryHackMe AI Security room before submission: **"Hijack the Assistant" — Indirect Prompt Injection Against a Tool-Using AI Agent**.

ADA is a fictional dental-clinic booking assistant with real tool access (check availability, book appointments, send confirmation emails, look up patient records). It is used to teach and test prompt injection, filter evasion, and excessive-agency vulnerabilities in tool-calling AI agents, aligned with OWASP LLM01 and LLM06.

This is **not** a production system and is not meant to run anywhere but a local machine, by its own author, to validate training content before submitting it.

## Contents

- `room/` — the TryHackMe room content (scenario, tasks, flags, walkthrough, MITRE/OWASP mapping)
- `app/` — the local Flask + Anthropic tool-use demo implementing ADA
- `BUILD_PLAN.md` — architecture, full code walkthrough, setup and test guide

## Status (22.10.2026)

- Code in `app/` compiles cleanly and passes an independent, API-key-free logic test (routes, keyword filter, VIP-slot booking, hidden-tool leak via the server log, flag strings — see `BUILD_PLAN.md`, section "Frischer Beleg").
- **Not yet run:** a real end-to-end conversation against the Claude API (needs a personal `ANTHROPIC_API_KEY`) — see `BUILD_PLAN.md`, section 3, for the exact PowerShell commands and the two-pass test checklist (attacker pass + fresh-player pass).
- **Known open design question:** the hidden tool (`override_calendar_slot`) is discovered via a line in the server's terminal log. That works for local testing, but a real deployed TryHackMe room needs some way for a remote player to see that log (e.g. a simple log-viewer page) — not built yet, decide before submitting as a real room.
- No video recorded yet, no TryHackMe application submitted yet.

See `BUILD_PLAN.md` for the full architecture, code, and setup/test guide.
