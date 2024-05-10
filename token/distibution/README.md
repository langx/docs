---
description: >-
  Detailed explanation of how the LangX Token distribution system works,
  including eligibility criteria, calculation formula, and anti-abuse measures.
---

# 📊 Distribution

## Token Distribution

Our platform operates a straightforward token distribution system that features both a general limit and a daily limit on the number of tokens allocated. These tokens are distributed based on a member's contribution to the community, measured through various activities.

### Eligibility for Daily Tokens

To be eligible for daily token distribution, members' activities are assessed using the following criteria:

- Number of text, voice, and image messages sent
- Daily active time on the platform
- Login streak
- Badges earned during membership

### Distribution Calculation

The number of tokens you receive daily is calculated as a percentage of the daily supply remaining. This calculation:

- Incorporates the above activities.
- Is subject to caps to prevent abuse. Activities exceeding these caps are appreciated but not included in the calculation.
- Each person can receive a very small percentage of the available daily supply.

## Formula

`Baseamount = (Image-Messages * 200 + Voice-Messages * 100 + Text-Messages * 10) * (Online-Time / 120) * (Streak / 10) * Badges-Bonus`

`Distribution Percentage = Baseamount / Total-Baseamounts`

In this formula:

- `Image-Messages`, `Voice-Messages`, and `Text-Messages` are the number of each type of message the user has sent. These are weighted differently, with image messages contributing the most to the base amount and text messages the least.
- `Online-Time` is the amount of time the user has spent online. This is divided by 120 to normalize it, meaning it reduces the value to a more manageable number. The more time a user spends online, the higher their base amount.
- `Streak` is the number of consecutive days the user has been active. This is divided by 10 to convert it into a multiplier. The longer the user's streak of activity, the higher their base amount.
- `Badges-Bonus` is a multiplier based on the badges the user has earned. The more badges or achievements a user has, the higher their base amount.
- `Baseamount` is the total score calculated based on the user's activity. It's used to determine the user's share of the total token distribution.
- `Total-Baseamounts` is the sum of the base amounts of all users. It represents the total activity of all users in the system.
- `Distribution Percentage` is the percentage of the total token distribution that the user will receive. It's calculated by dividing the user's base amount by the total base amounts of all users. The higher a user's base amount compared to the total, the larger the percentage of tokens they will receive.

**Distribution Percentage:**

The distribution percentage is the proportion of the total daily token distribution that a user is eligible for. It's calculated by dividing the user's base amount by the total base amounts of all users.

For example, if the total base amounts for all users is 9000 and a user's base amount is 975, the distribution percentage for that user would be `975 / 9000 = 0.1083` or 10.83%.

This means that the user is eligible for 10.83% of the total daily token distribution.

### Bonus Percentages

The badges work as multiplicand for the before calculated amount. This percentage bonus will be calculated ON TOP of the base-amount and accumulate, the more one have, therefore a maximum bonus of **350%** of the base amount is possible for now.

| Badge                                                              | Multiplier | Bonus |
| ------------------------------------------------------------------ | ---------- | ----- |
| [Fundamental Badge](../../welcome/badges.md#fundamental-badge)     | x3.0       | 200%  |
| [Sponsor Badge](../../welcome/badges.md#sponsor-badge)             | x2.0       | 100%  |
| [Early-Adopter Badge](../../welcome/badges.md#early-adopter-badge) | x1.5       | 50%   |
| [Pioneer Badge](../../welcome/badges.md#pioneer-badge)             | x1.2       | 20%   |
| [Teacher Badge](../../welcome/badges.md#teacher-badge)             | x1.1       | 10%   |
| [Creator Badge](../../welcome/badges.md#creator-badge)             | x1.1       | 10%   |

### Anti-Abuse Measures

To ensure fairness and prevent exploitation, specific caps have been implemented across all parameters. Activities that exceed these caps contribute positively to the community but do not increase the token distribution amount.

This balanced approach ensures that our token distribution remains equitable and rewards meaningful contributions to our community.

| Feature        | Limit            |
| -------------- | ---------------- |
| Text-Messages  | 100 messages/day |
| Voice-Messages | 10 messages/day  |
| Image-Messages | 5 messages/day   |
| Online-Time    | 120 minutes/day  |

In this section, you can find an example related to this distribution.

- [Example](example.md)
