# AGENTS.md

Short, high-signal instructions for coding agents working in `grok-bot-router`.

## What this repo is

Primary Grok Bot router: classifies tasks, hands work to specialist bots, and stays quiet unless the owner is needed.

This is a sanitized proof-of-work snapshot of a Grok Bot design. Markdown skills and docs are the product. There is no service binary to compile.

## Layout

| Path | Role |
|------|------|
| `agents/` | Sanitized primary-bot definition |
| `skills/` | Routing rules and getting started |
| `docs/` | Architecture, workflow, failure modes |
| `evals/` | Golden set of fictional routing days |
| `examples/` | Fictional multi-bot day |
| `scripts/check.py` | Hygiene CI entrypoint |

## Commands

```bash
python scripts/check.py
```

## Hard boundaries

- Never invent specialist bots that do not exist in the owner's fleet.
- Never paste secrets, vault contents, or personal data into group chats or public summaries.
- Do not silently set a new primary bot without confirmation.
- No em dashes or en dashes in prose.
- No secrets in the repo.

## Definition of done

- Routing examples match `skills/routing.md`.
- New route types get a golden-set case.
- `python scripts/check.py` passes; README import link intact.

## Ownership

Maintained by Thiago De Sa. Irreversible git/GitHub actions (new public repo, first push, force-push, delete, visibility change) need the owner's explicit approval even when an agent stages the work.
