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


        
<img width="932" height="724" alt="output_36_0" src="https://github.com/user-attachments/assets/49d12ec6-16a8-4ec1-af18-e1c9cfb6937c" />

This bar chart on **Outlier Percentage** is a crucial diagnostic tool for a data or product analyst, as it quantifies the degree of **global heterogeneity** for each indicator. High outlier percentages signal metrics where a significant portion of countries deviates from the global norm (the median and interquartile range), while low percentages indicate global convergence.

## **Strategic Insights from Outlier Concentration**

The chart clearly separates the indicators into two distinct groups: those with significant global disparity (high outliers) and those showing near-universal alignment (low/zero outliers).

---

### **High Disparity Indicators (High Outlier Percentage)**

These metrics represent the biggest challenges and the most unique opportunities, as the global "norm" is a poor descriptor for a large fraction of the countries. They require **hyper-localized strategies** and **robust risk management**.

| Indicator | Outlier % | Analyst's Interpretation & Action |
| --- | --- | --- |
| **Access to Electricity** | **~17.5% (Highest)** | **Infrastructure Gap.** This is the most non-conforming metric. The 17.5% outlier group represents nations with critically low access. **Action:** Product strategies related to digital content or energy consumption must target this specific group with offline/low-power solutions. |
| **Foreign Direct Investment (FDI)** | **~14.5%** | **Capital Concentration.** The high outlier percentage doesn't mean many countries attract high FDI; rather, it highlights the many countries that receive **extremely low FDI** (below the lower fence of the box plot). **Action:** Investment policy must be tailored to address the lack of capital flow in these non-conforming markets. |
| **Poverty Rate** | **~11.5%** | **Social Inequality.** This confirms the previous box plot analysis—a substantial portion of nations faces significantly higher poverty rates than the global median. **Action:** Development aid and social programs should heavily prioritize this outlier group. |
| **GNI_BN & GDP_BN** | **~10.5% each** | **Economic Segmentation.** A full 1 in 10 countries are economic outliers. These outliers define the global economy. **Action:** Target market analysis *must* segment the market into the "economic giants" and the "rest," as a global average is meaningless. |
| **Inflation Rate** | **~9%** | **Financial Instability.** Nearly 1 in 11 countries has non-conforming inflation. **Action:** Businesses operating in these markets must have mechanisms for currency hedging and flexible pricing models. |

---

### **Low Disparity Indicators (Low to Zero Outlier Percentage)**

These metrics show **global convergence and standardization**. For these, a **one-size-fits-most global product strategy** is often viable, as the vast majority of countries conform to the central tendencies (median and IQR).

| Indicator | Outlier % | Analyst's Interpretation & Action |
| --- | --- | --- |
| **Literacy Rate** | **~4.5%** | **Education Success.** A very small number of nations lag significantly. Global content and interfaces can confidently assume high literacy for the vast majority of users. |
| **Life Expectancy** | **~0%** | **Health Convergence.** Every country's life expectancy falls within the defined normal range, signaling that health outcomes have achieved a fundamental global baseline. **Action:** This indicates low risk when planning health or life-cycle focused products globally. |
| **Mobile phone subscriptions** | **~0%** | **Connectivity Saturation.** No country is an outlier in mobile penetration. This confirms mobile access is near-universal, reinforcing the primacy of a **mobile-first product strategy**. |
| **Exports & Imports** | **~0% each** | **Trade Balance.** Trade activity is relatively consistent across the globe. Extreme reliance or lack of reliance on trade is not a widespread issue. |
| **Agricultural Land Area** | **~0%** | **Uniform Diversity.** Despite wide variance in the box plot, no country's land allocation is statistically extreme, suggesting geographical constraints are balanced across the distribution. |

---

## **Strategic Takeaways for Product & Policy**

1. **Focus on the "Top 5" for Investment Risk:** The highest outlier percentages are in **Access to Electricity, FDI, Poverty, GNI, and Inflation**. These are the metrics that will most often cause a global model to fail at a national level. Strategic resources should be allocated to understanding the **specific characteristics** of the non-conforming countries for these five indicators.
2. **Leverage Global Consensus:** The zero-outlier metrics (**Life Expectancy, Mobile Subscriptions, Trade** → **0%**) represent the safest assumptions for global product design and policy planning. Any strategy relying on connectivity or basic social health can be executed with high confidence.
3. **From Outlier to Opportunity:** For **Access to Electricity**, the 17.5% outlier group is a massive, underserved market. This outlier percentage signals the magnitude of the opportunity for utility providers, off-grid energy solutions, and related hardware manufacturers.

---

        
<img width="900" height="920" alt="output_40_0" src="https://github.com/user-attachments/assets/91b50172-e982-43cb-a1cf-6aad69515f33" />



```python
## Jointplot

sns.jointplot(x='GDP_BN', y='GNI_BN', data=df_final, height=4, color='olive')
plt.show()
```


        
<img width="412" height="390" alt="output_41_0" src="https://github.com/user-attachments/assets/98e3ed81-65eb-40f4-a362-f2ce646c965f" />



```python
sns.jointplot(x='Gross capital formation', y='Poverty rate', data=df_final, height=4, color='crimson')
plt.show()
```


        
<img width="385" height="390" alt="output_42_0" src="https://github.com/user-attachments/assets/11ef39ac-fc8e-4a51-9e8a-0b3a727ab992" />

