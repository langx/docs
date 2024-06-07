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

### Base Amount Calculation

The `Baseamount` is calculated using the following formula:

$$
\begin{align*}
\text{Baseamount} = & (Text \times 10 + Voice \times 100 + Image \times 200) \\
          & \times \left(\frac{\text{Online-Time}}{120}\right) \\
          & \times \left(\frac{\text{Streak}}{10}\right) \\
          & \times \text{Badges-Bonus}
\end{align*}
$$

> Note that if no messages are sent within the day, the value will be 0.

### Distribution Percentage

The `Distribution Percentage` is the proportion of the total daily token distribution that a user is eligible for. It's calculated by dividing the user's base amount by the total base amounts of all users.

For example, if the total base amounts for all users is 9000 and a user's base amount is 975, the `Distribution Percentage` for that user would be `975 / 9000 = 0.1083` or 10.83%.

This means that the user is eligible for 10.83% of the total daily token distribution.

The distribution percentage is calculated as follows:

$$
\text{Distribution Percentage} = \frac{\text{Baseamount}}{\text{Total-Baseamounts}}
$$

### Parameters Description

The table below provides a description of each parameter used in the calculation of the `Baseamount` and `Distribution Percentage`.

| Parameter                 | Description                                                                                                                                                                                                                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Text`                    | The number of text messages the user has sent. These contribute the least to the base amount.                                                                                                                                                                                       |
| `Voice`                   | The number of voice messages the user has sent. These contribute moderately to the base amount.                                                                                                                                                                                     |
| `Image`                   | The number of image messages the user has sent. These contribute the most to the base amount.                                                                                                                                                                                       |
| `Online-Time`             | The amount of time the user has spent online. This is divided by 120 to normalize it. The more time a user spends online, the higher their base amount.                                                                                                                             |
| `Streak`                  | The number of consecutive days the user has been active. This is divided by 10 to convert it into a multiplier. The longer the user's streak of activity, the higher their base amount.                                                                                             |
| `Badges-Bonus`            | A multiplier based on the badges the user has earned. The more badges or achievements a user has, the higher their base amount.                                                                                                                                                     |
| `Baseamount`              | The total score calculated based on the user's activity. It's used to determine the user's share of the total token distribution.                                                                                                                                                   |
| `Total-Baseamounts`       | The sum of the base amounts of all users. It represents the total activity of all users in the system.                                                                                                                                                                              |
| `Distribution Percentage` | The percentage of the total token distribution that the user will receive. It's calculated by dividing the user's base amount by the total base amounts of all users. The higher a user's base amount compared to the total, the larger the percentage of tokens they will receive. |

**Distribution Percentage:**

### Bonus Percentages

The badges and day streaks work as multiplicands for the before calculated amount. This percentage bonus will be calculated ON TOP of the base-amount and accumulate, the more one have, therefore a maximum bonus of **x10.0** of the base amount is possible for now.

| Badge                                                                    | Multiplier | Bonus |
| ------------------------------------------------------------------------ | ---------- | ----- |
| [Day Streak Bonus](../../welcome/day-streaks.md) [(formula)](./#formula) | x3.0       | 200%  |
| [Fundamental Badge](../../welcome/badges.md#fundamental-badge)           | x3.0       | 200%  |
| [Backer Badge](../../welcome/badges.md#backer-badge)                     | x2.0       | 100%  |
| [Early-Adopter Badge](../../welcome/badges.md#early-adopter-badge)       | x1.5       | 50%   |
| [Pioneer Badge](../../welcome/badges.md#pioneer-badge)                   | x1.2       | 20%   |
| [Teacher Badge](../../welcome/badges.md#teacher-badge)                   | x1.1       | 10%   |
| [Creator Badge](../../welcome/badges.md#creator-badge)                   | x1.1       | 10%   |

The Day Streak Bonus is calculated using the formula `* (Streak / 10)`, where `Streak` is the number of consecutive days a user has been active. This bonus can reach a maximum of x3.0.

### Anti-Abuse Measures

To ensure fairness and prevent exploitation, specific caps have been implemented across all parameters. Activities that exceed these caps contribute positively to the community but do not increase the token distribution amount.

This balanced approach ensures that our token distribution remains equitable and rewards meaningful contributions to our community.

| Feature        | Limit            |
| -------------- | ---------------- |
| Text-Messages  | 100 messages/day |
| Voice-Messages | 10 messages/day  |
| Image-Messages | 5 messages/day   |
| Online-Time    | 120 minutes/day  |
| Day-Streaks    | 30 days          |

## Example

To understand the distribution of one-time bonuses for referred friends based on daily activities, let's break down the formula with an example.

### Recall Formula

The [formula](#formula) for the daily bonus distribution factors in user engagement metrics like message counts, online duration, activity streaks, and badge bonuses to compute a Baseamount. This determines a user's share of daily tokens, ensuring fair and proportional rewards. It incentivizes meaningful participation, fostering a vibrant and engaged community by basing rewards on the value contributed to the platform.

### Inputs

- Images sent: 1
- Audio messages sent: 3
- Text messages sent: 80
- Online time: 1 hour (60 minutes)
- Streak: 10 days
- Badges bonus (Early Adopter): 1.5
- Daily tokens to be allocated by the smart contract: 10,000 tokens

### Calculation Steps

1. `Baseamount = [(1*200+3*100+80*10)*(60/120)*(10/10)*1.5] = (200+300+800)*0.5*1*1.5 = 750`
2. Assume `Total-Baseamounts` (the sum of base amounts of all users) is 7000. Then, `Distribution Percentage = Baseamount / Total-Baseamounts = 750 / 7000 = 0.1071` or 10.71%

This result signifies you are eligible for 10.71% of the daily token distribution.

### Final Calculation

`Distribution = Distribution Percentage * Daily tokens = 0.1071 * 10,000 = 1071 tokens`

This example leads to a total distribution of **1071 tokens** due to your activity level and your "Early Adopter" badge bonus.
