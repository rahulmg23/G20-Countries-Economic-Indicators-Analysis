<img width="932" height="724" alt="image" src="https://github.com/user-attachments/assets/29d7a281-d570-417e-8c29-99991f05c9d0" />
# G20 Countries Economic Indicators Analysis

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

## Tools & Technologies
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

--


    
   <img width="1410" height="990" alt="output_30_0" src="https://github.com/user-attachments/assets/ff1d6f6a-3be1-4272-b9b8-c0ec1919fdb9" />


This collection of histograms offers a powerful, data-driven narrative about the **Progressive but Unequal World**. It moves beyond simple metrics to reveal the deep structural differences between nations, providing a critical foundation for strategic policy and product decisions.

## Executive Summary: The Dual-Speed Global Economy

The global development landscape is one of stark contrasts. **Social welfare is converging**—most countries have achieved high marks in health, education, and basic infrastructure. However, **economic prosperity is heavily centralized and unequal**, with a few nations dominating wealth, investment, and productivity.

This "dual-speed" reality dictates unique challenges and opportunities: while product strategy can assume a globally literate and connected user base, investment strategy must contend with extreme concentrations of economic power.

---

## The Centralization of Wealth: Economic Health Indicators

**The Takeaway:** Global economic power is overwhelmingly centralized. The world's wealth distribution is a testament to the "Matthew Effect"—to those who have, more will be given.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (What it means for Business/Policy)** |
| --- | --- | --- |
| **GDP & GNI** | **Extreme Right Skew** | A small fraction of nations (the long tail) accounts for the vast majority of global wealth. **Strategic Focus:** Targeting product development and scaling for these mega-economies yields maximum immediate return. |
| **Poverty Rate** | **High Right Skew** | While most enjoy low poverty, the long tail represents a critical challenge. **Policy Focus:** These outliers require targeted, hyper-localized economic inclusion programs, as general development aid is often diffused. |
| **Inflation Rate** | **Heavy Clustering (low) with Outliers** | The majority (low inflation) suggests global economic anchors (US, EU, Japan) maintain stability. The outliers represent high-risk, high-volatility markets—potentially driven by currency crises or political instability. **Risk Management:** Essential for any firm considering market entry in these unstable regions. |
| **Unemployment Rate** | **Clustering (5-10%)** | A healthy cluster suggests structural employment is managed in most developed and developing markets. The outliers over 20% indicate deeply rooted structural or youth unemployment problems, likely signaling a talent drain or mismatch. |

---

## The Global Convergence: Social Development Indicators

**The Takeaway:** Universal access to basic human development is an achievable global reality. This convergence creates a massive, *qualitatively similar* global consumer base.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (What it means for Product Strategy)** |
| --- | --- | --- |
| **Access to Electricity** | **Peak at 95-100%** | **Near-Universal Basic Infrastructure.** A strong signal for **digital product developers**—assume your user has power access. The few remaining gaps are geographically concentrated (e.g., last-mile rural areas) and require specific infrastructure or off-grid solutions. |
| **Literacy Rate** | **Peak at 90-100%** | **Converging Human Capital.** The global market is predominantly **literate**. Product design can leverage text, written instructions, and complex interfaces with high confidence. The low-end tail still requires localization and visual-first design principles. |
| **Life Expectancy** | **Strong Central Concentration (70-85)** | **A Maturing, Aging Global Market.** The world population is living longer. **Product Development:** Increased focus on healthcare, financial planning, and aging-in-place technologies for the expanding elderly demographic. |
| **Govt. Exp. on Education** | **Normal Distribution (4-5% of GDP)** | Most nations treat human capital development as a similar priority. The variance suggests varying returns on investment (ROI)—some may spend less but achieve high literacy, indicating efficiency. **Benchmarking:** This is a key metric for evaluating national commitment to long-term growth. |

## The Investor's Paradox: Trade and Capital Flows

