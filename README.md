# ⚖️ A/B-Test-Power

**A/B Testing Power Analysis with Sample Size Adjustment in R**  
📊 *Simulated Binary Outcome Dataset | R Portfolio Project*

---

## 📁 Project Structure

This project demonstrates a step-by-step simulation and analysis of A/B testing under varying sample sizes.  
It showcases how small sample sizes can lead to inconclusive results and how adjusting sample size improves statistical power, p-values, and conversion rate estimation.

---

## 💡 Objectives

- Simulate small-sample A/B test data (binary outcomes)
- Calculate power using Cohen’s h and `pwr` package
- Estimate required sample size to achieve 80% power
- Compare small vs. adjusted samples in terms of:
  - ✅ P-values
  - ✅ Conversion rate differences
  - ✅ Statistical power
- Visualize results using multiple R libraries

---

## 🛠️ Tools & Libraries

- `pwr` for power and sample size calculation
- `dplyr` for data wrangling
- `ggplot2` for base visualization
- `ggstatsplot` for statistical visualizations
- `ggpubr` + `ggsignif` for annotated comparisons
- `ggpmisc` for trendlines with R² equations
- `gghighlight` for focused highlights
- `knitr` for summary tables

---

## 📊 Analysis Summary

| Stage            | Sample Size | Conv_A | Conv_B | P-value | Power  |
|------------------|-------------|--------|--------|---------|--------|
| Small Sample     | 50          | 0.6400 | 0.7200 | 0.7618  | 0.1899 |
| Adjusted Sample  | 339         | 0.4675 | 0.6509 | 0.0010  | 0.8010 |

---

## 📈 Visualizations

The following statistical plots were used to communicate findings:

- **ggstatsplot**: `ggbetweenstats()` for group comparisons with effect size and CI  
- **ggpubr**: `ggboxplot()` with jitter + significance annotations  
- **ggsignif**: bar plot with `geom_signif()` for visual hypothesis testing  
- **ggpmisc**: polynomial regression fits with `stat_poly_eq()`  
- **ggplot2**: trend lines, mean estimates with error bars  
- **Comparison plot** of p-values across sampling strategies

---

## 📌 Key Takeaways

- Small samples yielded inconclusive results (p > 0.05, power < 20%)
- With 339 observations, the experiment achieved **80% power**
- Conversion rate differences became statistically significant
- 📉 Inadequate sample sizes reduce test reliability and can lead to false negatives

---

## 📂 How to Run

1. Clone this repository  
2. Open `ab_test_power.R` in RStudio  
3. Run sections sequentially (or knit as `.html`)  
4. Required R version: `>= 4.3`  
5. Ensure required libraries are installed

---

## 📬 Contact

*Luke Wamalwa*  
[GitHub](https://github.com/lukahere007) | [LinkedIn](https://www.linkedin.com/in/your-profile/)  
This project is part of my **Data Science for Clinical Research** portfolio.

---

> 📜 Licensed under MIT License