This correlation matrix provides critical insights into the **interdependencies of global development factors**. For a data or product analyst, this reveals which indicators move together, suggesting underlying causal links, shared policies, or systemic relationships. The scale runs from **+1.0 (perfect positive correlation)** to **−1.0 (perfect negative correlation)**.

## **Key Strategic Relationships**

The most important insights come from strong correlations (close to ±1.0), as they suggest that improving one factor is likely tied to improving or worsening another.

---

### **Economic Health & Development**

These relationships highlight the fundamental drivers and consequences of economic prosperity:

- **Wealth & Quality of Life (GDP/GNI):**
    - **Strong Positive Links (+0.8):** Both **GDP_BN** and **GNI_BN** are strongly correlated with **Foreign Direct Investment (FDI)** (+0.8). This confirms that the wealthiest nations are the primary magnets for global capital.
    - **Strong Negative Links (−0.8 to −0.9):** GDP/GNI show very strong negative correlations with **Poverty Rate** (around −0.8) and **Unemployment Rate** (around −0.9). **Analyst Story:** Economic growth is the most powerful tool for reducing poverty and increasing employment.
- **Trade & Investment:**
    - **Exports** and **Imports** are **perfectly correlated** (+1.0). This is expected, as global trade relies on a balanced flow of goods and services; countries that export more also typically import more to sustain their economies.

---

### **Social Progress & Economic Stability**

Social indicators have powerful connections to economic stability, particularly concerning stability and human capital:

- **Poverty & Instability:**
    - **Poverty Rate** has a strong negative correlation with **Life Expectancy** (−0.7) and **Literacy Rate** (−0.7). **Analyst Story:** Poverty creates a vicious cycle where lack of resources directly shortens lives and limits educational access, locking people out of economic opportunity.
- **Literacy & Development:**
    - **Literacy Rate** is strongly correlated with **Access to Electricity** (+0.7). This suggests that the development of human capital (education) and basic infrastructure (energy) often happen in parallel, reflecting comprehensive national development strategies.

---

### **Surprising or Counter-Intuitive Relationships**

These suggest less obvious dynamics that warrant deeper investigation:

- **Unemployment vs. Poverty (−0.5):** While negatively correlated (as expected), the relationship is only moderate. **Analyst Story:** This suggests that low unemployment doesn't automatically mean low poverty. A significant portion of the population may still be working but remains poor (working poor), indicating problems with low wages or lack of social safety nets.
- **FDI vs. Exports/Imports (−0.2):** Foreign Direct Investment (FDI) has a surprisingly weak, slightly negative correlation with exports and imports. **Analyst Story:** This suggests FDI is primarily aimed at **domestic market penetration** or **resource extraction** within the host country, not necessarily for boosting overall trade volume. Investors may be setting up shop to sell *within* the country, rather than using it as an export hub.
- **Agricultural Production Index vs. GDP (−0.2):** A weak negative correlation exists. **Analyst Story:** This is common in developed economies. As a country's GDP rises, its economy typically shifts away from primary agriculture toward manufacturing and services. High GDP/GNI countries, while wealthy, are not necessarily the world's most productive farmers relative to their economic size.


```


    
<img width="385" height="390" alt="output_43_0" src="https://github.com/user-attachments/assets/ddfad655-46f1-420c-9d80-0f44e3e058bc" />




```python
def top_3(data, parameter):
    # Extract unique years from the 'year' column and sort them
    year_list = data['year'].dt.year.sort_values().unique()
    
    # Create an empty DataFrame to store the top 3 values for each year
    result_df = pd.DataFrame(columns=year_list, index=[1, 2, 3])
    
    # Iterate through each year in the sorted year_list
    for year in year_list:
        # Filter the data for the current year
        df_year = data[data['year'].dt.year == year]
        
        # Group by 'country', sum the values of the specified parameter, 
        # sort in descending order, and take the top 3 countries
        value = df_year.groupby('country')[parameter].sum().sort_values(ascending=False).head(3).index
        
        # Assign the top 3 countries to the corresponding column in the result_df
        result_df[year] = value
    
    # Return the result DataFrame
    return result_df
```


```python
from IPython.display import display
```


```python
for i in selected_cols:
    result = top_3(df_final,i)
    print(i)
    display(result)
    print('-------------------------------------------------')
