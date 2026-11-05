# 1. THINK — Claims, Testable Questions and Predictions

**Student:** Ali Ahmad Jan  
**ERP ID:** 35945

## Claim 1: City-level price difference
**Everyday claim:** The same everyday product may be more expensive in one city than another.

**Testable question:** For each tracked item, what is the average recorded price difference between City 1 and City 2 across the available dates?

**Variables needed:** `item`, `city`, `price`, and `date`.

## Claim 2: Price stability
**Everyday claim:** Some household goods have less volatile prices than others.

**Testable question:** Which tracked item has the smallest and largest standard deviation of recorded prices across all observations?

**Variables needed:** `item` and `price` (with `date` retained to understand the observation period).

## Predictions (made before running the analysis)
- **Predicted dataset shape:** approximately 120 rows and 6 columns.
- **Predicted distinct items:** 5.
- **Predicted distinct dates:** 10.
- **Prediction for Claim 1:** I expect City 2 to have slightly higher average prices for most or all items.
- **Prediction for Claim 2:** I expect the cooking-oil category (Oil B) to show the greatest price variation, while Pulse C may be comparatively stable.

**Prediction status:** These are reasoned estimates for the exercise, not measured results. They must be compared with the actual output in the notebook.

**Data caution:** The CSV labels its observations as illustrative teaching data, not actual PBS observations. Conclusions therefore apply only to this dataset.
