# ICA Assignment 13 — Ali Ahmad Jan (ERP: 35945)

# 2. Work: Data and Calculations

## Dataset inspection

- Rows: 96
- Dates: 12 (2026-01-01 to 2026-03-19)
- Items: Staple A, Oil B, Pulse C, Sweetener D
- Cities: City 1, City 2
- Missing prices: 1
- Flagged unusual value: Sweetener D, City 1, 2026-01-22, PKR 9,999 per kg.
- Data label: illustrative teaching data, not actual PBS observations.

## Method

1. For each item, calculate the mean and median from all available non-missing price observations across both cities and all dates.
2. For first-to-last percentage change, first calculate the average price across the two cities on the first date and on the last date for each item. Then use:

   `percentage change = ((last-date average - first-date average) / first-date average) × 100`

3. For the flagged-value comparison, use Sweetener D. Calculate its mean and median with the flagged PKR 9,999 value included, then calculate them again after excluding that flagged row. The missing Pulse C value is omitted from calculations because it is not a numerical price.

## Results by item

| Item | Valid prices (n) | Mean (PKR/kg) | Median (PKR/kg) | First-date avg. | Last-date avg. | Change |
|---|---:|---:|---:|---:|---:|---:|
| Staple A | 23 | 160.89 | 112.50 | 104.00 | 117.50 | +12.98% |
| Oil B | 25 | 316.18 | 324.00 | 301.00 | 347.00 | +15.28% |
| Pulse C | 23 | 205.91 | 206.00 | 200.00 | 210.50 | +5.25% |
| Sweetener D | 24 | 576.81 | 167.75 | 152.00 | 181.50 | +19.41% |

**Interpretation caution:** Sweetener D's mean is much higher than its median because of the flagged PKR 9,999 observation. Its first-to-last change is calculated from date-level averages across the two cities, not from the overall mean.

## Week 2 flagged-value comparison: Sweetener D

| Measure | With flagged value | Without flagged value |
|---|---:|---:|
| Number of valid prices | 24 | 23 |
| Mean (PKR/kg) | 576.81 | 167.15 |
| Median (PKR/kg) | 167.75 | 167.50 |

### What changed?

- The mean falls by PKR 409.66 when the flagged value is excluded.
- The median changes only from PKR 167.75 to PKR 167.50.
- This demonstrates why the mean is sensitive to an extreme observation, while the median is more resistant.

## Limitations

- The dataset is explicitly labelled illustrative and is not official PBS data.
- The calculations summarize the supplied file only.
- A flagged value should not automatically be deleted in real research. It should be checked against the original source and documented. Here it is excluded only for the requested with/without comparison.
- The first-to-last comparison does not explain the cause of the change.
