# Silent Blade

**Silent Blade** is a strategy for the Iterated Prisoner's Dilemma that combines early aggression with tactical adaptability. It starts strong, feels out its opponent, and then strikes with precision — either exploiting naive cooperators or standing firm against aggression.

---

## Strategy Overview

Silent Blade follows a simple yet powerful principle: **adapt to your opponent’s personality** over time.

### Behavior:

1. **First Move: Defect**
   - Silent Blade opens with betrayal to test the opponent’s response.

2. **Adaptation (Every Round After):**
   - It looks at the **last 5 moves** of the opponent:
     - If the opponent **cooperated 4 or more times**, it assumes they are too trusting and **betrays** again to exploit them.
     - If the opponent **defected 3 or more times**, it sees them as hostile and **retaliates** by betraying.
     - Otherwise, it **mirrors** the opponent’s last move — a cautious, reactive approach.
