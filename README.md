# Re-analysis in Python of a systematic review and meta-analysis: Global prevalence of gaming disorder

By: Mariana Lopes Peixe, r1125391

Course: Programming for Humanities [F0BR0a] - KU Leuven

Academic year: 2025-2026


## Introduction
Gaming Disorder (GD) has gained significant clinical attention, culminating in its inclusion in the 11th revision of the International Classification of Diseases (ICD-11). In 2021, Stevens et al. published a systematic review and meta-analysis on the global prevalence of GD, utilizing the software Meta-Essentials to report a global pooled prevalence of 3.05%.

For a current Meta-Analysis academic, I did a data audit and re-analysis of the Stevens et al. (2021) dataset using R (via the `metafor` package). Due to corrections during the data extraction phase, the R-based re-analysis yielded a slightly higher global pooled prevalence of 3.15%. While working on that project, I got curious as to how that data analysis could be done using Python and if that would change the results.
As a result, the current project, developed for the "Programming for Humanities" course, aims to translate this into Python. By replicating the previous R scripts using Python's data science stack (`pandas`, `seaborn`, `statsmodels`), this project serves as a methodological comparison across three distinct analytical environments:
1. The original meta-analysis by Stevens et al. (Meta-Essentials).
2. The previous data audit and re-analysis (R).
3. The current computational translation (Python).

The objectives are to verify that Python can replicate the R-based mathematical findings, generate aditional comparative data visualizations (graphics), and conduct a sensitivity analysis restricted to representative samples (Type 1 studies).

**Methodological Note & References:**
The mathematical formulas utilized in this notebook for data transformation (logits and variance) are the ones used by Stevens et al. (2021). These formulas were previously coded in R and are now adapted for Python. To replicate the Random-Effects Model without R's `metafor` package, the official documentation for Python's `statsmodels.stats.meta_analysis` module was consulted, specifically utilizing the `combine_effects` function. Since we did not learn about the `statsmodels`in class, this was a process of trial and error.

Documentation for `statsmodels.stats.meta_analysis`: https://www.statsmodels.org/dev/generated/statsmodels.stats.meta_analysis.combine_effects.html 

To help edit the Markdown text this “cheat sheet” was used: https://www.ibm.com/docs/en/db2-event-store/2.0.0?topic=notebooks-markdown-jupyter-cheatsheet 
