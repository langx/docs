---
cover: ../.gitbook/assets/site-preview.png
coverY: 0
---

# 🪙 LangX Token

## LangX: The Economy-Token of the Language-Exchange Platform

[LangX](../) stands as the proprietary economy-token for its namesake platform—a unique, free, open-source, and community-driven arena for language exchange. This document aims to shed light on all aspects of LangX, offering a comprehensive overview for newcomers and existing users alike.

_**Introduction**_ [LangX](../) is the economy-token of the even-named, free, opensource and community-driven language-exchange platform. Even though the supply is limited it is still meant as encouragement for users of the app to increase their knowledge about languages and cultures of other people, countries and groups. Depending on their activity on the app, the development and growth of the community and their consistency in learning one will earn more and more of the token. The formula for the calculation is found later on this page.&#x20;

### Why?

We, as a community, have decided to develop an own token for multiple reasons.

- Users can earn tokens and seamlessly transfer them to their wallets for trading, embracing a [learn-to-earn](broken-reference) model through [Web 3.0 ](../library/technology/web-3.0.md)and [blockchain](../library/technology/blockchain.md) technologies. Many platforms offer alternative or unique ecosystem tokens, but later restrict access through paywalls or limitations, eroding trust in the crypto market. Our mission is to restore faith in cryptocurrencies by providing a transparent and unrestricted token ecosystem.
- To enhance user engagement and broaden their knowledge base, the platform should both incentivize active participation and facilitate learning.
- Currently, we are the only language exchange platform that utilizes an actual token system.

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

### Formula

`Baseamount = (Image-Messages * 200 + Voice-Messages * 100 + Text-Messages * 10) * (Online-Time / 120) * (Streak / 10) * Badges-Bonus`

`Distribution Percentage  = Baseamount / Total-Baseamounts`

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

| Badge               | Multiplier | Bonus |
| ------------------- | ---------- | ----- |
| Fundamental Badge   | x3.0       | 200%  |
| Sponsor Badge       | x2.0       | 100%  |
| Early-Adopter Badge | x1.5       | 50%   |
| Pioneer Badge       | x1.2       | 20%   |
| Teacher Badge       | x1.1       | 10%   |
| Creator Badge       | x1.1       | 10%   |

### Anti-Abuse Measures

To ensure fairness and prevent exploitation, specific caps have been implemented across all parameters. Activities that exceed these caps contribute positively to the community but do not increase the token distribution amount.

This balanced approach ensures that our token distribution remains equitable and rewards meaningful contributions to our community.

| Feature        | Limit            |
| -------------- | ---------------- |
| Text-Messages  | 100 messages/day |
| Voice-Messages | 10 messages/day  |
| Image-Messages | 5 messages/day   |
| Online-Time    | 120 minutes/day  |

## Example for Daily Distribution

To understand the distribution of one-time bonuses for referred friends based on daily activities, let's break down the formula with an example.

**Formula:**

`Baseamount = (Image-Messages * 200 + Voice-Messages * 100 + Text-Messages * 10) * (Online-Time / 120) * (Streak / 10) * Badges-Bonus`

`Distribution Percentage  = Baseamount / Total-Baseamounts`

**Example:**

- **Inputs:**

  - Images sent: 1
  - Audio messages sent: 3
  - Text messages sent: 80
  - Online time: 1 hour (60 minutes)
  - Streak: 10 days
  - Badges bonus (Early Adopter): 1.5

  - Daily tokens to be distributed by the smart contract: 10,000 tokens

- **Calculation Steps:**

  1. `Baseamount = [(1*200+3*100+80*10)*(60/120)*(10/10)*1.5] = (200+300+800)*0.5*1*1.5 = 750`

  2. Assume `Total-Baseamounts` (the sum of base amounts of all users) is 7000. Then, `Distribution Percentage = Baseamount / Total-Baseamounts = 750 / 7000 = 0.1071` or 10.71%

This result signifies you are eligible for 10.71% of the daily token distribution.

- **Final Calculation:** `Distribution = Distribution Percentage * Daily tokens = 0.1071 * 10,000 = 1071 tokens`

This example leads to a total distribution of 1071 tokens due to your activity level and your "Early Adopter" badge bonus.

1. The ultimate use of this token for sure is to enhance ones own experience and knowledge progress by our AI support for learning [**Copilot**](../library/copilot.md). One will be able to not only communicate with real people, but also with an AI which will respond to one in real-time, just as if there was someone even if no one is actually available, basically a non-stop-way for one to improve whenever they want.
2. Another way of spending this token is by gifting someone some of these who did a really great job at helping and basically pay them for their services.
3. Eventually we will implement a marketplace for platform-exclusive emoticons and expressions which only eligible currency this token will be.
4. You know about saving-accounts for real money? In Crypto-terms that is [Staking](defi-protocols/staking.md).
5. Last but not least; you can withdraw the tokens to your own [wallet](../library/technology/wallet.md) and buy more or sell them in a market.

### _**What is a Token ?**_

_**Okay, interesting, so, what is a token now basically?**_ If you want to know more about [blockchain](../library/technology/blockchain.md), tokens, [Web 3.0](../library/technology/web-3.0.md) and more just find our knowledge-base. You will find whatever you need to fully understand what you are getting in touch with here.