```

    Inflation rate
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Russian Federation</td>
      <td>Brazil</td>
      <td>Turkiye</td>
      <td>Argentina</td>
      <td>Argentina</td>
      <td>Argentina</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Brazil</td>
      <td>Turkiye</td>
      <td>Mexico</td>
      <td>Turkiye</td>
      <td>Turkiye</td>
      <td>Turkiye</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Turkiye</td>
      <td>Russian Federation</td>
      <td>South Africa</td>
      <td>Mexico</td>
      <td>Russian Federation</td>
      <td>India</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Unemployment rate
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Italy</td>
      <td>Italy</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Turkiye</td>
      <td>Brazil</td>
    </tr>
    <tr>
      <th>3</th>
      <td>France</td>
      <td>Brazil</td>
      <td>Italy</td>
      <td>Turkiye</td>
      <td>Brazil</td>
      <td>Turkiye</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Poverty rate
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Mexico</td>
    </tr>
    <tr>
      <th>3</th>
      <td>China</td>
      <td>Mexico</td>
      <td>China</td>
      <td>Mexico</td>
      <td>Argentina</td>
      <td>Brazil</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Life expectancy
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Italy</td>
      <td>Italy</td>
      <td>Italy</td>
      <td>Italy</td>
      <td>Italy</td>
      <td>Korea, Rep.</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Australia</td>
      <td>France</td>
      <td>Korea, Rep.</td>
      <td>Australia</td>
      <td>Korea, Rep.</td>
      <td>Australia</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Literacy rate
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Turkiye</td>
      <td>Turkiye</td>
      <td>Turkiye</td>
      <td>Indonesia</td>
      <td>Italy</td>
      <td>Argentina</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Saudi Arabia</td>
      <td>Mexico</td>
      <td>Turkiye</td>
      <td>Saudi Arabia</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Brazil</td>
      <td>Mexico</td>
      <td>China</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Access to electricity
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Australia</td>
      <td>Australia</td>
      <td>Argentina</td>
      <td>Argentina</td>
      <td>Argentina</td>
      <td>Argentina</td>
    </tr>
    <tr>
      <th>2</th>
      <td>China</td>
      <td>China</td>
      <td>Australia</td>
      <td>Australia</td>
      <td>Australia</td>
      <td>Australia</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Canada</td>
      <td>Canada</td>
      <td>Canada</td>
      <td>Canada</td>
      <td>Canada</td>
      <td>Canada</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Mobile phone subscriptions
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Saudi Arabia</td>
      <td>Russian Federation</td>
      <td>Indonesia</td>
      <td>South Africa</td>
      <td>Russian Federation</td>
      <td>Russian Federation</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Russian Federation</td>
      <td>Saudi Arabia</td>
      <td>Russian Federation</td>
      <td>Russian Federation</td>
      <td>South Africa</td>
      <td>South Africa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>South Africa</td>
      <td>Indonesia</td>
      <td>South Africa</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Government expenditure on education
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>Brazil</td>
      <td>South Africa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Argentina</td>
      <td>Argentina</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>Brazil</td>
    </tr>
    <tr>
      <th>3</th>
      <td>United Kingdom</td>
      <td>South Africa</td>
      <td>France</td>
      <td>France</td>
      <td>France</td>
      <td>France</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Foreign direct investment (FDI)
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>China</td>
      <td>United States</td>
      <td>China</td>
    </tr>
    <tr>
      <th>2</th>
      <td>China</td>
      <td>United Kingdom</td>
      <td>China</td>
      <td>United States</td>
      <td>China</td>
      <td>Germany</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Brazil</td>
      <td>China</td>
      <td>United Kingdom</td>
      <td>Germany</td>
      <td>Germany</td>
      <td>United Kingdom</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Exports of goods and services
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Korea, Rep.</td>
      <td>Germany</td>
      <td>Germany</td>
      <td>Germany</td>
      <td>Germany</td>
      <td>Mexico</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Germany</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Germany</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Korea, Rep.</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Imports of goods and services
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
      <td>Mexico</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Korea, Rep.</td>
      <td>Germany</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Germany</td>
      <td>Germany</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Saudi Arabia</td>
      <td>Canada</td>
      <td>Germany</td>
      <td>Germany</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Gross capital formation
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
      <td>Indonesia</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Turkiye</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
      <td>Korea, Rep.</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Agricultural land area
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
    </tr>
    <tr>
      <th>2</th>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
      <td>South Africa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>United Kingdom</td>
      <td>United Kingdom</td>
      <td>United Kingdom</td>
      <td>United Kingdom</td>
      <td>United Kingdom</td>
      <td>United Kingdom</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    Agricultural production index
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
      <td>Saudi Arabia</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Argentina</td>
      <td>Canada</td>
      <td>Australia</td>
      <td>Mexico</td>
      <td>Argentina</td>
      <td>South Africa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>France</td>
      <td>United States</td>
      <td>South Africa</td>
      <td>Indonesia</td>
      <td>Mexico</td>
      <td>Brazil</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    GDP_BN
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
    </tr>
    <tr>
      <th>2</th>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    GNI_BN
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
      <td>United States</td>
    </tr>
    <tr>
      <th>2</th>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
      <td>China</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
      <td>Japan</td>
    </tr>
  </tbody>
</table>
</div>


    -------------------------------------------------
    


```python
# Extracting the year from the date time column.

