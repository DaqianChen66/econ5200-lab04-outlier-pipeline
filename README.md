# econ5200-lab04-outlier-pipeline
# Outlier Detection on California Housing

## Objective

In this lab, I compared different outlier detection methods on the California Housing dataset and examined how each method identifies unusual observations.

## Methodology

- I diagnosed and fixed three bugs in an outlier-detection pipeline.
- I used an `OutlierDetector` class with Modified Z-score, Tukey fences, and Isolation Forest.
- I checked the parameters used by each method and used the class summary to review the results.
- I applied Modified Z-score and Tukey fences to `MedInc`.
- I applied Isolation Forest to all 9 numeric columns.
- I compared the observations flagged by the three methods using a Venn diagram.
- I wrote a method-selection memo recommending a combination of Tukey fences and Isolation Forest.
- I built an interactive outlier method explorer to compare different parameter settings and inspect flagged rows.

## Key Findings

Modified Z-score flagged **400** observations in `MedInc`, while Tukey fences flagged **681** observations. Isolation Forest flagged **1,032** observations using all 9 numeric columns.

The three methods agreed on **322** observations. This shows that different methods can identify different types of unusual observations because they use different information and rules.

Based on my comparison, I would use a combination of Tukey fences and Isolation Forest. Tukey fences are easy to understand for a single variable, while Isolation Forest can find unusual patterns across several variables.

I also learned that an observation being flagged does not automatically mean it should be removed. In housing data, unusual observations may represent real communities or important local conditions, so flagged rows should be reviewed before making a final decision.
