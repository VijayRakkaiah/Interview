# Statistics Interview Questions & Answers 

--- 

## Q1. How is the statistical significance of an insight assessed?

**Detailed Answer:**  
Statistical significance is assessed using **hypothesis testing**. We set up:  
- **Null hypothesis (H₀):** No effect or relationship.  
- **Alternative hypothesis (H₁):** There is an effect or relationship.  

A test statistic (like t, z, or χ²) is calculated, and a **p-value** is obtained. If the p-value is **less than the significance level (α, usually 0.05)**, we reject H₀ and conclude the result is statistically significant. Confidence intervals can also help assess significance—if the interval doesn’t contain the null value, the effect is significant.  

**Short & Sweet:**  
Significance = check **p-value < 0.05** or CI not containing null.

---

## Q2. Where are long-tailed distributions used? 

**Detailed Answer:**  
Long-tailed distributions (like Pareto, log-normal, or power-law) describe data where **rare, extreme events** have a disproportionately large impact. They are used in:  
- **Finance & Insurance:** Modeling risk, catastrophic losses.  
- **Internet & Social Media:** Website traffic, viral content.  
- **Economics:** Wealth distribution, inequality.  
- **Reliability Engineering:** Rare failures, defect modeling.  

**Short & Sweet:**  
Used where **rare events dominate outcomes** (finance, web, risk).

---

## Q3. What is the central limit theorem?

**Detailed Answer:**  
The **Central Limit Theorem (CLT)** states: For large enough sample size (n > 30), the **distribution of sample means** approaches a **normal distribution**, regardless of the original population’s shape (if variance is finite).  

- Sample mean → normal distribution.  
- Mean = population mean.  
- SD = σ/√n.  

**Short & Sweet:**  
CLT: **Sample means → normal distribution** as n grows.

---

## Q4. What is observational and experimental data in Statistics?

**Detailed Answer:**  
- **Observational Data:** Collected without intervention. Example: health surveys. Weakness: can’t prove causality.  
- **Experimental Data:** Collected by manipulating variables. Example: clinical trials. Strength: causality detection.  

**Short & Sweet:**  
- **Observational:** Just watch.  
- **Experimental:** Manipulate → causality.

---

## Q5. What is meant by mean imputation for missing data? Why is it bad?

**Detailed Answer:**  
**Mean imputation** = replacing missing values with the variable’s mean. Problems:  
- Underestimates variability.  
- Distorts correlations/regression.  
- Ignores missingness uncertainty.  

Alternatives: median, regression, multiple imputation.  

**Short & Sweet:**  
Mean imputation = fill with average. Bad → **bias & lost variance**.

---

## Q6. What is an outlier? How can outliers be determined in a dataset?

**Detailed Answer:**  
An **outlier** is an extreme/unusual observation.  
Detection methods:  
- **Z-score** (>3 or <-3).  
- **IQR method** (outside Q1–1.5×IQR or Q3+1.5×IQR).  
- **Visual:** Boxplot, scatterplot.  

**Short & Sweet:**  
Outlier = extreme value. Detect via **Z-score or IQR**.

---

## Q7. Bottom of Form

**Detailed Answer:**  
This looks like a misformatted question. No statistical meaning.  

**Short & Sweet:**  
Ignore—invalid question.

---

## Q8. How is missing data handled in statistics?

**Detailed Answer:**  
Methods:  
- **Deletion:** Listwise, pairwise.  
- **Imputation:** Mean, median, regression, multiple.  
- **Model-based:** EM algorithm, likelihood.  

Depends on **MCAR, MAR, MNAR**.  

**Short & Sweet:**  
Handle by **deletion, imputation, or model-based methods**.

---

## Q9. What is exploratory data analysis?

**Detailed Answer:**  
**EDA** = initial investigation of data with statistical summaries and visualizations. Purpose:  
- Discover patterns.  
- Spot anomalies/outliers.  
- Test assumptions before modeling.  

**Short & Sweet:**  
EDA = **summarize + visualize data** before modeling.

---

## Q10. What is the meaning of selection bias?

**Detailed Answer:**  
Selection bias = when chosen sample is **not representative** of population, leading to flawed conclusions. Example: surveying only internet users.  

**Short & Sweet:**  
Selection bias = **non-representative sample**.

---