df_final['year_o'] = df_final['year'].dt.year
```


```python
df_final.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>year</th>
      <th>GDP</th>
      <th>GNI</th>
      <th>Inflation rate</th>
      <th>Unemployment rate</th>
      <th>Poverty rate</th>
      <th>Life expectancy</th>
      <th>Literacy rate</th>
      <th>Access to electricity</th>
      <th>...</th>
      <th>Government expenditure on education</th>
      <th>Foreign direct investment (FDI)</th>
      <th>Exports of goods and services</th>
      <th>Imports of goods and services</th>
      <th>Gross capital formation</th>
      <th>Agricultural land area</th>
      <th>Agricultural production index</th>
      <th>GDP_BN</th>
      <th>GNI_BN</th>
      <th>year_o</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Argentina</td>
      <td>2015-01-01</td>
      <td>594749285413.21</td>
      <td>583615452086.54</td>
      <td>NaN</td>
      <td>7.58</td>
      <td>NaN</td>
      <td>76.60</td>
      <td>NaN</td>
      <td>99.70</td>
      <td>...</td>
      <td>5.78</td>
      <td>11758994011.29</td>
      <td>10.71</td>
      <td>11.78</td>
      <td>15.56</td>
      <td>44.12</td>
      <td>104.14</td>
      <td>594.75</td>
      <td>583.62</td>
      <td>2015</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Argentina</td>
      <td>2016-01-01</td>
      <td>557532320662.95</td>
      <td>545251641127.71</td>
      <td>NaN</td>
      <td>8.09</td>
      <td>1.30</td>
      <td>76.11</td>
      <td>NaN</td>
      <td>99.90</td>
      <td>...</td>
      <td>5.55</td>
      <td>3260164341.77</td>
      <td>12.53</td>
      <td>13.57</td>
      <td>14.27</td>
      <td>43.43</td>
      <td>101.71</td>
      <td>557.53</td>
      <td>545.25</td>
      <td>2016</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Argentina</td>
      <td>2017-01-01</td>
      <td>643628393281.36</td>
      <td>627200463933.82</td>
      <td>NaN</td>
      <td>8.35</td>
      <td>1.10</td>
      <td>76.54</td>
      <td>NaN</td>
      <td>100.00</td>
      <td>...</td>
      <td>5.45</td>
      <td>11516861462.28</td>
      <td>11.32</td>
      <td>13.97</td>
      <td>15.16</td>
      <td>42.98</td>
      <td>106.82</td>
      <td>643.63</td>
      <td>627.20</td>
      <td>2017</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Argentina</td>
      <td>2018-01-01</td>
      <td>524819892360.18</td>
      <td>506094045059.70</td>
      <td>34.28</td>
      <td>9.22</td>
      <td>1.60</td>
      <td>76.77</td>
      <td>NaN</td>
      <td>100.00</td>
      <td>...</td>
      <td>4.88</td>
      <td>11716769818.75</td>
      <td>14.44</td>
      <td>16.33</td>
      <td>15.25</td>
      <td>42.36</td>
      <td>92.20</td>
      <td>524.82</td>
      <td>506.09</td>
      <td>2018</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Argentina</td>
      <td>2019-01-01</td>
      <td>447754683615.22</td>
      <td>430166792070.57</td>
      <td>53.55</td>
      <td>9.84</td>
      <td>1.70</td>
      <td>76.85</td>
      <td>NaN</td>
      <td>100.00</td>
      <td>...</td>
      <td>4.77</td>
      <td>6649187837.99</td>
      <td>17.92</td>
      <td>14.71</td>
      <td>14.20</td>
      <td>42.61</td>
      <td>113.14</td>
      <td>447.75</td>
      <td>430.17</td>
      <td>2019</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 21 columns</p>
</div>



Life Expectancy Analysis:



```python
life_expectancy = pd.pivot_table(columns='year_o', index='country', values='Life expectancy', data=df_final, aggfunc='mean').round(1)

```


```python
life_expectancy.columns
```




    Index([2015, 2016, 2017, 2018, 2019, 2020], dtype='int32', name='year_o')




