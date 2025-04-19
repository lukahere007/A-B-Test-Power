📊 A/B Test Power Analysis in R

Overview

This project provides a hands-on walkthrough of A/B testing with a focus on sample size adjustment to achieve adequate statistical power. Using simulated binary outcome data, we evaluate the impact of increasing sample size on:

Statistical significance (p-values)

Power of the test

Conversion rate estimates

The analysis is implemented entirely in R and highlights key concepts in experimental design, hypothesis testing, and data visualization.

🎯 Objective

To demonstrate how underpowered experiments (e.g., small sample sizes) can lead to inconclusive results, and how increasing sample size can yield statistically significant outcomes and more reliable effect estimates.

🧪 Workflow Summary

1. Simulate Small Sample A/B Test

Group A conversion rate: p_A = 0.5

Group B conversion rate: p_B = 0.65

Sample size per group: n = 25

Steps:

Simulate binary outcomes

Estimate conversion rates

Perform chi-squared test

Calculate statistical power using Cohen’s h

2. Sample Size Calculation

Target power: 80%

Use pwr.2p.test() to estimate required sample size

3. Simulate Adequate Sample A/B Test

Re-run simulation using recommended sample size

Re-analyze and compare results with original small-sample scenario

4. Summary Table

Includes:

Conversion rates for A and B

p-values

Power

📊 Visualizations

We used the following libraries to generate informative visual summaries:

Library

Plot Type / Purpose

ggstatsplot

ggbetweenstats() for group comparison and test stats

ggpubr

ggbarplot() with CI bars and stat_compare_means()

ggsignif

Significance brackets for bar charts

ggpmisc

Polynomial trend line + regression equation

gghighlight

Enhanced group-wise emphasis in line/bar plots

📦 Key Packages

library(pwr)          # Power analysis
library(dplyr)        # Data manipulation
library(ggplot2)      # Visualization
library(knitr)        # Summary table formatting
library(ggstatsplot)  # Stats plots with inference details
library(ggpubr)       # Bar/box plots with CI
library(ggsignif)     # Add significance annotations
library(ggpmisc)      # Regression lines and equations
library(gghighlight)  # Emphasis in ggplots

🧾 Example Output Table

Stage

Sample Size

Conv A

Conv B

p-value

Power

Small Sample

50

0.6400

0.7200

0.7618

0.1899

Adjusted Sample

339

0.4675

0.6509

0.0010

0.8010

🧠 Insights

Small sample sizes may fail to detect real effects even when they exist.

Properly powered experiments reduce Type II errors.

Visualization is critical to communicate uncertainty, effect size, and group differences.

📁 Files Included

ab_test_power.R: Full reproducible R script

README.md: This overview

Visual plots included in project repository

📬 Contact

Created by Luke WamalwaFeel free to connect on GitHub or submit issues and suggestions.

