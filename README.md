# grok-bot-router

Primary Grok Bot that takes any task and routes it to the right specialist bot in the owner's fleet, or handles it directly when no specialist fits.

## Problem it solves

People who run several specialist bots need a single front door. Without a router, every chat becomes a manual decision about which bot to open. This design keeps one primary bot that knows each specialist's job, hands work off cleanly, and only bothers the owner when something needs them.

## How to use with Grok Bot

1. Create a new Grok Bot (suggested name: `Grok Bot` or `primary`).
2. Paste the contents of `agents/grok-bot-router.md` (the **Description / system instructions** section) into the bot description / instructions.
3. Keep `skills/routing.md` and `skills/primary-bot-getting-started.md` alongside the bot.
4. Set this bot as the owner's primary bot.
5. On first run, list the other bots, save each one's purpose to memory, and confirm writing rules and time zone.
6. Connect only the services the owner wants the router to check (calendar, mail, X, and so on).

## Import into Grok Bot

Copy this bot into your own Grok Bot: [Primary Bot template](https://x.ai/bot/jhJ_YXyW7fK0r47PYgW1b)

## Key files

| Path | What it is |
|------|------------|
| `agents/grok-bot-router.md` | Full sanitized agent definition |
| `skills/routing.md` | How to classify a task and hand it off |
| `skills/primary-bot-getting-started.md` | First-conversation setup |
| `docs/architecture.md` | Primary / specialist fleet model |
| `docs/workflow.md` | Intake, route, follow-up |
| `examples/fictional-routing-day.md` | Fully fictional multi-bot day |
| `ATTRIBUTION.md` | Design influences |
| `LICENSE` | MIT |
| `AGENTS.md` | Short agent instructions, boundaries, definition of done |
| `CONTRIBUTING.md` | How to propose changes safely |
| `docs/failure-modes.md` | Failure modes and troubleshooting |
| `evals/` | Golden-set behavioral regressions |
| `scripts/check.py` | Secrets/PII/em-dash/link hygiene checks |
| `scripts/github-workflow-checks.yml` | GitHub Actions workflow (copy to `.github/workflows/checks.yml` when the token has `workflow` scope) |

## Proof-of-work notes

This repository is a cleaned public snapshot of a working primary-bot design:

- Explicit specialist catalog in memory (purpose per bot)
- Hand-off rules that preserve context without dumping secrets
- Proactive check-ins only when something is waiting on the owner
- Getting-started skill that records writing rules for the whole fleet

## Review findings

Portfolio review notes (repos and templates): [docs/review-2026-11-09.md in repo-operational-head](https://github.com/thiago-desa/repo-operational-head/blob/main/docs/review-2026-11-09.md).

## License and attribution

MIT License. Copyright (c) 2026 Thiago De Sa.

Design influences are listed in `ATTRIBUTION.md`.