**The Takeaway:** While global trade (Exports/Imports) is diversified, the inflow of long-term capital (FDI) is not. Investors overwhelmingly prefer stability and scale, reinforcing the existing wealth concentration.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (Investment Thesis)** |
| --- | --- | --- |
| **Foreign Direct Investment (FDI)** | **Heavy Right Skew** | **High-Confidence Investment Thesis.** FDI flows disproportionately to a few nations. **Investment Strategy:** Look for countries in the low FDI range but with *high* Literacy and *high* Access to Electricity—these are **Emerging Value Opportunities** where human capital is high, but the market is under-penetrated by international capital. |
| **Exports & Imports** | **Fairly Even Spread** | **Diversified Trade Activity.** Global supply chains are not overly dependent on a single set of markets. **Policy Focus:** This spread suggests trade policy needs to be regionally customized, as national trade reliance varies widely. |
| **Gross Capital Formation** | **Moderate Right Skew (15-30%)** | **Steady Global Reinvestment.** The clustering indicates a global commitment to business and infrastructure expansion, suggesting a sustainable growth outlook, distinct from volatile short-term speculation. |

---

## The Foundation of Prosperity: Agricultural Indicators

**The Takeaway:** Productivity, not just land, determines a nation's ability to feed itself and contribute to the global economy.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (Sustainability and Food Security)** |
| --- | --- | --- |
| **Agricultural Production Index** | **Clustering (100-120)** | **Incremental Global Efficiency.** Most nations are seeing moderate, stable productivity growth (above the base of 100). **AgriTech Opportunity:** The spread suggests a massive market for precision agriculture and mechanization in the lower-performing nations to boost yields and resilience. |
| **Agricultural Land Area** | **Uniform Distribution** | **Geographic Diversity.** The lack of a central cluster shows there's no "typical" land allocation, reflecting varied geography, population density, and economic structure. |    
--




    
<img width="1389" height="990" alt="output_32_0" src="https://github.com/user-attachments/assets/f095e384-c4c5-4901-8516-066914a7166b" />

This collection of histograms offers a powerful, data-driven narrative about the **Progressive but Unequal World**. It moves beyond simple metrics to reveal the deep structural differences between nations, providing a critical foundation for strategic policy and product decisions.

## Executive Summary: The Dual-Speed Global Economy

The global development landscape is one of stark contrasts. **Social welfare is converging**—most countries have achieved high marks in health, education, and basic infrastructure. However, **economic prosperity is heavily centralized and unequal**, with a few nations dominating wealth, investment, and productivity.

This "dual-speed" reality dictates unique challenges and opportunities: while product strategy can assume a globally literate and connected user base, investment strategy must contend with extreme concentrations of economic power.

---

## The Centralization of Wealth: Economic Health Indicators

Global economic power is overwhelmingly centralized. The world's wealth distribution is a testament to the "Matthew Effect"—to those who have, more will be given.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (What it means for Business/Policy)** |
| --- | --- | --- |
| **GDP & GNI** | **Extreme Right Skew** | A small fraction of nations (the long tail) accounts for the vast majority of global wealth. **Strategic Focus:** Targeting product development and scaling for these mega-economies yields maximum immediate return. |
| **Poverty Rate** | **High Right Skew** | While most enjoy low poverty, the long tail represents a critical challenge. **Policy Focus:** These outliers require targeted, hyper-localized economic inclusion programs, as general development aid is often diffused. |
| **Inflation Rate** | **Heavy Clustering (low) with Outliers** | The majority (low inflation) suggests global economic anchors (US, EU, Japan) maintain stability. The outliers represent high-risk, high-volatility markets—potentially driven by currency crises or political instability. **Risk Management:** Essential for any firm considering market entry in these unstable regions. |
| **Unemployment Rate** | **Clustering (5-10%)** | A healthy cluster suggests structural employment is managed in most developed and developing markets. The outliers over 20% indicate deeply rooted structural or youth unemployment problems, likely signaling a talent drain or mismatch. |