## Q11. What are the types of selection bias in statistics?

**Detailed Answer:**  
Types include:  
- **Sampling bias** – poor sampling method.  
- **Attrition bias** – dropout from study.  
- **Survivorship bias** – only successful cases studied.  
- **Exclusion bias** – excluding groups incorrectly.  

**Short & Sweet:**  
Types: **sampling, attrition, survivorship, exclusion**.

---

## Q12. What is the meaning of an inlier?

**Detailed Answer:**  
An **inlier** is a data point that lies within expected range of values, but may still be unusual compared to model fit. Example: fits distribution but not model prediction.  

**Short & Sweet:**  
Inlier = data within range but not fitting model well.

---

## Q13. What is the probability of throwing two fair dice when the sum is 5 and 8?

**Detailed Answer:**  
- Total outcomes = 36.  
- Sum = 5: (1,4),(2,3),(3,2),(4,1) → 4 outcomes. → 4/36 = 1/9.  
- Sum = 8: (2,6),(3,5),(4,4),(5,3),(6,2) → 5 outcomes. → 5/36.  

**Short & Sweet:**  
P(sum=5)=1/9, P(sum=8)=5/36.

---

## Q14. State the case where the median is a better measure when compared to the mean.

**Detailed Answer:**  
Median is better when data is **skewed or has outliers**. Example: income data—few billionaires inflate mean, median shows central tendency better.  

**Short & Sweet:**  
Median > Mean when **data is skewed or has outliers**.

---

## Q15. Can you give an example of root cause analysis?

**Detailed Answer:**  
Root cause analysis (RCA) = finding underlying cause. Example: Manufacturing defects—use **5 Whys**:  
- Why machine stopped? → Overheated.  
- Why overheated? → Lubrication failed.  
- Why failed? → Maintenance skipped.  

**Short & Sweet:**  
RCA = drill down (“5 Whys”) to find **true cause**.

---

## Q16. What is the meaning of six sigma in statistics?

**Detailed Answer:**  
**Six Sigma** = data-driven methodology for quality improvement. A process at Six Sigma has only **3.4 defects per million opportunities (DPMO)**. Based on reducing variability and defects using DMAIC (Define, Measure, Analyze, Improve, Control).  

**Short & Sweet:**  
Six Sigma = quality method aiming for **3.4 defects per million**.

---

## Q17. What is DOE?

**Detailed Answer:**  
DOE = **Design of Experiments**, a structured statistical method to plan, conduct, and analyze experiments efficiently. Used to identify factor effects and optimize outcomes.  

**Short & Sweet:**  
DOE = **planned experiments** to study factors/effects.

---

## Q18. What is the meaning of KPI in statistics?

**Detailed Answer:**  
KPI = **Key Performance Indicator**, measurable value that indicates how effectively objectives are achieved. Example: churn rate, accuracy, revenue growth.  

**Short & Sweet:**  
KPI = **performance metric** to track goals.

---

## Q19. What type of data does not have a log-normal distribution or a Gaussian distribution?

**Detailed Answer:**  
Categorical/nominal data (like gender, colors, types) do not follow Gaussian or log-normal distributions because these apply only to continuous numerical data.  

**Short & Sweet:**  
**Categorical data** (non-numeric) isn’t Gaussian/log-normal.

---

## Q20. What is the Pareto principle?

**Detailed Answer:**  
Pareto Principle (80/20 rule): **80% of outcomes come from 20% of causes**. Example: 80% of sales from 20% of customers.  

**Short & Sweet:**  
Pareto = **80/20 rule**.

---

## Q21. What is the meaning of the five-number summary in Statistics?

**Detailed Answer:**  
Five-number summary includes:  
1. Minimum  
2. Q1 (25th percentile)  
3. Median (Q2)  
4. Q3 (75th percentile)  
5. Maximum  

Used in boxplots to describe data distribution.  

**Short & Sweet:**  
5-number summary = **min, Q1, median, Q3, max**.

---

## Q22. What are population and sample in Inferential Statistics, and how are they different?

**Detailed Answer:**  
- **Population:** Entire group of interest (all people in a country).  
- **Sample:** Subset of population studied to infer about population.  

Difference: Population = whole; Sample = part.  

**Short & Sweet:**  
Population = **whole group**, Sample = **subset used for inference**.

