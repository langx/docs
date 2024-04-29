# 💡 Example

## Example for Daily Distribution

To understand the distribution of one-time bonuses for referred friends based on daily activities, let's break down the formula with an example.

### **Formula**

The [formula](../../langx-token/token/distibution/#formula) for the daily bonus distribution factors in user engagement metrics like message counts, online duration, activity streaks, and badge bonuses to compute a Baseamount. This determines a user's share of daily tokens, ensuring fair and proportional rewards. It incentivizes meaningful participation, fostering a vibrant and engaged community by basing rewards on the value contributed to the platform.&#x20;

`Baseamount = (Image-Messages * 200 + Voice-Messages * 100 + Text-Messages * 10) * (Online-Time / 120) * (Streak / 10) * Badges-Bonus`

`Distribution Percentage = Baseamount / Total-Baseamounts`

### **Example**

* **Inputs**
  * Images sent: 1
  * Audio messages sent: 3
  * Text messages sent: 80
  * Online time: 1 hour (60 minutes)
  * Streak: 10 days
  * Badges bonus (Early Adopter): 1.5
  * Daily tokens to be distributed by the smart contract: 10,000 tokens
* **Calculation Steps:**
  1. `Baseamount = [(1*200+3*100+80*10)*(60/120)*(10/10)*1.5] = (200+300+800)*0.5*1*1.5 = 750`
  2. Assume `Total-Baseamounts` (the sum of base amounts of all users) is 7000. Then, `Distribution Percentage = Baseamount / Total-Baseamounts = 750 / 7000 = 0.1071` or 10.71%

This result signifies you are eligible for 10.71% of the daily token distribution.

* **Final Calculation:** `Distribution = Distribution Percentage * Daily tokens = 0.1071 * 10,000 = 1071 tokens`

This example leads to a total distribution of **1071 tokens** due to your activity level and your "Early Adopter" badge bonus.