---

## The Global Convergence: Social Development IndicatorsUniversal access to basic human development is an achievable global reality. This convergence creates a massive, *qualitatively similar* global consumer base.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (What it means for Product Strategy)** |
| --- | --- | --- |
| **Access to Electricity** | **Peak at 95-100%** | **Near-Universal Basic Infrastructure.** A strong signal for **digital product developers**—assume your user has power access. The few remaining gaps are geographically concentrated (e.g., last-mile rural areas) and require specific infrastructure or off-grid solutions. |
| **Literacy Rate** | **Peak at 90-100%** | **Converging Human Capital.** The global market is predominantly **literate**. Product design can leverage text, written instructions, and complex interfaces with high confidence. The low-end tail still requires localization and visual-first design principles. |
| **Life Expectancy** | **Strong Central Concentration (70-85)** | **A Maturing, Aging Global Market.** The world population is living longer. **Product Development:** Increased focus on healthcare, financial planning, and aging-in-place technologies for the expanding elderly demographic. |
| **Govt. Exp. on Education** | **Normal Distribution (4-5% of GDP)** | Most nations treat human capital development as a similar priority. The variance suggests varying returns on investment (ROI)—some may spend less but achieve high literacy, indicating efficiency. **Benchmarking:** This is a key metric for evaluating national commitment to long-term growth. |

## The Investor's Paradox: Trade and Capital Flows

 While global trade (Exports/Imports) is diversified, the inflow of long-term capital (FDI) is not. Investors overwhelmingly prefer stability and scale, reinforcing the existing wealth concentration.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (Investment Thesis)** |
| --- | --- | --- |
| **Foreign Direct Investment (FDI)** | **Heavy Right Skew** | **High-Confidence Investment Thesis.** FDI flows disproportionately to a few nations. **Investment Strategy:** Look for countries in the low FDI range but with *high* Literacy and *high* Access to Electricity—these are **Emerging Value Opportunities** where human capital is high, but the market is under-penetrated by international capital. |
| **Exports & Imports** | **Fairly Even Spread** | **Diversified Trade Activity.** Global supply chains are not overly dependent on a single set of markets. **Policy Focus:** This spread suggests trade policy needs to be regionally customized, as national trade reliance varies widely. |
| **Gross Capital Formation** | **Moderate Right Skew (15-30%)** | **Steady Global Reinvestment.** The clustering indicates a global commitment to business and infrastructure expansion, suggesting a sustainable growth outlook, distinct from volatile short-term speculation. |

---

## The Foundation of Prosperity: Agricultural Indicators

 Productivity, not just land, determines a nation's ability to feed itself and contribute to the global economy.

| **Indicator** | **Distribution Shape** | **Data-Driven Story (Sustainability and Food Security)** |
| --- | --- | --- |
| **Agricultural Production Index** | **Clustering (100-120)** | **Incremental Global Efficiency.** Most nations are seeing moderate, stable productivity growth (above the base of 100). **AgriTech Opportunity:** The spread suggests a massive market for precision agriculture and mechanization in the lower-performing nations to boost yields and resilience. |
| **Agricultural Land Area** | **Uniform Distribution** | **Geographic Diversity.** The lack of a central cluster shows there's no "typical" land allocation, reflecting varied geography, population density, and economic structure. |

This collection of **Box Plots** provides a complementary view to the histograms, zeroing in on **median values, interquartile ranges (IQR), and the severity of global outliers**. As a data analyst, this visual helps quickly identify volatility and the "typical" country versus the exceptional ones.

## **The Severity of Economic Inequality: Economic Health Indicators**

The box plots vividly confirm that global wealth is concentrated, and economic instability (inflation, poverty) is an acute problem for a few, not the majority. The length of the "whisker" on the right side of the box plot for GDP and GNI is the most compelling evidence of extreme wealth concentration.

