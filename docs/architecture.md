# Architecture

conductor is a long-lived primary agent in front of a specialist fleet.

## Goals

1. One chat the owner can always open
2. Correct handoffs to specialists that already know their domain
3. Shared writing rules and time zone across bots
4. Quiet proactive monitoring instead of daily noise

## Primary vs specialist

| Role | Owns | Does not own |
|------|------|--------------|
| Primary (this bot) | User-facing thread, routing, cross-bot coordination, simple tasks | Deep domain work that a specialist already covers |
| Specialist | Domain playbooks, deep tools, domain memory | Becoming the default chat without SetPrimaryBot |

## Memory

- Shared: owner name, time zone, writing rules
- Primary-local: specialist purpose catalog, open handoffs, proactive preferences

## What this repo is

A public-ready snapshot of the primary-router agent definition, routing skill, getting-started skill, and a fictional day-in-the-life example. It does not include any real specialist ids or private handoff text.
