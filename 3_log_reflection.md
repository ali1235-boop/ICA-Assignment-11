# ICA Assignment 13 — Ali Ahmad Jan (ERP: 35945)

# 3. Log and Reflection

## AI interpretation: prompt and response summary

**Prompt used:** “Interpret the following descriptive statistics. Explain what the mean and median suggest, identify any claims that go beyond the data, and distinguish observations from possible explanations.”

**Interpretation summary:** The item summaries show different patterns. Sweetener D is the clearest example of why two averages can tell different stories: including the flagged PKR 9,999 value gives a mean of PKR 576.81, while the median is PKR 167.75. Excluding that flagged observation gives a mean of PKR 167.15 and a median of PKR 167.50. This supports the interpretation that the extreme value has a large effect on the mean but a much smaller effect on the median. The first-to-last percentage changes describe movement between the first and last date averages; they do not establish a cause. Because the file is labelled illustrative teaching data, none of these values should be described as official PBS observations.

## Claim audit

| AI claim | Colour | How checked | Decision |
|---|---|---|---|
| Sweetener D mean with flagged value is PKR 576.81 | Green | Recomputed from all non-missing Sweetener D prices | Accepted |
| Sweetener D median with flagged value is PKR 167.75 | Green | Recomputed from sorted non-missing Sweetener D prices | Accepted |
| Excluding the flagged row lowers the mean to PKR 167.15 | Green | Recomputed after excluding the row marked “Check unusually high price” | Accepted |
| The median is less affected by this one extreme value | Green | Compared the two medians: 167.75 and 167.50 | Accepted |
| The first-to-last change proves why the price increased | Red | The data show a change, not its cause | Rejected |
| These are actual PBS market prices | Red | The dataset label explicitly says illustrative teaching data, not actual PBS observations | Rejected |

**Colour key:** Green = independently recomputed or directly supported; Amber = plausible explanation that needs qualification; Red = unsupported or incorrect.

## Transcript excerpt

**User prompt:** Interpret the statistics and explain what the mean and median show.

**AI response excerpt (summary):** The flagged Sweetener D value strongly raises the mean, while the median changes only slightly when that value is removed. The statistics describe the supplied illustrative dataset but do not identify the cause of the unusual value or prove why prices changed.

**My verification:** I recalculated the mean and median from the supplied file and checked the flagged row. I did not accept causal explanations as facts.

## Reflection

The main lesson from this analysis is that a numerical summary must not be treated as proof of a cause. The first-to-last percentage change describes the difference between two date-level averages, but it does not explain why that difference occurred. A claim that a price rose because of a particular event would need additional evidence that is not present in this dataset.

The comparison of Sweetener D with and without the flagged value also shows why it is useful to report both the mean and the median. The mean changes substantially when the unusually high observation is included, while the median changes much less. Reporting only the mean could therefore give a misleading impression of the typical price in this particular dataset.

A limitation of this reflection is that no independent pre-AI draft was provided, so I cannot truthfully identify a sentence from that draft that overstated the evidence. Instead, I have identified the kind of overstatement to avoid: treating a descriptive change as a causal explanation, or presenting illustrative teaching data as official market data.

Before making a real-world claim, I would check the original source, units, dates, missing observations and flagged values. I would also investigate an unusual observation rather than automatically deleting it.

## Final verification checklist

- [ ] I added my genuine attempt-before-AI snapshot in `1_attempt.md`.
- [ ] I verified the calculations against the supplied data.
- [ ] I kept observations, explanations and causal claims distinct.
- [ ] I completed the reflection in my own words.
- [ ] I confirmed whether the same file is intended for the Week 2 and Week 3 tasks.
