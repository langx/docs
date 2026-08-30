---
description: >-
  How LangX Tokens are earned — the direct awards, the daily caps that keep them
  honest, and the shared daily pool.
---

# 📊 How Tokens Are Earned

Tokens come from two places: **direct awards**, paid the moment you do
something, and a **daily pool** that is shared out at the end of the day among
everyone who was active.

## Direct awards

| What you did                                                      | Tokens |
| ----------------------------------------------------------------- | ------ |
| Send a message                                                    | 2      |
| Write a correction on someone's sentence                          | 10     |
| Get a conversation going — the first time you and a partner have both spoken | 15     |

A correction is worth five messages, and that ratio is not an accident.
Teaching someone is the behaviour the platform exists for, so it is the
behaviour worth paying for. Corrections have no daily cap on either the free or
the Pro tier.

### Caps on message tokens

| Cap                                  | Limit                  |
| ------------------------------------ | ---------------------- |
| Messages that pay, per day           | 100 (up to 200 tokens) |
| Messages that pay, from one partner  | 30 (up to 60 tokens)   |

The per-partner cap is what stops two accounts from farming each other, and the
daily cap is what stops volume from beating quality. Anything past the cap
still helps the person you are talking to; it just does not pay again.

Both caps reset at **00:00 UTC**, the same clock the pool and the leaderboards
use. Your **streak** is the one thing measured in your own local day.

## The daily pool

Every day, **10,000 tokens** are shared out among the members who were active
that day, in proportion to how active they were. Nobody's share is fixed —
yours depends on everyone else's day as well as your own, which is what keeps
it worth watching.

Your activity score for the day:

$$
\text{Score} = 5 \times \text{Conversations} + 3 \times \text{Corrections} + 1 \times \min(\text{Messages}, 50) + 4 \times \text{Partners}
$$

| Term            | What it counts                                                    |
| --------------- | ----------------------------------------------------------------- |
| `Conversations` | New conversations where both sides spoke for the first time today |
| `Corrections`   | Corrections you wrote today                                       |
| `Messages`      | Messages you sent today, counted up to 50                         |
| `Partners`      | Distinct people you talked to today                               |

Talking to **four different people** is worth more than sending four times as
many messages to one, which is the behaviour the pool is trying to buy.

Your share:

$$
\text{Share} = \left\lfloor 10{,}000 \times \frac{\text{Your Score}}{\text{Everyone's Score}} \right\rfloor
$$

capped at **5% of the pool** (500 tokens), no matter how quiet the day was.

### Worked example

You send 30 messages to 4 different people, write 3 corrections, and one new
conversation gets going both ways:

$$
\text{Score} = 5 \times 1 + 3 \times 3 + 1 \times 30 + 4 \times 4 = 60
$$

If everyone's scores add up to 3,000 that day, your share is
$$\lfloor 10{,}000 \times 60 / 3{,}000 \rfloor = 200$$ tokens — on top of the
2 × 30 + 10 × 3 + 15 = 105 tokens you were already paid directly.

### Two conditions

- **Accounts younger than 24 hours earn no pool share.** A pool that paid out
  to hour-old accounts would be a throwaway-account generator.
- **A quiet day distributes nothing** rather than dividing a fixed pot among
  three people.
- **The share is paid at 04:00 UTC** the morning after the day it rewards, and
  is not shown to you before then — see
  [Daily tokens](../learn-2-earn/daily-tokens.md).

## Streak bonuses

Keeping a daily streak pays a bonus when you reach a milestone:

| Streak   | Bonus |
| -------- | ----- |
| 7 days   | 50    |
| 30 days  | 250   |
| 100 days | 1,000 |
| 365 days | 5,000 |

A day counts towards the streak when you do something meaningful — send a
message or write a correction. Opening the app does not count. See
[Day Streaks](../library/day-streaks.md).

## Why these numbers are public

Every rate, cap and weight on this page is in the app's source, in the open, in
`packages/shared`. That is fine: none of it is enforced by being secret. Awards
are written server-side, once, against a unique ledger entry per event — so an
award cannot be paid twice, whatever the client says.

These are also **starting values**. The right pool size and weights can only
really be found with real activity, so expect them to be tuned. The ledger they
are written to is append-only, which means a change can always be applied
without rewriting anyone's history.
