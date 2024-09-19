# Statistical-Analysis-of-F1-Driver-Dataset #

Project Overview
This project aims to analyze and identify the factors that significantly contribute to a Formula 1 driver becoming a champion. Specifically, we explore the relationships between three performance metrics:
- Win Rate
- Pole Rate
- Points Per Entry

The goal is to determine whether these features have a significant impact on the likelihood of a driver becoming a champion. We use both exploratory data analysis (EDA) and statistical tests (bootstrap and Z-tests) to validate our findings.

### Dataset ###
The dataset used in this project is from Kaggle, containing historical data about Formula 1 drivers and their performance statistics. You can find the dataset [here](https://www.kaggle.com/datasets/petalme/f1-drivers-dataset).

### Project Structure ###
The project consists of the following key steps:
#### 1. Exploratory Data Analysis (EDA): ####
  - Objective: To get an initial understanding of the data distribution for the performance metrics of champions vs. non-champions.
  - We use visualizations (bar charts, histograms) to compare the distributions of Win Rate, Pole Rate, and Points Per Entry for champions and non-champions.
#### 2. Hypothesis Formulation: ####
  - Null Hypothesis (H₀): Win Rate, Pole Rate, and Points Per Entry have no significant effect on a driver becoming a champion.
  - Alternative Hypothesis (H₁): Win Rate, Pole Rate, and Points Per Entry significantly affect whether a driver becomes a champion.
#### 3. Bootstrap Analysis: ####
  - Bootstrap Sampling: We perform non-parametric bootstrap sampling to estimate confidence intervals for the mean values of Win Rate, Pole Rate, and Points Per Entry for both champions and non-champions.
  - Objective: To check whether the confidence intervals of the two groups overlap and assess the practical significance of the difference.
#### 4. Z-Test: ####
  - We then conduct Z-tests to check the statistical significance of the difference in means between champions and non-champions for each of the performance metrics.
  - The Z-test allows us to calculate the Z-scores and p-values to statistically validate or reject the null hypothesis.

#### Results: ####
**Bootstrap Results:** The bootstrap analysis showed that Points Per Entry has a significant and meaningful difference between champions and non-champions. However, the confidence intervals for Win Rate and Pole Rate overlapped, suggesting that these features may not have a large practical impact.

**Z-Test Results:** The Z-test indicated that all three features (Win Rate, Pole Rate, and Points Per Entry) are statistically significant with very low p-values. However, the Z-test might be sensitive to large sample sizes and normality assumptions, leading to statistical significance even when the practical difference is small.

### Conclusion: ###
`Points Per Entry` is the most important feature that differentiates champions from non-champions, both statistically and practically.

While `Win Rate` and `Pole Rate` are statistically significant according to the Z-test, the bootstrap analysis suggests that they may not be practically meaningful in determining a champion.
Therefore, `Points Per Entry` should be considered the strongest predictor for a driver becoming a Formula 1 champion.

### Key Python Libraries Used: ###
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical calculations.
- `plotly`: For interactive visualizations.
- `scipy.stats`: For statistical tests (Z-tests).
