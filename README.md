# Preregistration Protocol: Effect of Public Self-Review on Citation Inflow
**Author:** Amir Omidvarnia  

![Citation report](cover.png)

**Website:** https://www.citation-report.com
---

## Research Question
This preregistered study examines whether public self-critical reviews of a researcher's own peer-reviewed journal articles influence subsequent citation inflow. It is explicitly an n=1 single-case natural experiment, with the focal researcher as both subject and investigator. The intervention comprises self-critical commentaries posted publicly on LinkedIn. Monthly citation trajectories for all eligible journal articles are analyzed using interrupted time-series regression, benchmarked against 100 randomly selected external control authors from engineering and related fields. The study does not seek generalizability, but aims to provide a transparent, well-documented workflow for future replication.  

---

## Hypotheses
- **Primary hypothesis:** Public self-review reduces citation inflow for the focal author.  
- **Null hypothesis:** No change in citation trends after self-review intervention.  
- **Alternative hypothesis:** Public self-review increases citation inflow.  

### Interpretive Extension
Evidence in favor of the primary hypothesis would support the claim that research openness, in the form of self-review, is not welcomed or rewarded by the scientific community because it carries a citation cost for the researcher.  

---

## Study Design
This is an **observational, interrupted time-series study**.  

- **Unit of analysis:** monthly new citations across my publications (author-level aggregate).  
- **Publications:** 15 first-author peer-reviewed journal articles ([Google Scholar](https://scholar.google.com/citations?user=BAZiv8sAAAAJ&hl=en)).  
- **Inclusion threshold:** each included item had >10 citations at the intervention (Aug 2025).  
- **Pre-intervention period:** January 2022 – July 2025.  
- **Intervention:** August 2025, date of first LinkedIn self-review post ([LinkedIn post](https://www.linkedin.com/feed/update/urn:li:activity:7363176261566767106/)).  
- **Post-intervention period:** 24 months (Aug 2025 – Aug 2027).  
- **Primary analysis:** 12 months post (Aug 2025 – Jul 2026).  
- **Secondary analysis:** 24 months post (Aug 2025 – Jul 2027).  
- **Final analysis:** 36 months post (Aug 2025 – Jul 2028).  
- **Sampling:** All citing works indexed in [OpenAlex](https://openalex.org/authors/A5080711096).  
- **Exclusion:** self-citations excluded from primary analysis.
- **Citation report platform**: https://www.citation-report.com

---

## Key Variables
- **Outcome variable:** Monthly count of new citations (excluding self-citations).  
- **Predictor:** Intervention indicator (0 = pre, 1 = post).  
- **Covariates (robustness):**  
  - Calendar month indicators (seasonality).  
  - Months with new publications by me (to control for bursts).  

---

## Background and Literature
Previous research on open science shows that practices like open access and open data are often associated with neutral or positive citation effects (Christensen et al., 2019; Zhang & Ma, 2023; Borregaard et al., 2024).  
Studies on formal criticism suggest that papers receiving critical comments are often more cited (Radicchi, 2012; Bozzo et al., 2024).  
Self-citation patterns are widely studied (King et al., 2017), but no study has tested whether self-criticism of one’s own work affects citation inflow.  

---

## Analysis Plan

### Descriptive Analysis
- Plot monthly citations (Jan 2022 – Aug 2028).  
- Mark intervention (Aug 2025).  
- Overlay 3-month moving average.  

### Interrupted Time-Series
Let:  

- $Y_t$ = citations in month $t$  
- $D_t = 0$ before Aug 2025, $1$ after  
- $(t - T_0)D_t = 0$ pre, else counts months since intervention  

Model:  

$$
Y_t = \beta_0 + \beta_1 t + \beta_2 D_t + \beta_3 (t - T_0)D_t + \varepsilon_t
$$

- $\beta_2 < 0$: immediate drop  
- $\beta_3 < 0$: slower growth post-intervention  
- Residual autocorrelation corrected (Newey–West or ARIMA errors).  

### Rate Ratio with Poisson Test
Predict monthly counts $\hat{Y}_t$ from pre-trend regression.  

Observed total in $k$ post months:  

$$
O_k = \sum_{t=T_0}^{T_0+k-1} Y_t
$$

Expected total:  

$$
E_k = \sum_{t=T_0}^{T_0+k-1} \hat{Y}_t
$$

Rate Ratio:  

$$
RR = \frac{O_k}{E_k}
$$

Test: Under the null, $O_k \sim \text{Poisson}(E_k)$.  

Two-sided p-value:  

$$
p =
\begin{cases}
2 \cdot P(X \leq O_k \mid X \sim \text{Poisson}(E_k)), & O_k \leq E_k \\
2 \cdot P(X \geq O_k \mid X \sim \text{Poisson}(E_k)), & O_k > E_k
\end{cases}
$$

---

## Placebo and Sensitivity Analyses
- **Placebo:** Pretend intervention at Feb 2025.  
- **Sensitivity 1:** Include self-citations.  
- **Sensitivity 2:** Exclude months with new publications.  
- **Sensitivity 3:** Lagged intervention start (Oct 2025).  

---

## Decision Rules
- **Primary (12 months):** If $RR \leq 0.85$ and $p \leq 0.05$ → evidence of decline.  
- **Final (36 months):** Repeat decision rule over 3-year window.  
- **Secondary:** Significant negative $\beta_2$ or $\beta_3$ in ITS supports hypothesis.  

---

## Timeline
- **Preregistration filed:** before analysis of post-intervention data.  
- **Primary analysis:** August 2026.  
- **Secondary analysis:** August 2027.  
- **Final analysis:** August 2028.  

---

## Data Sharing and Transparency
- Data, codes, and analysis results on [GitHub](https://github.com/omidvarnia).  
- Analysis scripts (Python/Jupyter notebooks).  
- Deviations documented in [OSF](https://osf.io/zp9q3/).  

---

## Benefits of Preregistration
This preregistration reduces hindsight bias, enhances transparency, and secures intellectual priority.  
It provides a permanent, timestamped record of this novel research question.  

---

## References
- Christensen G, Dafoe A, Miguel E, Moore D, Rose AK. *Open science practices are on the rise*. PLOS Biology, 2019.  
- Zhang Y, Ma L. *Data sharing policies and citation impact: Evidence from China*. Journal of Informetrics, 2023.  
- Borregaard MK, et al. *The academic impact of open science: A scoping review*, 2024.  
- Radicchi F. *Comments on scientific articles: Influences on citations and impact*. arXiv:1209.4997, 2012.  
- Bozzo A, et al. *Do critical letters affect citation trajectories?* arXiv:2412.02809, 2024.  
- King MM, et al. *Men set their own cites high: Gender and self-citation*. arXiv:2109.09192, 2017.  




