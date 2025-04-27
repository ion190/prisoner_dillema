# Silent Blade

**Silent Blade** is a strategy for the Iterated Prisoner's Dilemma that combines early aggression with tactical adaptability. It starts strong, reads its opponents carefully, and then strikes with precision — either exploiting naive cooperators, punishing aggressors, or adapting intelligently to changing behavior.

---

## Strategy Overview

Silent Blade follows two core principles:  
**adapt to your opponent’s personality** and **choose your battles wisely**.

---

### Behavior During a Match:

1. **First Move: Defect**

   - Silent Blade opens by betraying to test the opponent’s behavior.

2. **Adaptation (Every Round After):**
   - It analyzes the opponent’s **last 5 moves**:
     - If the opponent **cooperated 4 or more times**, it assumes they are overly trusting and **betrays** again to exploit them.
     - If the opponent **defected 3 or more times**, it sees them as hostile and **retaliates** by betraying.
     - Otherwise, it **mirrors** the opponent’s last move — a cautious, reactive approach.

---

### Opponent Selection Strategy (Round 2 Specific):

Since in Round 2 Silent Blade can **choose its opponents**, it uses a smart selection mechanism:

- It **calculates a "trust score"** for each opponent based on their history:
  \[
  \text{trust score} = \frac{\text{number of cooperations}}{\text{total rounds played}}
  \]
- **Selection Priority:**

  1. Prefer opponents with the **highest trust score** (most cooperative).
  2. If multiple candidates have the same trust score, choose the one with **fewer rounds played** (less familiar with Silent Blade’s tactics).
  3. If the current opponent still has rounds available, Silent Blade may continue exploiting them.

- Silent Blade **avoids opponents** who have already reached the maximum allowed number of rounds (200 rounds).

---

## Summary

Silent Blade plays **ruthlessly when it senses weakness**, **punishes aggression**, and **chooses the most exploitable opponents** whenever possible.  
It balances **aggression** and **cunning opponent selection** to maximize its score in the long game.