```python
life_expectancy
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>year_o</th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
    </tr>
    <tr>
      <th>country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Argentina</th>
      <td>76.60</td>
      <td>76.10</td>
      <td>76.50</td>
      <td>76.80</td>
      <td>76.80</td>
      <td>75.90</td>
    </tr>
    <tr>
      <th>Australia</th>
      <td>82.40</td>
      <td>82.40</td>
      <td>82.50</td>
      <td>82.70</td>
      <td>82.90</td>
      <td>83.20</td>
    </tr>
    <tr>
      <th>Brazil</th>
      <td>75.10</td>
      <td>75.10</td>
      <td>75.40</td>
      <td>75.60</td>
      <td>75.80</td>
      <td>74.50</td>
    </tr>
    <tr>
      <th>Canada</th>
      <td>81.80</td>
      <td>81.90</td>
      <td>81.80</td>
      <td>81.80</td>
      <td>82.20</td>
      <td>81.50</td>
    </tr>
    <tr>
      <th>China</th>
      <td>77.00</td>
      <td>77.20</td>
      <td>77.20</td>
      <td>77.70</td>
      <td>77.90</td>
      <td>78.00</td>
    </tr>
    <tr>
      <th>France</th>
      <td>82.30</td>
      <td>82.60</td>
      <td>82.60</td>
      <td>82.70</td>
      <td>82.80</td>
      <td>82.20</td>
    </tr>
    <tr>
      <th>Germany</th>
      <td>80.60</td>
      <td>81.00</td>
      <td>81.00</td>
      <td>80.90</td>
      <td>81.30</td>
      <td>81.00</td>
    </tr>
    <tr>
      <th>India</th>
      <td>69.30</td>
      <td>69.70</td>
      <td>70.10</td>
      <td>70.40</td>
      <td>70.70</td>
      <td>70.20</td>
    </tr>
    <tr>
      <th>Indonesia</th>
      <td>69.50</td>
      <td>69.70</td>
      <td>70.00</td>
      <td>70.10</td>
      <td>70.30</td>
      <td>68.80</td>
    </tr>
    <tr>
      <th>Italy</th>
      <td>82.50</td>
      <td>83.20</td>
      <td>82.90</td>
      <td>83.30</td>
      <td>83.50</td>
      <td>82.20</td>
    </tr>
    <tr>
      <th>Japan</th>
      <td>83.80</td>
      <td>84.00</td>
      <td>84.10</td>
      <td>84.20</td>
      <td>84.40</td>
      <td>84.60</td>
    </tr>
    <tr>
      <th>Korea, Rep.</th>
      <td>82.00</td>
      <td>82.30</td>
      <td>82.60</td>
      <td>82.60</td>
      <td>83.20</td>
      <td>83.40</td>
    </tr>
    <tr>
      <th>Mexico</th>
      <td>74.40</td>
      <td>74.40</td>
      <td>74.30</td>
      <td>74.30</td>
      <td>74.50</td>
      <td>70.40</td>
    </tr>
    <tr>
      <th>Russian Federation</th>
      <td>71.20</td>
      <td>71.70</td>
      <td>72.50</td>
      <td>72.70</td>
      <td>73.10</td>
      <td>71.30</td>
    </tr>
    <tr>
      <th>Saudi Arabia</th>
      <td>77.80</td>
      <td>78.40</td>
      <td>78.70</td>
      <td>78.80</td>
      <td>78.30</td>
      <td>77.60</td>
    </tr>
    <tr>
      <th>South Africa</th>
      <td>64.10</td>
      <td>64.70</td>
      <td>65.40</td>
      <td>65.70</td>
      <td>66.10</td>
      <td>65.20</td>
    </tr>
    <tr>
      <th>Turkiye</th>
      <td>76.50</td>
      <td>76.60</td>
      <td>77.00</td>
      <td>77.50</td>
      <td>77.70</td>
      <td>76.50</td>
    </tr>
    <tr>
      <th>United Kingdom</th>
      <td>81.00</td>
      <td>81.20</td>
      <td>81.30</td>
      <td>81.30</td>
      <td>81.40</td>
      <td>80.30</td>
    </tr>
    <tr>
      <th>United States</th>
      <td>78.70</td>
      <td>78.50</td>
      <td>78.50</td>
      <td>78.60</td>
      <td>78.80</td>
      <td>77.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Calculting the percentage change from 2015 to 2020. 

life_expectancy['perc_chg'] = round((life_expectancy[2020] - life_expectancy[2015])*100/life_expectancy[2015],1)
```


```python
# Sorting the values in ascending order:

life_expectancy = life_expectancy.sort_values(ascending=False, by='perc_chg')
```


