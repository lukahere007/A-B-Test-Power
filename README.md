# A-B-Test-Power
A/B Testing Power Analysis with Sample Size Adjustment in R

This project demonstrates a step-by-step simulation and analysis of A/B testing under varying sample sizes. The goal is to evaluate the effect of increasing sample size on statistical power, p-values, and conversion estimates, using simulated binary data.

Objective

To explore how underpowered experiments (i.e., small sample sizes) can lead to inconclusive results, and how adjusting sample sizes can yield statistically significant outcomes and more reliable effect estimates.

Workflow Summary

1. Simulate Small Sample A/B Test

Group A conversion rate: p_A = 0.5

Group B conversion rate: p_B = 0.65

Sample size per group: n = 25

Analyze conversion rates and perform chi-squared test

Calculate power of the test using Cohen's h

2. Sample Size Calculation

Target power: 80%

Using pwr.2p.test to estimate required sample size to detect the effect

3. Simulate Large Sample A/B Test

Re-run simulation using the recommended sample size

Re-analyze and compare results to the small sample scenario

4. Summary Table

A clean summary table using kable presents:

Sample size

Conversion rates for A and B

P-values

Power

5. Visualizations

Several visualizations have been used to display the differences and improvements:

ggstatsplot::ggbetweenstats for statistical comparison with effect size

ggpubr::ggboxplot with p-value annotations

ggsignif bar plots with significance levels

ggpmisc to show regression line with equation

Confidence intervals using error bars

Key Packages Used

pwr for power analysis

dplyr for data manipulation

ggplot2 for general plotting

ggstatsplot, ggpubr, ggsignif, ggpmisc, and gghighlight for enhanced statistical plotting

Summary Table Output (Example)

Stage

Sample Size

Conv A

Conv B

P-value

Power

Small Sample

50

0.64

0.72

0.76

0.19

Adjusted Sample

339

0.47

0.65

0.001

0.80

Interpretation

Small sample resulted in low statistical power (~19%) and a high p-value, failing to detect the difference between groups.

After adjusting the sample size to achieve 80% power, a significant difference was observed (p = 0.001), with a narrower confidence interval.

How to Run

Clone the repository:

git clone https://github.com/lukahere007/missing-data-imputation-analysis.git

Open the R script or R Notebook

Run section by section to follow the simulation

License

This project is licensed under the MIT License.

Developed by Luke Wamalwa

University of Kansas Medical Center

Data Science & Statistics Program, 2025