| Indicator | Box Plot Insight | Analyst's Story (Volatility & Central Tendency) |
| --- | --- | --- |
| **GDP_BN & GNI_BN** | **Box is tiny, Right Whisker/Outliers are vast.** | **Extreme Skew.** The median country has a negligible GDP/GNI compared to the maximum. The wealth gap is not just large; it's vast. **Product Strategy:** To capture the *value* ($$$), target the few outliers; to capture *volume* (users), understand the vast majority clustered near zero. |
| **Poverty Rate** | **Box is compressed near zero; many outliers.** | The **median** country enjoys a very low poverty rate (near 0%). High poverty is an issue of **acute national crisis** (the outliers), not a widespread global challenge. |
| **Inflation Rate** | **Box is tightly packed near zero; extreme outliers up to 50.** | The global economy is largely stable (low median/IQR). The countries with high inflation are **financial risk zones**; their volatility makes them highly challenging markets for long-term investment. |
| **Unemployment Rate** | **Relatively centered box (5-10%); few high outliers.** | The interquartile range (IQR) is narrow, suggesting most countries have structurally similar employment challenges. The high outliers represent distinct structural employment failures. |

---

## **Global Standardization: Social Development Indicators**

For social indicators, the boxes are generally wide and centered at high values, confirming global progress. The convergence on high medians provides a robust assumption base for global product design.

| Indicator | Box Plot Insight | Analyst's Story (Reliability for Product Design) |
| --- | --- | --- |
| **Life Expectancy** | **High Median (around 75), wide IQR (70-85).** | **Robust Health Baseline.** The "typical" country enjoys a relatively long lifespan. This indicates a high global baseline for public health and care infrastructure, simplifying assumptions for healthcare or retirement product markets. |
| **Literacy Rate** | **Box compressed very tightly near 100%.** | **Near-Universal Literacy.** The median and IQR are exceptionally high. A product analyst can safely assume a user base is literate when designing interfaces. |
| **Access to Electricity** | **Box compressed near 100%; small group of low outliers.** | **Infrastructure Success Story.** The vast majority of countries have near-complete access. Product focus should shift from **getting access** to **improving reliability** for the core market. |
| **Govt. Exp. on Education** | **Box centered around 4-5% of GDP, short whiskers.** | **Standardized Commitment.** There is a strong consensus on the budget allocated to education. This stability suggests predictable human capital development over time. |

---

## **Capital Flow and Trade Dynamics**

Trade activities (Exports/Imports) show broad global participation (wide IQR), but Foreign Direct Investment (FDI) remains highly selective, reinforcing the centralization of economic power.

| Indicator | Box Plot Insight | Analyst's Story (Investment & Trade Risk) |
| --- | --- | --- |
| **Foreign Direct Investment (FDI)** | **Box compressed near zero; extensive, vast outliers.** | **Investor Selectivity.** Most countries attract very little FDI (low median). The outliers—the massive FDI recipients—are the **preferred, low-risk markets**. The high skew suggests capital is not evenly distributed or seeking high-risk, high-reward opportunities. |
| **Exports & Imports** | **Wide boxes (e.g., 20-40% of GDP), moderate outliers.** | **Trade Activity is Broadly Distributed.** The large IQR indicates that a wide range of countries are active in global trade, suggesting robust and diversified supply chains. This makes the **global trade environment less vulnerable** to shock in any single region. |
| **Gross Capital Formation** | **Box centered well above zero (15-30% range).** | **Healthy Investment Base.** The robust box indicates a strong global commitment to reinvesting in future capacity (infrastructure, equipment). This is a good sign for long-term global growth potential. |

---

## **Agricultural Foundations**

Agricultural productivity is more stable than land area allocation, suggesting global efforts towards efficiency are paying off.