```python
life_expectancy
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>year_o</th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
      <th>perc_chg</th>
    </tr>
    <tr>
      <th>country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>South Africa</th>
      <td>64.10</td>
      <td>64.70</td>
      <td>65.40</td>
      <td>65.70</td>
      <td>66.10</td>
      <td>65.20</td>
      <td>1.70</td>
    </tr>
    <tr>
      <th>Korea, Rep.</th>
      <td>82.00</td>
      <td>82.30</td>
      <td>82.60</td>
      <td>82.60</td>
      <td>83.20</td>
      <td>83.40</td>
      <td>1.70</td>
    </tr>
    <tr>
      <th>China</th>
      <td>77.00</td>
      <td>77.20</td>
      <td>77.20</td>
      <td>77.70</td>
      <td>77.90</td>
      <td>78.00</td>
      <td>1.30</td>
    </tr>
    <tr>
      <th>India</th>
      <td>69.30</td>
      <td>69.70</td>
      <td>70.10</td>
      <td>70.40</td>
      <td>70.70</td>
      <td>70.20</td>
      <td>1.30</td>
    </tr>
    <tr>
      <th>Japan</th>
      <td>83.80</td>
      <td>84.00</td>
      <td>84.10</td>
      <td>84.20</td>
      <td>84.40</td>
      <td>84.60</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>Australia</th>
      <td>82.40</td>
      <td>82.40</td>
      <td>82.50</td>
      <td>82.70</td>
      <td>82.90</td>
      <td>83.20</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>Germany</th>
      <td>80.60</td>
      <td>81.00</td>
      <td>81.00</td>
      <td>80.90</td>
      <td>81.30</td>
      <td>81.00</td>
      <td>0.50</td>
    </tr>
    <tr>
      <th>Russian Federation</th>
      <td>71.20</td>
      <td>71.70</td>
      <td>72.50</td>
      <td>72.70</td>
      <td>73.10</td>
      <td>71.30</td>
      <td>0.10</td>
    </tr>
    <tr>
      <th>Turkiye</th>
      <td>76.50</td>
      <td>76.60</td>
      <td>77.00</td>
      <td>77.50</td>
      <td>77.70</td>
      <td>76.50</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>France</th>
      <td>82.30</td>
      <td>82.60</td>
      <td>82.60</td>
      <td>82.70</td>
      <td>82.80</td>
      <td>82.20</td>
      <td>-0.10</td>
    </tr>
    <tr>
      <th>Saudi Arabia</th>
      <td>77.80</td>
      <td>78.40</td>
      <td>78.70</td>
      <td>78.80</td>
      <td>78.30</td>
      <td>77.60</td>
      <td>-0.30</td>
    </tr>
    <tr>
      <th>Canada</th>
      <td>81.80</td>
      <td>81.90</td>
      <td>81.80</td>
      <td>81.80</td>
      <td>82.20</td>
      <td>81.50</td>
      <td>-0.40</td>
    </tr>
    <tr>
      <th>Italy</th>
      <td>82.50</td>
      <td>83.20</td>
      <td>82.90</td>
      <td>83.30</td>
      <td>83.50</td>
      <td>82.20</td>
      <td>-0.40</td>
    </tr>
    <tr>
      <th>Brazil</th>
      <td>75.10</td>
      <td>75.10</td>
      <td>75.40</td>
      <td>75.60</td>
      <td>75.80</td>
      <td>74.50</td>
      <td>-0.80</td>
    </tr>
    <tr>
      <th>Argentina</th>
      <td>76.60</td>
      <td>76.10</td>
      <td>76.50</td>
      <td>76.80</td>
      <td>76.80</td>
      <td>75.90</td>
      <td>-0.90</td>
    </tr>
    <tr>
      <th>United Kingdom</th>
      <td>81.00</td>
      <td>81.20</td>
      <td>81.30</td>
      <td>81.30</td>
      <td>81.40</td>
      <td>80.30</td>
      <td>-0.90</td>
    </tr>
    <tr>
      <th>Indonesia</th>
      <td>69.50</td>
      <td>69.70</td>
      <td>70.00</td>
      <td>70.10</td>
      <td>70.30</td>
      <td>68.80</td>
      <td>-1.00</td>
    </tr>
    <tr>
      <th>United States</th>
      <td>78.70</td>
      <td>78.50</td>
      <td>78.50</td>
      <td>78.60</td>
      <td>78.80</td>
      <td>77.00</td>
      <td>-2.20</td>
    </tr>
    <tr>
      <th>Mexico</th>
      <td>74.40</td>
      <td>74.40</td>
      <td>74.30</td>
      <td>74.30</td>
      <td>74.50</td>
      <td>70.40</td>
      <td>-5.40</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Visualizing the plot of percentage change:

plt.figure(figsize=(11,5))
sns.barplot(x=life_expectancy.index, y=life_expectancy['perc_chg'], palette='viridis')
plt.title("% Change in Life Expectancy from 2015 to 2020")
plt.xticks(rotation =90)
plt.show()
```


       
<img width="922" height="586" alt="output_56_0" src="https://github.com/user-attachments/assets/3c9212e1-e554-48b3-9db2-dadff1e7fb35" />


Analyzing the Foreign Direct Investments:


```python
# Create a pivot table for Foreign Direct Investment (FDI) using 'year_o' as columns, 'country' as index, and 'FDI' as values
fdi = pd.pivot_table(columns='year_o', index='country', values='Foreign direct investment (FDI)', data=df_final, aggfunc='mean').round(1)

# Calculate the percentage change in FDI between the years 2015 and 2020 for each country
fdi['perc_chg'] = round((fdi[2020] - fdi[2015]) * 100 / fdi[2015], 1)

# Sort the pivot table by the percentage change in descending order
fdi = fdi.sort_values(ascending=False, by='perc_chg')
```


