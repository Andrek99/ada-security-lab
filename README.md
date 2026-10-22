# ADA Security Lab

A small, deliberately vulnerable local demo built to test a TryHackMe AI Security room before submission: **"Hijack the Assistant" — Indirect Prompt Injection Against a Tool-Using AI Agent**.

ADA is a fictional dental-clinic booking assistant with real tool access (check availability, book appointments, send confirmation emails, look up patient records). It is used to teach and test prompt injection, filter evasion, and excessive-agency vulnerabilities in tool-calling AI agents, aligned with OWASP LLM01 and LLM06.

This is **not** a production system and is not meant to run anywhere but a local machine, by its own author, to validate training content before submitting it.

## Contents

- `room/` — the TryHackMe room content (scenario, tasks, flags, walkthrough, MITRE/OWASP mapping)
- `app/` — the local Flask + Anthropic tool-use demo implementing ADA
- `BUILD_PLAN.md` — architecture, full code walkthrough, setup and test guide

## Status

Private repository, used to prepare a work sample for a TryBuildMe application. See `BUILD_PLAN.md` for the full setup and the two-pass test checklist (attacker pass + fresh-player pass) before this is considered submission-ready.
