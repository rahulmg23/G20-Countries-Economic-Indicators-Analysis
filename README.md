# Global Economic Indicators Analysis

Exploring key economic trends and global development indicators such as GDP, GNI, Inflation, FDI, Literacy, and more — to understand how various macroeconomic factors influence growth and sustainability across countries.

---

## Table of Contents
- [Overview](#overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Tools & Technologies](#tools--technologies)
- [Project Structure](#project-structure)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Research Questions & Insights](#research-questions--insights)
- [Visualizations](#visualizations)
- [How to Run This Project](#how-to-run-this-project)
- [Key Findings](#key-findings)
- [Future Scope](#future-scope)
- [Author & Contact](#author--contact)

---

## Overview
This project performs a **comprehensive exploratory data analysis (EDA)** of global economic indicators using Python.  
It identifies relationships among GDP, inflation, literacy, and investment trends, helping policymakers, analysts, and students understand **economic growth drivers** and **development disparities**.

By leveraging **data-driven insights**, we aim to reveal how interconnected global economies are — and what patterns shape financial health and human progress.

---

## Business Problem
Economic indicators influence critical decisions such as:
- **Government policies** for sustainable growth and trade.
- **Investment strategies** in emerging and developed markets.
- **Education and infrastructure planning** for developing nations.

This project aims to:
1. Analyze correlations between GDP, GNI, inflation, and other indicators.
2. Discover trends that highlight economic development patterns.
3. Compare the impact of FDI and exports on overall growth.
4. Understand socioeconomic factors (like literacy and employment) affecting stability.

---

## Dataset
**Source:** World Development Indicators (manually curated / CSV file)  
**Records:** 114 rows × 22 columns  
**Time Period:** 2000–2023  

| Column Name | Description |
|--------------|-------------|
| Country | Country name |
| Year | Year of record |
| GDP | Gross Domestic Product |
| GNI | Gross National Income |
| Inflation rate | Annual inflation (%) |
| Unemployment rate | % of workforce unemployed |
| Poverty rate | % population below poverty line |
| Life expectancy | Average life expectancy |
| Literacy rate | Literacy rate (%) |
| FDI | Foreign Direct Investment inflows |
| Exports / Imports | Trade performance metrics |
| Agricultural indices | Land use & production values |

---

## ools & Technologies
- **Language:** Python 
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, SciPy  
- **Visualization:** Correlation Heatmaps, Pair Plots, Trend Charts  
- **Environment:** Jupyter Notebook  
- **Version Control:** GitHub  

---

## Data Cleaning & Preparation
Steps performed before analysis:
- Removed **duplicate columns** (`GDP_BN`, `GNI_BN`, `FDI_BN`, etc.)
- Converted **Year** column to `datetime` type.
- Handled **missing values** using interpolation & mean imputation.
- Dropped **irrelevant or redundant columns**.
- Checked for **outliers** and distribution skews using boxplots.
- Normalized numerical columns where required.

---

## Exploratory Data Analysis (EDA)
The EDA focused on identifying **patterns, anomalies, and relationships** between economic variables.

### Key Analyses Conducted:
1. **Correlation Analysis:**  
   Examined how GDP, GNI, inflation, and FDI relate.  
   → *Strong positive correlation between GDP & GNI (≈ 1.00)*  
   → *Negative correlation between Inflation & Life Expectancy (-0.45)*  

2. **Trend Analysis:**  
   Visualized year-over-year changes in GDP and Inflation.

3. **Distribution Analysis:**  
   Identified skewness in FDI and Poverty Rate using histograms.

4. **Outlier Detection:**  
   Boxplots revealed extreme FDI inflow values in developing nations.

---

## Research Questions & Insights
| Research Question | Insight |
|-------------------|----------|
| Does GDP strongly correlate with GNI? | Yes, correlation ≈ 1.00 |
| Is inflation inversely related to life expectancy? | Yes, moderate negative correlation |
| Does FDI boost exports? | ⚖️ Weak positive correlation found |
| Are literacy rates linked to unemployment reduction? |  Moderate correlation observed |
| Which countries show best GDP–Inflation balance? | Developed economies like the US, Japan, Germany |

---

## Visualizations
-  **Correlation Heatmap:** Shows strong relationships between GDP, GNI, and FDI.  
-  **Trend Charts:** GDP vs. Year, FDI vs. Year.  
-  **Boxplots:** Highlighting outliers in inflation and unemployment.  
-  **Pairplots:** Relationships among social and economic indicators.


---

## Key Findings

GDP and GNI show near-perfect correlation (1.00) → strong economic consistency.

Inflation tends to negatively affect life expectancy and GDP growth.

FDI inflows correlate positively with exports, suggesting global investment supports trade.

Unemployment and poverty rates are interlinked with education and infrastructure gaps.

Developed nations show stable inflation and strong GNI, while emerging economies exhibit volatility.

## Future Scope

Expand analysis to 200+ countries with live World Bank APIs.

Integrate Machine Learning for GDP prediction based on multiple indicators.

Perform cluster analysis to group countries by economic similarity.

👨‍💻 Author & Contact
Rahul Googikoll
📍 Goa, India
💼 Java Full Stack Developer | Aspiring Data Analyst & Data Engineer
📧 Email: raulgoogikoll23@gmail.com
🔗 LinkedIn
🔗 GitHub
