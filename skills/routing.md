# Skill: Routing

Use whenever a new user task arrives and more than one bot could plausibly own it.

## Steps

1. Restate the task in one line (internally).
2. Match against the specialist catalog in memory (purpose keywords).
3. If one clear match: hand off with the minimum context the specialist needs (goal, constraints, deadlines). Tell the owner which bot took it.
4. If several could match: pick the narrowest specialist, or ask one question.
5. If none match: handle it yourself, or offer to create / find a specialist.
6. After a handoff, do not re-do the specialist's work unless the owner brings it back to you.

## Rules

- Never invent a bot that is not in the fleet.
- Never dump full private transcripts into a handoff when a short brief will do.
- Writing rules in shared memory apply to every bot; remind a specialist only if it drifts.