---

## Q23. What are quantitative data and qualitative data?

**Detailed Answer:**  
- **Quantitative:** Numerical values (age, salary).  
- **Qualitative:** Categorical values (color, brand).  

**Short & Sweet:**  
Quantitative = numbers, Qualitative = categories.

---

## Q24. What is Mean?

**Detailed Answer:**  
Mean = sum of values ÷ number of values. Sensitive to outliers.  

**Short & Sweet:**  
Mean = **average value**.

---

## Q25. What is the meaning of standard deviation?

**Detailed Answer:**  
Standard deviation (σ) measures how spread out data is around the mean. Higher = more variability. Formula: √variance.  

**Short & Sweet:**  
SD = **spread of data around mean**.

---

## Q26. What is a bell-curve distribution?

**Detailed Answer:**  
Bell curve = shape of **normal distribution**: symmetric, unimodal, mean=median=mode.  

**Short & Sweet:**  
Bell curve = **normal distribution shape**.

---

## Q27. What is skewness?

**Detailed Answer:**  
Skewness measures asymmetry of data distribution.  
- Positive skew = right tail longer.  
- Negative skew = left tail longer.  

**Short & Sweet:**  
Skewness = **asymmetry** of distribution.

---

## Q28. What is kurtosis?

**Detailed Answer:**  
Kurtosis measures **tailedness**:  
- High kurtosis → heavy tails, more outliers.  
- Low kurtosis → light tails.  

**Short & Sweet:**  
Kurtosis = **tail heaviness**.

---

## Q29. What is correlation?

**Detailed Answer:**  
Correlation measures strength/direction of relationship between two variables. Pearson’s r ranges -1 to +1.  

**Short & Sweet:**  
Correlation = **how variables move together**.

---

## Q30. What are left-skewed and right-skewed distributions?

**Detailed Answer:**  
- **Left-skewed (negative):** Tail on left, mean < median.  
- **Right-skewed (positive):** Tail on right, mean > median.  

**Short & Sweet:**  
Left = tail left (mean<median), Right = tail right (mean>median).

---

## Q31. What is the difference between Descriptive and Inferential Statistics?

**Detailed Answer:**  
- **Descriptive:** Summarize data (mean, charts).  
- **Inferential:** Use sample data to infer about population (hypothesis testing, regression).  

**Short & Sweet:**  
Descriptive = describe data, Inferential = infer about population.

---

## Q32. What are the types of sampling in Statistics?

**Detailed Answer:**  
Types:  
- Random sampling.  
- Stratified sampling.  
- Cluster sampling.  
- Systematic sampling.  
- Convenience sampling.  

**Short & Sweet:**  
Types: random, stratified, cluster, systematic, convenience.

---

## Q33. What is the meaning of covariance?

**Detailed Answer:**  
Covariance = measure of how two variables vary together. Positive = move same direction; Negative = opposite.  

**Short & Sweet:**  
Covariance = **joint variability of two variables**.

---

## Q34. Imagine Jeremy took a test (mean=160, SD=15, z=1.20). What is his score?

**Detailed Answer:**  
Formula: X = μ + zσ = 160 + (1.2×15) = 160 + 18 = 178.  

**Short & Sweet:**  
Jeremy’s score = **178**.

---

## Q35. If a distribution is skewed to the right and has median 20, will the mean be greater or less?

**Detailed Answer:**  
Right-skewed: mean > median. So mean > 20.  

**Short & Sweet:**  
Mean > 20.

---

## Q36. What is Bessel's correction?

**Detailed Answer:**  
Bessel’s correction adjusts sample variance calculation by dividing by (n-1) instead of n to remove bias.  

**Short & Sweet:**  
Bessel’s correction = divide by (n-1) for sample variance.

---

## Q37. The standard normal curve has area 1 and is symmetric around 0. True or False?

**Detailed Answer:**  
True. Standard normal curve = total area 1, symmetric about 0.  

**Short & Sweet:**  
True.

---

## Q38. High correlation between sleep and productivity. What can be inferred?

**Detailed Answer:**  
Correlation shows association, not causation. Cannot conclude sleep causes productivity without experiment.  

**Short & Sweet:**  
Correlation ≠ causation.

---

## Q39. Relationship between confidence level and significance level?

