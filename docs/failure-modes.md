# Failure modes and troubleshooting

## Routing failures

| Failure | What it looks like | What to do |
|---------|--------------------|------------|
| Wrong specialist | Civic task sent to a shopping bot | Re-check purpose catalog; state why; re-route |
| Invented bot | Hand-off to a name not in the fleet | Stop; handle locally or ask to create a specialist |
| Ambiguous task | "Fix it" with no object | One clarifying question or take a safe first step |
| Context leak | Secrets included in hand-off | Strip secrets; pass only needed task context |

## Operations failures

| Failure | What it looks like | What to do |
|---------|--------------------|------------|
| Noisy proactive pings | Daily "just checking in" | Surface only blockers waiting on the owner |
| Stale catalog | New specialist exists but router unaware | Refresh from teammates list into memory |
| Primary flip error | SetPrimaryBot to wrong bot | Confirm choice first; verify after |

## Design notes

The router is the interaction plane; specialists are isolated workers. Fast-path filters (explicit @mention, channel already bound) beat slow semantic classification. Record what each finished hand-off taught for later routing quality.
