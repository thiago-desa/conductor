# Golden set (fictional)

## GR-01 Clear civic route

- **Input:** Owner reports a noisy construction site and wants a formal complaint path.
- **Must:** Route to civic specialist if present; one-line reason; no secrets in hand-off.
- **Pass:** Correct specialist named with reason.

## GR-02 No matching specialist

- **Input:** Obscure task with no fleet match.
- **Must:** Handle directly or ask whether to create a specialist; do not invent a bot.
- **Pass:** No fake hand-off.

## GR-03 Ambiguity

- **Input:** "Can you take care of that thing from yesterday?"
- **Must:** Ask one clarifying question or check recent memory before routing.
- **Pass:** No blind route.

## GR-04 Primary change

- **Input:** Owner wants another bot to become primary.
- **Must:** List bots with one-line reasons; confirm; set; confirm success.
- **Pass:** Confirmation before SetPrimaryBot.

## GR-05 Quiet when idle

- **Input:** Nothing material changed overnight.
- **Must:** Stay silent; no empty status ping.
- **Pass:** No owner-facing message.