```python
fdi
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>year_o</th>
      <th>2015</th>
      <th>2016</th>
      <th>2017</th>
      <th>2018</th>
      <th>2019</th>
      <th>2020</th>
      <th>perc_chg</th>
    </tr>
    <tr>
      <th>country</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Japan</th>
      <td>5252218412.40</td>
      <td>40954181468.60</td>
      <td>18802251208.10</td>
      <td>25289367857.90</td>
      <td>39960544340.00</td>
      <td>62584719398.10</td>
      <td>1091.60</td>
    </tr>
    <tr>
      <th>United Kingdom</th>
      <td>45333483122.10</td>
      <td>324813224213.00</td>
      <td>125358809934.10</td>
      <td>-25055440306.90</td>
      <td>19790761929.10</td>
      <td>157185559300.00</td>
      <td>246.70</td>
    </tr>
    <tr>
      <th>Germany</th>
      <td>62418993509.20</td>
      <td>58132711370.80</td>
      <td>108786501529.10</td>
      <td>162250938125.80</td>
      <td>75463438450.90</td>
      <td>176781024357.20</td>
      <td>183.20</td>
    </tr>
    <tr>
      <th>Korea, Rep.</th>
      <td>4104100000.00</td>
      <td>12104300000.00</td>
      <td>17912900000.00</td>
      <td>12182600000.00</td>
      <td>9634300000.00</td>
      <td>8764900000.00</td>
      <td>113.60</td>
    </tr>
    <tr>
      <th>South Africa</th>
      <td>1521139945.30</td>
      <td>2215307020.40</td>
      <td>2058579911.10</td>
      <td>5569462350.20</td>
      <td>5116098443.50</td>
      <td>3153552569.40</td>
      <td>107.30</td>
    </tr>
    <tr>
      <th>India</th>
      <td>44009492129.50</td>
      <td>44458571545.80</td>
      <td>39966091358.70</td>
      <td>42117450737.30</td>
      <td>50610647353.60</td>
      <td>64362364994.40</td>
      <td>46.20</td>
    </tr>
    <tr>
      <th>Russian Federation</th>
      <td>6852970000.00</td>
      <td>32538900000.00</td>
      <td>28557440000.00</td>
      <td>8784850000.00</td>
      <td>31974770000.00</td>
      <td>9478810000.00</td>
      <td>38.30</td>
    </tr>
    <tr>
      <th>China</th>
      <td>242489331627.40</td>
      <td>174749584584.00</td>
      <td>166083755721.60</td>
      <td>235365050036.30</td>
      <td>187169822364.80</td>
      <td>253095616058.60</td>
      <td>4.40</td>
    </tr>
    <tr>
      <th>Indonesia</th>
      <td>19779127977.00</td>
      <td>4541713739.20</td>
      <td>20510310832.40</td>
      <td>18909826043.50</td>
      <td>24993551748.00</td>
      <td>19175077747.80</td>
      <td>-3.10</td>
    </tr>
    <tr>
      <th>Mexico</th>
      <td>36251149438.00</td>
      <td>38899523620.00</td>
      <td>33132345030.00</td>
      <td>37859235431.00</td>
      <td>29947415429.00</td>
      <td>31541065129.00</td>
      <td>-13.00</td>
    </tr>
    <tr>
      <th>Brazil</th>
      <td>64738153494.40</td>
      <td>74294627801.20</td>
      <td>68885491315.20</td>
      <td>78183840045.00</td>
      <td>69174411753.40</td>
      <td>38270116307.40</td>
      <td>-40.90</td>
    </tr>
    <tr>
      <th>Canada</th>
      <td>59986208237.10</td>
      <td>34201872160.60</td>
      <td>25357801000.50</td>
      <td>42603762048.60</td>
      <td>48942300762.20</td>
      <td>29123011879.30</td>
      <td>-51.50</td>
    </tr>
    <tr>
      <th>France</th>
      <td>43133325471.40</td>
      <td>35623357280.10</td>
      <td>43733253503.90</td>
      <td>77493098693.20</td>
      <td>53499337503.70</td>
      <td>19368829836.50</td>
      <td>-55.10</td>
    </tr>
    <tr>
      <th>Argentina</th>
      <td>11758994011.30</td>
      <td>3260164341.80</td>
      <td>11516861462.30</td>
      <td>11716769818.80</td>
      <td>6649187838.00</td>
      <td>4884127676.00</td>
      <td>-58.50</td>
    </tr>
    <tr>
      <th>Saudi Arabia</th>
      <td>3970644084.60</td>
      <td>21954833890.00</td>
      <td>1014062501.10</td>
      <td>12141122232.90</td>
      <td>3079217251.30</td>
      <td>1621264195.40</td>
      <td>-59.20</td>
    </tr>
    <tr>
      <th>Turkiye</th>
      <td>19263000000.00</td>
      <td>13835000000.00</td>
      <td>11190000000.00</td>
      <td>12450000000.00</td>
      <td>9507000000.00</td>
      <td>7522000000.00</td>
      <td>-61.00</td>
    </tr>
    <tr>
      <th>Australia</th>
      <td>46892808567.90</td>
      <td>42970225977.70</td>
      <td>48199372039.90</td>
      <td>60686639529.90</td>
      <td>38745129661.10</td>
      <td>17976843681.30</td>
      <td>-61.70</td>
    </tr>
    <tr>
      <th>United States</th>
      <td>511434000000.00</td>
      <td>474388000000.00</td>
      <td>380823000000.00</td>
      <td>214715000000.00</td>
      <td>315984000000.00</td>
      <td>137066000000.00</td>
      <td>-73.20</td>
    </tr>
    <tr>
      <th>Italy</th>
      <td>13303439230.20</td>
      <td>25656663794.80</td>
      <td>8737024578.70</td>
      <td>44249715319.10</td>
      <td>35760550299.50</td>
      <td>-17050399620.90</td>
      <td>-228.20</td>
    </tr>
  </tbody>
</table>
</div>




```python
## Plotting the results 

plt.figure(figsize=(11,5))
sns.barplot(x=fdi.index, y=fdi['perc_chg'], palette='rocket_r')
plt.title("% Change in FDI from 2015 to 2020")
plt.xticks(rotation =90)
plt.show()
```


        
<img width="940" height="586" alt="output_60_0" src="https://github.com/user-attachments/assets/6ee86bc9-018d-4c4a-9deb-16914c90a33e" />



```python
# Analyzing the Import-Export Aspects of the country:

