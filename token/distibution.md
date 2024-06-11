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
- [Day Streaks](/library/day-streaks.md), consecutive days of activity
- [Badges](/library/badges.md), that have been earned

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

### Bonus Multipliers

#### Badges Bonus

Badges work as multiplicands for the previously calculated amount. This percentage bonus is calculated on top of the base amount and accumulates with each badge. Therefore, a maximum bonus of **x10.0** of the base amount is possible for now. For example, if you have the Early-Adopter and Pioneer badges, the bonus would be calculated as (1 + 0.5 + 0.2) = 1.7, meaning a 70% increase on the base amount.

| Badge                                                              | Bonus Multiplier | Bonus Percentage |
| ------------------------------------------------------------------ | ---------------- | ---------------- |
| [Fundamental Badge](../../welcome/badges.md#fundamental-badge)     | x3.0             | 200%             |
| [Backer Badge](../../welcome/badges.md#backer-badge)               | x2.0             | 100%             |
| [Early-Adopter Badge](../../welcome/badges.md#early-adopter-badge) | x1.5             | 50%              |
| [Pioneer Badge](../../welcome/badges.md#pioneer-badge)             | x1.2             | 20%              |
| [Teacher Badge](../../welcome/badges.md#teacher-badge)             | x1.1             | 10%              |
| [Creator Badge](../../welcome/badges.md#creator-badge)             | x1.1             | 10%              |

**Calculation Method**

To calculate the total bonus, sum up the bonus percentages of all the badges you possess and add 1 (representing the base amount). The result is your total multiplier. For example, if you have the **Fundamental Badge** and the **Teacher Badge**, the calculation would be:

\[ \text{Badges-Bonus} = 1 + 2.0 + 0.1 = 3.1 \]

This means you get a 210% increase on the base amount.

#### Day Streak Bonus

Day streaks also work as multiplicands for the previously calculated amount. This bonus is calculated using the formula `(Streak / 10)`, where `Streak` is the number of consecutive days a user has been active. This bonus can reach a maximum of **x3.0**.

| Streak                                                                   | Multiplier | Bonus |
| ------------------------------------------------------------------------ | ---------- | ----- |
| [Day Streak Bonus](../../library/day-streaks.md) [(formula)](./#formula) | x3.0       | 200%  |

## Example

To understand the distribution of one-time bonuses for referred friends based on daily activities, let's break down the formula with an example.

### Recall Formula

The [formula](#formula) for the daily bonus distribution factors in user engagement metrics like message counts, online duration, activity streaks, and badge bonuses to compute a Baseamount. This determines a user's share of daily tokens, ensuring fair and proportional rewards. It incentivizes meaningful participation, fostering a vibrant and engaged community by basing rewards on the value contributed to the platform.

### Inputs

| Parameter                                    | Value         |
| -------------------------------------------- | ------------- |
| Text messages sent                           | 80            |
| Audio messages sent                          | 3             |
| Image messages sent                          | 1             |
| Online time                                  | 60 minutes    |
| Streak                                       | 10 days       |
| Badges bonus (Early Adopter and Pioneer)     | 1 + 0.5 + 0.2 |
| Daily tokens to be allocated by the contract | 10,000 tokens |

### Calculation Steps

$$
\begin{align*}
\text{Baseamount} = & (80 \times 10 + 3 \times 100 + 1 \times 200) \\
                    & \times \left(\frac{\text{60}}{120}\right) \\
                    & \times \left(\frac{\text{10}}{10}\right) \\
                    & \times \text{1 + 0.5 + 0.2} \\
                  = & 1300 \times 0.5 \times 1 \times 1.7 \\
                  = & 1105
\end{align*}
$$

$$
\begin{align*}
\text{Distribution Percentage} = & \frac{\text{Baseamount}}{\text{Total-Baseamounts}} \\
                               = & \frac{\text{1105}}{\text{50000}} \\
                               = & 0.0221
                               \end{align*}
$$

> Assume `Total-Baseamounts` (the sum of Base Amounts of All Users) is **50000**.

Then, Distribution Percentage is equal **0.0221** or **2.21%**

This result signifies you are eligible for 2.21% of the daily token distribution.

### Final Calculation

`Distribution = Distribution Percentage * Daily tokens = 0.0432 * 10,000 = 432 tokens`

$$
\begin{align*}
\text{Distribution} = & \text{Distribution Percentage} \times  \text{Daily tokens} \\
                               = & \text{0.0221} \times \text{10000} \\
                               = & 221
                               \end{align*}
$$

This example leads to a total distribution of **221 tokens** due to your activity level and your all Badges and Day Streak bonuses.

## Anti-Abuse Measures

To ensure fairness and prevent exploitation, specific caps have been implemented across all parameters. Activities that exceed these caps contribute positively to the community but do not increase the token distribution amount.

This balanced approach ensures that our token distribution remains equitable and rewards meaningful contributions to our community.

| Feature        | Limit            |
| -------------- | ---------------- |
| Text-Messages  | 100 messages/day |
| Voice-Messages | 10 messages/day  |
| Image-Messages | 5 messages/day   |
| Online-Time    | 120 minutes/day  |
| Day-Streaks    | 30 days          |