| Indicator | Box Plot Insight | Analyst's Story (Efficiency vs. Endowment) |
| --- | --- | --- |
| **Agricultural Land Area** | **Wide, almost uniform box (20-60%).** | **Geographic Variation.** Land allocation varies wildly, reflecting geographic constraints and policy choices. Land area alone is a poor predictor of output. |
| **Agricultural Production Index** | **Tight box clustered near 100-120.** | **Focus on Efficiency.** The tight cluster shows that the majority of countries are maintaining or slightly improving agricultural productivity. The outliers with very high indices are likely nations with advanced, heavily mechanized agricultural sectors. |

```

<img width="932" height="724" alt="image" src="https://github.com/user-attachments/assets/fe1d68d8-88a4-410e-b7de-284f5a5f3ed4" />


- 

This bar chart on **Outlier Percentage** quantifies the degree of **global heterogeneity** for each socioeconomic indicator. It's a crucial tool for an analyst to determine which global average metrics are reliable and which are misleading due to extreme national deviations.

The indicators are divided into two clear strategic groups: those with **High Disparity** (requiring highly segmented, localized strategies) and those with **Global Convergence** (allowing for standardized strategies).

---

## **Group 1: High Disparity Indicators (The Risk Zones)**

These metrics have a significant percentage of countries that are statistical outliers (deviating sharply from the global median). They represent the biggest challenges, risks, and unique underserved opportunities.

| Indicator | Outlier % | Analyst's Interpretation and Strategic Action |
| --- | --- | --- |
| **Access to electricity** | **~17.5% (Highest)** | **The Infrastructure Gap.** The highest non-conforming rate globally. This confirms that nearly **1 in 6 countries** has a critically underdeveloped power grid. **Action:** A product or service relying on stable electricity must specifically account for this 17.5% with low-power or offline solutions. |
| **Foreign direct investment (FDI)** | **~14.5%** | **Capital Selectivity.** This high percentage primarily represents the many nations receiving **extremely low FDI**. Global capital is highly selective. **Action:** Investment strategies must segment the market into the few capital magnets and the many capital-starved nations. |
| **Poverty rate** | **~11.5%** | **Acute Social Crisis.** A significant portion of nations faces a poverty problem far exceeding the global norm. **Action:** Development aid and social policies must be targeted and deep, as general economic growth models may bypass this group. |
| **GNI_BN & GDP_BN** | **~10.5% each** | **Economic Segmentation.** Around **1 in 10 countries** is an economic outlier. Given that these are the mega-economies, this means the global average wealth is meaningless. **Action:** Businesses must use a **two-tiered pricing/product model**—one for the wealthy 10% and another for the mass market. |
| **Inflation rate** | **~9%** | **Financial Volatility.** Nearly 1 in 11 countries has non-conforming inflation. **Action:** Indicates markets with high financial risk, necessitating robust mechanisms for **currency hedging and flexible, adaptive pricing**. |

---

## **Group 2: Global Convergence Indicators (The Baseline)**

These metrics have low or zero outlier percentages, signaling that the majority of countries conform to the global standard. These are the **safest assumptions** for a universal product or policy design.

| Indicator | Outlier % | Analyst's Interpretation and Strategic Action |
| --- | --- | --- |
| **Agricultural production index** | **~5.5%** | **Managed Efficiency.** Most nations maintain a production index close to the baseline. Low risk of extreme, chaotic variation in food output. |
| **Gross capital formation & Gov't expenditure on education & Literacy rate** | **~4.5% each** | **Standardized Investment.** The world shows a strong, consistent consensus on investing in **infrastructure, education, and human capital**. This predictability allows for long-term planning regarding workforce quality and capacity expansion. |
| **Life expectancy, Mobile phone subscriptions, Exports/Imports, Agricultural land area** | **~0%** | **Universal Baselines.** These zero-outlier metrics are the foundation for a **Global Standard Strategy**. Every country falls within the normal range for these factors. **Action:** Assume near-universal mobile connectivity and basic health for all global product users. |

--