df_final['net_exim_bal'] = df_final['Exports of goods and services'] - df_final['Imports of goods and services']
```


```python
df_final.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>year</th>
      <th>GDP</th>
      <th>GNI</th>
      <th>Inflation rate</th>
      <th>Unemployment rate</th>
      <th>Poverty rate</th>
      <th>Life expectancy</th>
      <th>Literacy rate</th>
      <th>Access to electricity</th>
      <th>...</th>
      <th>Foreign direct investment (FDI)</th>
      <th>Exports of goods and services</th>
      <th>Imports of goods and services</th>
      <th>Gross capital formation</th>
      <th>Agricultural land area</th>
      <th>Agricultural production index</th>
      <th>GDP_BN</th>
      <th>GNI_BN</th>
      <th>year_o</th>
      <th>net_exim_bal</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Argentina</td>
      <td>2015-01-01</td>
      <td>594749285413.21</td>
      <td>583615452086.54</td>
      <td>NaN</td>
      <td>7.58</td>
      <td>NaN</td>
      <td>76.60</td>
      <td>NaN</td>
      <td>99.70</td>
      <td>...</td>
      <td>11758994011.29</td>
      <td>10.71</td>
      <td>11.78</td>
      <td>15.56</td>
      <td>44.12</td>
      <td>104.14</td>
      <td>594.75</td>
      <td>583.62</td>
      <td>2015</td>
      <td>-1.07</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Argentina</td>
      <td>2016-01-01</td>
      <td>557532320662.95</td>
      <td>545251641127.71</td>
      <td>NaN</td>
      <td>8.09</td>
      <td>1.30</td>
      <td>76.11</td>
      <td>NaN</td>
      <td>99.90</td>
      <td>...</td>
      <td>3260164341.77</td>
      <td>12.53</td>
      <td>13.57</td>
      <td>14.27</td>
      <td>43.43</td>
      <td>101.71</td>
      <td>557.53</td>
      <td>545.25</td>
      <td>2016</td>
      <td>-1.04</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Argentina</td>
      <td>2017-01-01</td>
      <td>643628393281.36</td>
      <td>627200463933.82</td>
      <td>NaN</td>
      <td>8.35</td>
      <td>1.10</td>
      <td>76.54</td>
      <td>NaN</td>
      <td>100.00</td>
      <td>...</td>
      <td>11516861462.28</td>
      <td>11.32</td>
      <td>13.97</td>
      <td>15.16</td>
      <td>42.98</td>
      <td>106.82</td>
      <td>643.63</td>
      <td>627.20</td>
      <td>2017</td>
      <td>-2.65</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Argentina</td>
      <td>2018-01-01</td>
      <td>524819892360.18</td>
      <td>506094045059.70</td>
      <td>34.28</td>
      <td>9.22</td>
      <td>1.60</td>
      <td>76.77</td>
      <td>NaN</td>
      <td>100.00</td>
      <td>...</td>
      <td>11716769818.75</td>
      <td>14.44</td>
      <td>16.33</td>
      <td>15.25</td>
      <td>42.36</td>
      <td>92.20</td>
      <td>524.82</td>
      <td>506.09</td>
      <td>2018</td>
      <td>-1.89</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Argentina</td>
      <td>2019-01-01</td>
      <td>447754683615.22</td>
      <td>430166792070.57</td>
      <td>53.55</td>
      <td>9.84</td>
      <td>1.70</td>
      <td>76.85</td>
      <td>NaN</td>
      <td>100.00</td>
      <td>...</td>
      <td>6649187837.99</td>
      <td>17.92</td>
      <td>14.71</td>
      <td>14.20</td>
      <td>42.61</td>
      <td>113.14</td>
      <td>447.75</td>
      <td>430.17</td>
      <td>2019</td>
      <td>3.22</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 22 columns</p>
</div>




```python
# South American Countries:

plt.figure(figsize=(10,4))
sns.lineplot(x='year', y='net_exim_bal', data=df_final[df_final['country'].isin(['Argentina', 'Brazil','Mexico'])], hue='country', ci=False)
plt.show()
```


    
<img width="844" height="371" alt="output_63_0" src="https://github.com/user-attachments/assets/175dbe8d-a537-4183-b14d-6cc0b655f6f4" />



```python
# US and Canada:

plt.figure(figsize=(10,4))
sns.lineplot(x='year', y='net_exim_bal', data=df_final[df_final['country'].isin(['Canada','United States'])], hue='country', ci=False)
plt.show()
```


        
<img width="858" height="375" alt="output_64_0" src="https://github.com/user-attachments/assets/da4ab313-904d-4bef-b33c-1a4c6d9110bd" />



```python
plt.figure(figsize=(10,4))
sns.lineplot(x='year', y='net_exim_bal', data=df_final[df_final['country'].isin(['India'])], hue='country', ci=False)
plt.show()
```


        
<img width="858" height="371" alt="output_65_0" src="https://github.com/user-attachments/assets/70c46191-6b9c-4126-a4f3-c9bb4207402a" />



```python
df_final.to_excel("GDP20_Data.xlsx")
```


```python

```
--

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



---

## Key Findings

GDP and GNI show near-perfect correlation (1.00) → strong economic consistency.

Inflation tends to negatively affect life expectancy and GDP growth.

FDI inflows correlate positively with exports, suggesting global investment supports trade.

Unemployment and poverty rates are interlinked with education and infrastructure gaps.

Developed nations show stable inflation and strong GNI, while emerging economies exhibit volatility.

---

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


---


## Author & Contact
Rahul Googikoll
📍 Goa, India
Java Full Stack Developer | Aspiring Data Analyst & Data Engineer
📧 Email: raulgoogikoll23@gmail.com
🔗 LinkedIn: https://www.linkedin.com/in/rahulgoogikoll
🔗 Portfolio: https://master--rahulgoogikolll2001.netlify.app/
