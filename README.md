# **Global Diabetes Diagnosis Gap Insights – Project Overview**

**The goal of this project is to identify high-need regions with the largest diagnosis gaps in diabetes care and translate these findings into recommendations for public health planning and market access strategy.**

Diabetes continues to rise globally, yet millions remain undiagnosed, leading to delayed treatment, higher mortality, and increasing healthcare costs. Using data from the **International Diabetes Federation (IDF) Diabetes Atlas, 11th Edition (2025)**, this analysis measures the scale of undiagnosed diabetes and highlights regions where early detection initiatives would yield the most significant outcomes.

To quantify this diagnosis gap, the analysis introduces a **Diagnosis Gap Rate**, which estimates the share of adults living with undiagnosed diabetes by combining disease prevalence and diagnostic coverage into a single comparable measure. This rate enables public health and healthcare stakeholders to identify high-need regions where targeted screening, awareness campaigns, or diagnostic programs could deliver measurable benefit.

---

## **Dataset Structure**

The dataset consolidates global indicators related to diabetes prevalence and diagnostic coverage, supported by additional derived fields created for analytical interpretation. Each observation represents a country-level estimate, including both raw epidemiological indicators and calculated measures for segmentation and visualisation. Regional groupings were derived and mapped in Python to enable broader cross-market analysis and comparison.

| **Field** | **Type** | **Source / Derived** | **Description** |
|------------|-----------|----------------------|-----------------|
| **Country** | Text | Original | Country name |
| **Region** | Text | Derived | Regional grouping mapped in Python for cross-market comparison |
| **Prevalence_Pct** | Float | Original | Estimated diabetes prevalence (%) |
| **Undiagnosed_Pct** | Float | Original | Proportion of adults with diabetes who remain undiagnosed (%) |
| **Unmet_Need_Score** | Float | Derived | Composite indicator representing the diagnosis gap rate (DGR) |
| **Prevalence_Bucket** | Text | Derived | Grouped prevalence (%) bands for matrix visualisation |
| **Undiagnosed_Bucket** | Text | Derived | Grouped undiagnosed (%) bands for matrix visualisation |
| **Cohort_Groups** | Text | Derived | Diagnostic maturity category (A–D) based on DGR range |

## **Cohort Groups and Definitions**

Conditional formatting across the visualisations is based on the **Diagnosis Gap Rate (DGR)**, which represents the estimated proportion of adults with diabetes who remain undiagnosed.  

To support interpretability and comparison, DGR values were classified into 4 cohorts (A–D) representing progressive levels of diagnostic maturity.  

| **Cohort** | **Range (DGR %)** | **Interpretation** |
|-------------|------------------|--------------------|
| **A – Critical** | ≥ 8% | Highest priority for intervention and monitoring |
| **B – High** | 5 – < 8% | Significant diagnostic gap; targeted improvement needed |
| **C – Moderate** | 3 – < 5% | Partial diagnostic coverage; maintain improvement momentum |
| **D – Lower** | < 3% | Strong diagnostic coverage; sustain best practices |

While these numeric ranges are not standardised across global policy literature, they reflect the categorical framing commonly used in public-health and market-access contexts to describe diagnostic readiness. The thresholds were analytically defined to enable consistent regional comparison and to align with real-world interpretations of diagnostic performance.

---
