# Simple News Recommender Simulation

This project simulates a basic news recommender system that selects and displays **two news articles** from a pool of five "fresh" articles to a visiting user. The simulation models user behavior and click probabilities based on the position of the articles (top or bottom of the page).

---

## Scenario Overview

- There are **K = 5** fresh news articles available.
- For each visit, the system selects **two distinct articles**:
  - One article is placed at the **top** of the page.
  - One article is placed at the **bottom** of the page.
- The user's click behavior follows this rule:
  - The user **clicks the top article (i)** with probability **p<sub>i</sub>**.
  - If the top article is **not clicked (1 − p<sub>i</sub>)**, then the user **clicks the bottom article (j)** with probability **p<sub>j</sub>**.
  - The user can click **at most one article** (either top or bottom) per visit.
  - There is also a chance that **no article is clicked**.

---

## 🎲 Random Click Probability

- Each article **i** is assigned a click probability **p<sub>i</sub>**, sampled **uniformly at random from [0.0, 0.7]**.
- To ensure **reproducibility**, initialize the random number generator with:
  ```python
  random.seed(<seed_value>)