**Detailed Answer:**  
Confidence level = 1 - significance level (α). Example: 95% CI ↔ α=0.05.  

**Short & Sweet:**  
Confidence = 1 - α.

---

## Q40. Regression line y=100+2x (apples vs oranges). If x ↑1?

**Detailed Answer:**  
Slope=2 → For each extra orange, apples increase by 2.  

**Short & Sweet:**  
1 orange ↑ → apples ↑ by 2.

---

## Q41. What types of variables are used for Pearson’s correlation coefficient?

**Detailed Answer:**  
Used for continuous, numerical variables measured on interval/ratio scale.  

**Short & Sweet:**  
Pearson’s r → continuous numeric variables.

---

## Q42. In scatter diagram, line drawn above/below regression line is?

**Detailed Answer:**  
It’s the **residual line** or error term (distance between observed and predicted).  

**Short & Sweet:**  
Called **residual**.

---

## Q43. Examples of symmetric distribution?

**Detailed Answer:**  
Normal distribution, uniform distribution, t-distribution.  

**Short & Sweet:**  
Examples: normal, uniform, t.

---

## Q44. Where is inferential statistics used?

**Detailed Answer:**  
Used when making predictions/inferences about population from sample (surveys, experiments).  

**Short & Sweet:**  
Used to **generalize sample results to population**.

---

## Q45. Relationship between mean and median in a normal distribution?

**Detailed Answer:**  
In normal distribution, mean = median = mode.  

**Short & Sweet:**  
Equal.

---

## Q46. Difference between quartiles Q1, Q2, Q3?

**Detailed Answer:**  
- Q1 = 25th percentile.  
- Q2 = 50th (median).  
- Q3 = 75th percentile.  

**Short & Sweet:**  
Q1=25%, Q2=50%, Q3=75%.

---

## Q47. How do standard error and margin of error relate?

**Detailed Answer:**  
Margin of error = critical value × standard error.  

**Short & Sweet:**  
MoE = critical × SE.

---

## Q48. What is one sample t-test?

**Detailed Answer:**  
A statistical test comparing sample mean to known/hypothesized population mean.  

**Short & Sweet:**  
Test if sample mean = population mean.

---

## Q49. What is an alternative hypothesis?

**Detailed Answer:**  
Alternative hypothesis (H₁) = statement we want evidence for (effect exists).  

**Short & Sweet:**  
H₁ = effect/difference exists.

---

## Q50. Given left-skewed dist (median=60), what about mean and mode?

**Detailed Answer:**  
Left skew: mean < median < mode. So mean <60, mode >60.  

**Short & Sweet:**  
Mean < 60 < Mode.

---

## Q51. What are types of biases in sampling?

**Detailed Answer:**  
- Selection bias  
- Non-response bias  
- Undercoverage bias  
- Survivorship bias  

**Short & Sweet:**  
Types: selection, non-response, undercoverage, survivorship.

---

## Q52. Scenarios where outliers are kept?

**Detailed Answer:**  
- Genuine extreme values (income of billionaires).  
- When modeling rare events.  
- Domain-critical outliers (fraud detection).  

**Short & Sweet:**  
Keep outliers when **they’re real and meaningful**.

---

## Q53. Procedure to measure length of all sharks in world?

**Detailed Answer:**  
Use sampling: random sample of sharks across regions → measure → use inferential stats to estimate global distribution.  

**Short & Sweet:**  
Use **random sampling + inference**.

---

## Q54. How does width of confidence interval change with sample size?

**Detailed Answer:**  
Larger sample size → smaller standard error → narrower CI.  

**Short & Sweet:**  
More n → narrower CI.

---

## Q55. Meaning of degrees of freedom (DF) in statistics?

**Detailed Answer:**  
DF = number of independent values that can vary when estimating parameters. Example: variance → n-1.  

**Short & Sweet:**  
DF = **independent values free to vary**.

---

## Q56. How to calculate p-value using Excel?

**Detailed Answer:**  
Use functions:  
- `T.TEST()` for t-test.  
- `CHISQ.TEST()` for chi-square.  
- `Z.TEST()` for z-test.  

**Short & Sweet:**  
Excel functions: T.TEST, CHISQ.TEST, Z.TEST.

---

## Q57. What is the law of large numbers?

**Detailed Answer:**  
As sample size increases, sample mean converges to population mean.  

**Short & Sweet:**  
Larger n → sample mean ≈ population mean.

---

## Q58. Types of kurtosis?

**Detailed Answer:**  
- Mesokurtic (normal).  
- Leptokurtic (heavy tails).  
- Platykurtic (light tails).  

**Short & Sweet:**  
Types: meso, lepto, platy.

---

## Q59. Real-life examples of normal distribution?

**Detailed Answer:**  
Heights, IQ scores, measurement errors, test scores.  

**Short & Sweet:**  
Examples: heights, IQ, errors.

---

## Q60. What is robust statistics?

**Detailed Answer:**  
Methods resistant to violations of assumptions/outliers. Example: median instead of mean, MAD instead of SD.  

**Short & Sweet:**  
Robust stats = **resistant to outliers/assumptions**.

---

## Q61. Difference between descriptive and inferential statistics?

**Detailed Answer:**  
(Repeated Q31). Descriptive = summarize. Inferential = predict.  

**Short & Sweet:**  
Descriptive = describe, Inferential = infer.

---

## Q62. Explain a real-life situation where correlation is used.

**Detailed Answer:**  
Example: Studying correlation between exercise hours and cholesterol levels.  

**Short & Sweet:**  
Correlation: **exercise vs cholesterol**.

---

## Q63. Types of correlation?

**Detailed Answer:**  
- Positive correlation.  
- Negative correlation.  
- Zero correlation.  

**Short & Sweet:**  
Positive, Negative, Zero.

---

## Q64. What is t-test?

**Detailed Answer:**  
Statistical test comparing means: one-sample, two-sample, paired.  

**Short & Sweet:**  
t-test = compare means.

---

## Q65. Null and alternative hypothesis?

**Detailed Answer:**  
- Null (H₀): no effect/difference.  
- Alternative (H₁): effect/difference exists.  

**Short & Sweet:**  
H₀=no effect, H₁=effect.

---

## Q66. Steps in hypothesis testing?

**Detailed Answer:**  
1. Define H₀, H₁.  
2. Choose significance α.  
3. Compute test statistic.  
4. Find p-value.  
5. Compare with α → reject/accept H₀.  

**Short & Sweet:**  
Steps: state H₀/H₁ → α → test → p-value → decision.

---

## Q67. What is non-parametric test?

**Detailed Answer:**  
Statistical test not assuming data follows normal distribution. Example: Mann-Whitney U, Kruskal-Wallis.  

**Short & Sweet:**  
Non-parametric = no distribution assumption.

---

## Q68. Why is standard deviation better than variance?

**Detailed Answer:**  
Variance is squared units, harder to interpret. SD in same units as data → more intuitive.  

**Short & Sweet:**  
SD better → **same units as data**.

---

## Q69. Define inferential statistics.

**Detailed Answer:**  
Branch of stats making predictions/inferences about population based on sample data. Uses estimation, hypothesis testing, regression.  

**Short & Sweet:**  
Inferential = **generalize sample → population**.

---

## Q70. Difference between 1-tailed and 2-tailed tests?

**Detailed Answer:**  
- One-tailed: tests effect in one direction only.  
- Two-tailed: tests effect in both directions.  

**Short & Sweet:**  
1-tailed = one direction, 2-tailed = both.

---

## Q71. What is time series?

**Detailed Answer:**  
Time series = sequence of observations recorded over time intervals. Used in forecasting, trend analysis.  

**Short & Sweet:**  
Time series = **data over time**.

---

## Q72. Example of time series.

**Detailed Answer:**  
Stock prices daily, monthly rainfall, quarterly sales.  

**Short & Sweet:**  
Examples: stock prices, sales, weather.

---

## Q73. Steps in time series analysis?

**Detailed Answer:**  
1. Collect/clean data.  
2. Plot & visualize.  
3. Decompose (trend, seasonality, residual).  
4. Build models (ARIMA, ETS).  
5. Forecast & validate.  

**Short & Sweet:**  
Steps: collect → decompose → model → forecast.

---

## Q74. Uses of time series.

**Detailed Answer:**  
Used in forecasting demand, stock market, weather prediction, economics, business planning.  

**Short & Sweet:**  
Uses: forecasting **sales, stocks, weather**.

---



