# G20 & Global Economic Indicators Analysis: Driving Strategic Decisions with Data

**Repository Status:** Complete | **Analysis Period:** 2000–2023 | **Focus:** Global Development Disparity & Economic Levers

---

## Overview

This project provides a **comprehensive, evidence-based Exploratory Data Analysis (EDA)** of global socioeconomic indicators, moving beyond simple metrics to quantify structural relationships that drive national prosperity and risk.

We identify the critical drivers of economic growth, highlight the entrenched **Global Development Disparity**, and provide **data-driven insights** crucial for policymakers, investors, and product analysts focusing on the G20 and major global economies.

---

## Business Problem & Strategic Value

Economic stability and growth are influenced by complex, correlated factors. This project addresses key strategic challenges by:

1. **Quantifying Risk:** Using outlier detection and correlation analysis to isolate markets facing acute instability (e.g., high inflation, low capital flow).
2. **Identifying Growth Levers:** Determining which social indicators (Literacy, Life Expectancy) and capital indicators (FDI, GCF) have the highest verifiable impact on reducing poverty and boosting GDP.
3. **Informing Global Strategy:** Providing a clear, segmented view of the "Dual-Speed Global Economy" for targeted investment and policy interventions.

---

## Key Findings: The Dual-Speed Global Economy

Analysis of the data reveals two fundamental realities: **Social Convergence** and **Economic Centralization**.

### 1. Entrenched Economic Centralization

- **Wealth is Concentrated:** **GDP and GNI** show an **Extreme Right Skew**, with $\approx 10.5\%$ of countries accounting for the vast majority of global wealth. This concentration is reinforced by **Foreign Direct Investment (FDI)**, which is highly correlated ($\approx +0.8$) with national wealth, indicating capital prefers large, stable markets.
- **Poverty and Unemployment:** High Poverty is primarily an issue of acute national crisis ($\approx 11.5\%$ outliers) and is **strongly negatively correlated ($\approx -0.8$) with GDP/GNI**. Economic growth remains the most powerful tool for inclusion.
- **Inefficient Investment:** The **Joint Plot of Gross Capital Formation (GCF) vs. Poverty Rate** shows that high investment alone is not sufficient. A cluster of outliers shows **high GCF (up to 33%) concurrent with high Poverty**, suggesting inefficient, non-inclusive capital projects.

### 2. Universal Social Convergence

- **Health and Education:** **Life Expectancy** ($\mathbf{0\%}$ outliers) and **Literacy Rate** ($\mathbf{4.5\%}$ outliers) are highly standardized globally.
- **Infrastructure Baseline:** **Mobile Phone Subscriptions** and **Exports/Imports** show $\mathbf{0\%}$ outliers, reinforcing that trade participation and basic connectivity are near-universal.
- **Policy Link:** **Literacy Rate** is strongly correlated ($\approx +0.7$) with **Access to Electricity**, confirming that human capital and basic infrastructure development occur in parallel.

### 3. Critical Correlation Insights

- **Inflation's Cost:** Inflation has a moderate negative correlation ($\approx -0.45$) with **Life Expectancy**, confirming monetary instability directly degrades public health and welfare.
- **FDI Decoupling:** **FDI** shows a **weak negative correlation ($\approx -0.2$) with Exports/Imports**, suggesting that capital inflows are often driven by access to the domestic market, not by using the host country as an export platform.

---

## Data Cleaning & Preparation

| **Step** | **Rationale** |
| --- | --- |
| **Outlier Check/Handling** | Used Boxplots to identify extreme values in **FDI** and **Inflation**; handled to ensure robust correlation and modeling. |
| **Missing Value Handling** | Utilized interpolation and mean imputation to maintain dataset integrity for time-series and cross-sectional analysis. |
| **Column Refinement** | Removed redundant columns (`GDP_BN`, `GNI_BN`, etc.) and ensured `Year` was datetime-typed for accurate trend analysis. |

---

## Exploratory Data Analysis (EDA)

The EDA focused on **pattern recognition, anomaly detection, and relationship mapping** to derive strategic insights.

### Key Analyses Conducted:

1. **Distribution Analysis:** Used **Histograms** to verify the extreme skew in wealth (GDP/GNI) and **Outlier Percentage** chart to quantify global heterogeneity (e.g., **Access to Electricity** is the most non-conforming metric at $\approx 17.5\%$ outliers).
2. **Correlation Analysis:** Used **Heatmaps** to quantify systemic relationships, finding a strong link between GDP and poverty reduction, and the unexpected decoupling of FDI and exports.
3. **Joint Plot Analysis:** Explored complex non-linear relationships, such as **Gross Capital Formation vs. Poverty** (identifying ineffective investment) and **Education Spending vs. Life Expectancy** (identifying diminishing returns on education spending).
4. **Trend Analysis:** Visualized country-specific changes in **Trade Balance** and **Life Expectancy** (2015-2020) to analyze resilience to global shocks (e.g., COVID-19 impact on US/Mexico Life Expectancy vs. gains in South Africa/India).

---

## Research Questions & Insights

| **Research Question** | **Evidence-Based Insight** | **Strategic Recommendation** |
| --- | --- | --- |
| Does GDP strongly correlate with GNI? | **Yes, correlation $\approx 1.00$**. Highly interchangeable economic metrics. | Simplify financial modeling by focusing efforts on one core national wealth metric. |
| Is inflation inversely related to life expectancy? | **Yes, moderate negative correlation ($\approx -0.45$)**. | Monetary policy (fighting inflation) should be viewed as a critical public health strategy. |
| Does FDI boost exports? | **⚖️ Weak positive correlation found** ($\approx +0.1$ to $+0.2$). | Policy must mandate export targets for FDI projects to maximize trade impact. |
| Are literacy rates linked to unemployment reduction? | **Moderate correlation observed** (Stronger link to poverty reduction). | Focus on job **quality** and wage policy, as high literacy does not guarantee high-quality employment (the "working poor" problem). |
| Which countries show best GDP–Inflation balance? | Developed economies like the US, Japan, Germany show stability; **South Africa** and **India** showed strong recent life expectancy gains. | **Investment Opportunity:** Target nations with low FDI but strong social scores (Literacy, Access to Electricity) as under-penetrated emerging markets. |

---

## Tools & Technologies

- **Language:** Python
- **Libraries:** **Pandas**, **NumPy**, **Matplotlib**, **Seaborn** (for professional visualizations), **SciPy** (for statistical tests)
- **Environment:** Jupyter Notebook
- **Version Control:** GitHub

---

## Visualizations

- **Correlation Heatmap:** Quantifying all inter-variable dependencies.
- **Histograms & Boxplots:** Distribution and outlier checks across all 15+ indicators.
- **Joint Plots:** Detailed analysis of complex relationships (e.g., GCF vs. Poverty).
- **Trend Charts:** Tracking country-specific changes (e.g., % change in FDI/Life Expectancy).

---

## Future Scope

1. **Advanced Machine Learning:** Implement Regression or Time-Series models to **predict future GDP growth** based on current FDI, Inflation trends, and Literacy levels.
2. **Cluster Analysis:** Employ K-Means or DBSCAN to automatically group the 114 countries into distinct economic stability clusters for precise peer benchmarking.
3. **API Integration:** Expand analysis to $200+$ countries using live World Bank/IMF APIs for real-time data ingestion and analysis.

---
## The Dual-Speed Global Economy

<img width="1389" height="990" alt="output_32_0" src="https://github.com/user-attachments/assets/f095e384-c4c5-4901-8516-066914a7166b" />

This collection of histograms offers a powerful, data-driven narrative about the **Progressive but Unequal World**. It moves beyond simple metrics to reveal the deep structural differences between nations, providing a critical foundation for strategic policy and product decisions.

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

The Global Convergence: Social Development IndicatorsUniversal access to basic human development is an achievable global reality. This convergence creates a massive, *qualitatively similar* global consumer base.

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

--

## Outlier Percentage 

<img width="932" height="724" alt="504559803-49d12ec6-16a8-4ec1-af18-e1c9cfb6937c" src="https://github.com/user-attachments/assets/8c8e45c7-6a7e-4597-9fd6-7bb640a7e129" />



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
## Correlation Matrix

<img width="900" height="920" alt="68e80b34-084e-4239-b3b7-c3bca0780662" src="https://github.com/user-attachments/assets/2c31fb8d-3f4d-40ba-a7dc-1104af17c98c" />


This heatmap is a **Correlation Matrix**, which reveals the strength and direction of linear relationships between 15+ socioeconomic indicators. For an analyst, this is the most critical tool for understanding **systemic interdependencies** how a change in one factor is associated with a change in another across different countries.

The color scale ranges from **Red (strong positive correlation, $+1.0$)** to **Deep Blue (strong negative correlation, $-1.0$)**.

## Key Strategic Insights from Core Correlations

### 1. The Power of Economic Prosperity

The relationships involving GDP and GNI are the strongest and most telling, confirming that national wealth is the engine for global development.

- **Poverty Reduction:** **GDP_BN** and **GNI_BN** have a **very strong negative correlation** with the **Poverty Rate** (around $\mathbf{-0.8}$). This confirms the foundational policy truth: economic growth is the most effective way to reduce poverty.
- **Employment:** **Unemployment Rate** is also **strongly negatively correlated** with both GDP and GNI (around $\mathbf{-0.9}$). Wealthier nations consistently maintain lower unemployment, highlighting the effectiveness of industrialized economies at job creation.
- **Investment Magnet:** The high correlation between **Foreign Direct Investment (FDI)** and $\text{GDP/GNI}$ (around $\mathbf{+0.8}$) shows that global capital flows overwhelmingly to the largest, most stable economies, reinforcing the existing global wealth gap.

---

### 2. Social Development: A Web of Positive Feedback

Social indicators often rise together, suggesting that investment in one area benefits others.

- **Health and Education:** The **Poverty Rate** is **strongly negatively correlated** with **Life Expectancy** ($\mathbf{-0.7}$) and **Literacy Rate** ($\mathbf{-0.7}$). This reveals a vicious cycle: poverty prevents access to both education and healthcare, leading to lower human capital.
- **Literacy and Infrastructure:** **Literacy Rate** is **highly correlated** with **Access to electricity** ($\mathbf{+0.7}$). This suggests that countries prioritizing the development of human capital (education) are also effective at building basic modern infrastructure (energy).

---

### 3. Trade vs. Investment Dynamics

The correlations related to trade and investment reveal different strategic drivers.

- **Trade Balance:** **Exports of goods and services** and **Imports of goods and services** are **perfectly correlated** ($\mathbf{+1.0}$). This is a necessary reality of global trade, indicating countries that are active sellers are also active buyers.
- **FDI Decoupling:** **Foreign Direct Investment (FDI)** has a surprisingly **weak, slightly negative correlation** with **Exports** and **Imports** (around $\mathbf{-0.2}$).
    - **Analyst Story:** This suggests that much of FDI is driven by a desire to **penetrate domestic markets** (selling products *within* the country) or securing local resources, rather than using the host nation as a hub for international export trade.

---

### 4. Non-Obvious Relationships

These moderate correlations require a more nuanced interpretation:

- **Unemployment vs. Poverty ($-0.5$):** The correlation, though negative, is only moderate. **Analyst Story:** This weak link suggests that reducing unemployment doesn't automatically solve poverty. It points to a significant problem of the **working poor**—people who have jobs but whose wages are too low to escape poverty.
- **Agricultural Production Index vs. GDP ($-0.2$):** A weak negative correlation. **Analyst Story:** This is typical of developed economies. As a nation's $\text{GDP}$ rises, its economic focus shifts from agriculture to higher-value services and manufacturing, causing the agricultural sector's importance (and relative growth) to decline.

---
## Analysis of GDP and GNI Relationship

<img width="412" height="390" alt="96e0bc18-d170-4599-add5-cdb484d9f76d" src="https://github.com/user-attachments/assets/d7477bb9-9e8a-448e-bf84-2996ff2bcedf" />

This image is a **Joint Plot** showing the relationship between **GDP (Gross Domestic Product)** and **GNI (Gross National Income)**.

### Core Relationship

The scatter plot shows a **near-perfect positive linear relationship** between a country's GDP and its GNI. The data points cluster tightly along a straight line, indicating that as a country's GDP increases, its GNI increases by a proportional amount. This strong association is expected because:

- **GDP** measures the total value of goods and services produced **within** a country's borders.
- **GNI** measures GDP plus net income received from abroad (e.g., remittances, foreign investments) and minus income paid to non-residents.
- For most countries, the net difference between income generated domestically (GDP) and income received/paid internationally (GNI) is small relative to the total size of the economy, leading to a near $1:1$ correspondence.

### Distribution (Histograms)

The histograms on the top and right axes reinforce the findings from the previous analyses regarding economic disparity:

- Both GDP_BN and GNI_BN are **extremely right-skewed**.
- The vast majority of countries are clustered near **zero** (low GDP/GNI), represented by the high bars on the left of the top histogram and the bottom of the right histogram.
- A few countries are extreme outliers, represented by the sparse bars stretching out toward the high values (15,000 to 22,000).

### Strategic Implication

This plot confirms that for almost all global economic analysis, **GDP and GNI are virtually interchangeable**.

- **Data Validation:** The tight relationship validates the consistency of the underlying economic reporting.
- **Focus on the Skew:** The key takeaway is the **extreme concentration of wealth**. Economic analysis and market sizing must focus on the two distinct groups: the large mass of countries with low GDP/GNI and the few economic giants driving the high values. The total number of high-wealth countries is small, but their economic impact is massive.

---
## Analysis of Capital Formation and Poverty

<img width="385" height="390" alt="e8b46a11-7155-4919-b3c2-16ce33c9b3a9" src="https://github.com/user-attachments/assets/cb6ec426-95aa-40ba-a9c6-ce16f1dcda63" />

This image is a **Joint Plot** illustrating the relationship between **Gross Capital Formation (%)** and **Poverty Rate (%)**. It reveals a complex, non-linear relationship between investment and poverty across countries.

### 1. The Core Relationship: High Investment, Low Poverty (Mostly)

The overall pattern suggests a general trend, but with major exceptions:

- **Low Poverty Cluster:** The vast majority of countries show a **low Poverty Rate (below 5%)** across a wide range of **Gross Capital Formation (GCF) rates (from 15% to 45%)**. This suggests that once a country's investment in its economy is moderately high, poverty is often kept low.
- **The Investment Threshold:** Countries with **very low GCF (below 18%)** tend to have moderately higher poverty (up to 7%). This hints that a minimum level of economic investment is necessary to suppress mass poverty.
- **The Zero-Poverty Ceiling:** It is important to note that **no country with a GCF above 35% has a poverty rate above 5%**. High levels of reinvestment in the economy appear to act as a powerful safeguard against extreme poverty.

### 2. The Vertical Outlier Cluster: Investment Without Immediate Payoff

The most distinct feature is the **vertical cluster of outliers** around a GCF of **33%**:

- These countries have a **high rate of investment (GCF $\approx 33\%$)** but simultaneously show **very high Poverty Rates (ranging from 10% up to 22%)**.
- **Analyst Story:** This scenario is often indicative of **inefficient or misdirected investment**. High capital formation here might be driven by mega-projects (e.g., in mining, energy infrastructure) that are highly capital-intensive but **fail to generate widespread employment or income** for the population. This points to severe **income inequality** or systemic leakage where the benefits of investment do not trickle down.

### 3. Distribution (Histograms)

- **Poverty Rate (Right Histogram):** Highly skewed, with most countries clustered at very low poverty rates (0-2.5%), reinforcing the idea that high poverty is an issue of acute national crisis for a few.
- **Gross Capital Formation (Top Histogram):** Shows a fairly spread-out distribution, indicating that countries vary significantly in the percentage of their GDP they reinvest.
Conclusion for Policy/Strategy:** While investment (GCF) is a necessary condition for low poverty, it is **not sufficient**. Policy must focus not just on the *level* of investment but on its **quality and inclusivity** to ensure it translates into broad-based job creation and poverty reduction.
---
## Analysis of Education Spending vs. Life Expectancy

<img width="385" height="390" alt="5b4670e4-5c8f-4a79-88bf-2289b766434f" src="https://github.com/user-attachments/assets/0f43ff7c-b9d3-49f0-94cb-802030936e67" />

This **Joint Plot** explores the relationship between **Government Expenditure on Education (% of GDP)** and **Life Expectancy (Years)** across various countries.

The analysis shows a complex, **non-linear relationship** that suggests public investment in education is a necessary but not sufficient factor for achieving high life expectancy.

### 1. The Core Relationship: Diminishing Returns

There is a weak, overall **positive correlation**, but the data points form distinct clusters rather than a clean line:

- **Low Spenders, Low Expectancy (Bottom-Left):** Countries spending less than $2\%$ of GDP on education consistently have lower life expectancy (below 70 years). This suggests that a **minimum commitment to education funding is essential** for basic health and development gains.
- **The Optimal Range (Middle Cluster):** The vast majority of countries spend between **$3\%$ and $6\%$** of GDP on education. Within this range, life expectancy widely varies, from $\mathbf{70}$ to $\mathbf{85}$ years.
    - **Analyst Insight:** This wide vertical spread means that **high education spending alone does not guarantee long life expectancy**. Factors like healthcare spending, diet, environment, or income inequality are likely more dominant drivers of health outcomes in this range.
- **High Spenders, Varied Results (Right Cluster):** Countries spending the most (over $5.5\%$) on education do not show a corresponding, guaranteed peak in life expectancy. Results are mixed, ranging from the mid-60s to over 80 years. This indicates a case of **diminishing returns** or that the *quality and efficiency* of the education and health systems matter more than the raw percentage spent on education.

### 2. The Outliers

- **The Bottom-Right Outlier:** There is a small group of countries with **high education spending (around $6\%$ of GDP)** but **low life expectancy (mid-60s)**. This is a critical case for policy analysis, suggesting a severe failure to translate public investment into human welfare, likely due to a crisis in the healthcare system, high rates of disease, or systemic poverty.

### 3. Distribution (Histograms)

- **Government Expenditure (Top Histogram):** Shows a fairly normal, bell-shaped distribution centered around $4\%$ to $5\%$ of GDP. This indicates a **global consensus** on the typical level of education funding.
- **Life Expectancy (Right Histogram):** Shows a distribution heavily skewed towards the higher end (75 to 85 years), confirming the general global success in extending life spans.

**Conclusion for Policy/Strategy:** Investment in education is crucial to get countries off the low end of the life expectancy scale. However, for most countries already in the moderate spending range, **additional spending on education is unlikely to be the primary driver for further health gains**. Policy focus should shift to **healthcare infrastructure, sanitation, and addressing income inequality** to push life expectancy toward the maximum.

---
## Analysis of Life Expectancy Trends (2015-2020)


<img width="922" height="586" alt="535efa0b-8b83-4eb8-973c-f5e64e9b9ec4" src="https://github.com/user-attachments/assets/227e5037-c606-4a0f-9316-6fa292a50fc9" />

This bar chart illustrates the **Percentage Change in Life Expectancy from 2015 to 2020** for a selection of countries. This period is critical as it covers the immediate pre-pandemic years and the initial year of the COVID-19 pandemic, which significantly impacted global health outcomes.

The data clearly separates countries into two strategic groups: those that managed to achieve **health gains** and those that experienced **significant reversals**.

---

### Group 1: Countries with Life Expectancy Gains (Top Performers)

The countries on the left side showed an increase (positive change) in life expectancy during this period.

- **Emerging Economies Drive Gains:** **South Africa** and **India** lead with some of the highest percentage gains (around $1.8\%$ and $1.3\%$). This often reflects major progress in public health, access to antiretroviral therapies (in the case of South Africa), or significant reductions in child mortality from previously lower baselines.
- **Steady Growth in Asia-Pacific:** **Korea, Rep., China, Japan,** and **Australia** all registered strong, positive growth (over $1.0\%$ for the top three). This suggests continued improvements in healthcare and aging populations were not yet severely affected by major external shocks during this window.
- **Modest Western Gains:** **Germany** and the **Russian Federation** showed marginal to modest gains, suggesting their life expectancy was already high and approaching a global ceiling, or that they faced early, slow-down factors.

---

### Group 2: Countries with Life Expectancy Declines (Bottom Performers)

The countries on the right side experienced a decline (negative change) in life expectancy, with some showing profound setbacks.

- **Severe Reversals (High Decline):**
    - **Mexico** recorded the most drastic decline, falling over $\mathbf{-5.5\%}$.
    - The **United States** experienced the second-largest drop at about $\mathbf{-2.6\%}$.
    - **Indonesia** and **Argentina** also showed substantial declines (around $\mathbf{-1.0\%}$ to $\mathbf{-1.5\%}$).
    - **Analyst Interpretation:** Given the time frame (2015-2020), these significant drops are highly suggestive of the **initial impact of the COVID-19 pandemic** on these specific countries, which were heavily affected in terms of mortality and overwhelmed healthcare systems. For the US and Mexico, pre-existing issues like the opioid crisis (US) and rising rates of non-communicable diseases (both) likely exacerbated the decline.
- **Marginal Declines:** **France, Saudi Arabia, Canada, Italy, and Brazil** showed small, negative changes (less than $-1.0\%$). While these still represent a loss, the impact was less severe than the US or Mexico.

## Strategic Takeaways

1. **Baseline Matters:** Countries starting with lower life expectancy (e.g., South Africa, India) had the largest percentage room for improvement.
2. **Pandemic Shock:** The profound negative trends in countries like the **US and Mexico** highlight the **vulnerability of even high-income/middle-income economies** to major health crises, especially those with pre-existing health and economic inequalities.
3. **Policy Focus:** The data provides clear evidence of **divergent health outcomes** during a critical period. Policy analysts should investigate whether the top-gaining countries implemented specific, effective health policies that the declining countries failed to adopt or sustain.

---
<img width="940" height="586" alt="8f730fe4-015f-44cf-b083-ba0afadf85c8" src="https://github.com/user-attachments/assets/8e070dab-c479-4d4f-966d-1823aa63e29a" />

This bar chart illustrates the **Percentage Change in Foreign Direct Investment (FDI) from 2015 to 2020** for a selection of major global economies. This data highlights which countries successfully attracted or retained capital, and which experienced significant divestment, during a period of moderate economic growth followed by the initial global shock of 2020.

## Analysis of Global Capital Flow Trends (2015-2020)

The chart reveals an extremely polarized landscape for capital flow, demonstrating that investment growth was highly concentrated in a few markets while many others saw stagnation or massive withdrawal.

---

### Group 1: Explosive FDI Growth (The Capital Magnets)

Thse countries achieved phenomenal percentage growth in attracting FDI, often starting from a lower base in 2015 or successfully completing major regulatory reforms.

- **Japan's Dominance:** **Japan** stands alone with an unprecedented growth rate of over $\mathbf{1,100\%}$. This massive surge suggests a fundamental shift in its investment climate, likely driven by successful governance reforms aimed at making the traditionally difficult-to-enter market more appealing to foreign capital.
- **Strong Gains in Developed & Emerging Markets:** The **United Kingdom** ($\approx 250\%$), **Germany** ($\approx 200\%$), and **Korea, Rep.** ($\approx 150\%$) show strong triple-digit growth. This reflects their status as secure, high-value destinations.
- **Emerging Market Momentum:** **South Africa** and **India** also saw significant positive growth, indicating their rising importance as centers for global manufacturing and service outsourcing.

---

### Group 2: Stagnation and Decline (The Divestment Zones)

The right side of the chart shows a long list of countries where FDI growth was flat or, more commonly, negative.

- **Flat Growth:** **China** and **Indonesia** show minimal positive change, suggesting they maintained their investment levels but did not see the rapid growth experienced by their competitors.
- **Significant Declines (Negative Growth):** A large number of countries, including major Western economies, experienced a **net outflow or significant reduction** in FDI.
    - **Italy** recorded the most severe decline, losing over $\mathbf{200\%}$ of its 2015 FDI level. This is a red flag, pointing to deep issues of economic stability, political risk, or regulatory challenges.
    - The **United States** also saw a notable decline, losing capital in the net balance, possibly due to shifting tax policies or reduced attractiveness relative to rapidly growing markets.
    - **Brazil, Canada, France,** and **Argentina** all experienced negative growth, suggesting investors found their markets less appealing for long-term capital deployment during this period.

## Strategic Takeaways

1. **Japan's Policy Success:** The $\mathbf{1,100\%}$ gain for Japan is the single most important finding, highlighting the transformative power of **structural and regulatory reform** on attracting global capital, even in mature economies.
2. **Capital Flight:** The concentration of negative change in major economies like Italy and the United States suggests that global capital is becoming **highly sensitive to risk and returns**, bypassing established markets that show vulnerability or lack compelling growth opportunities.
3. **FDI as a Leading Indicator:** The stark polarization in this chart signals **future economic divergence**. Countries that successfully attracted capital (Group 1) are likely poised for stronger future economic growth, while those losing capital (Group 2) face headwinds in sustaining long-term development.

---
## Analysis of Global Capital Flow Trends (2015-2020)


<img width="940" height="586" alt="504560452-6ee86bc9-018d-4c4a-9deb-16914c90a33e" src="https://github.com/user-attachments/assets/cbc51d65-9e0f-4993-9ff4-eb6d69d1dd5a" />

This bar chart illustrates the **Percentage Change in Foreign Direct Investment (FDI) from 2015 to 2020** for a selection of major global economies. This data highlights which countries successfully attracted or retained capital, and which experienced significant divestment, during a period of moderate economic growth followed by the initial global shock of 2020.

The chart reveals an extremely polarized landscape for capital flow, demonstrating that investment growth was highly concentrated in a few markets while many others saw stagnation or massive withdrawal.

---

### Group 1: Explosive FDI Growth (The Capital Magnets)

These countries achieved phenomenal percentage growth in attracting FDI, often starting from a lower base in 2015 or successfully completing major regulatory reforms.

- **Japan's Dominance:** **Japan** stands alone with an unprecedented growth rate of over $\mathbf{1,100\%}$. This massive surge suggests a fundamental shift in its investment climate, likely driven by successful governance reforms aimed at making the traditionally difficult-to-enter market more appealing to foreign capital.
- **Strong Gains in Developed & Emerging Markets:** The **United Kingdom** ($\approx 250\%$), **Germany** ($\approx 200\%$), and **Korea, Rep.** ($\approx 150\%$) show strong triple-digit growth. This reflects their status as secure, high-value destinations.
- **Emerging Market Momentum:** **South Africa** and **India** also saw significant positive growth, indicating their rising importance as centers for global manufacturing and service outsourcing.

---

### Group 2: Stagnation and Decline (The Divestment Zones)

The right side of the chart shows a long list of countries where FDI growth was flat or, more commonly, negative.

- **Flat Growth:** **China** and **Indonesia** show minimal positive change, suggesting they maintained their investment levels but did not see the rapid growth experienced by their competitors.
- **Significant Declines (Negative Growth):** A large number of countries, including major Western economies, experienced a **net outflow or significant reduction** in FDI.
    - **Italy** recorded the most severe decline, losing over $\mathbf{200\%}$ of its 2015 FDI level. This is a red flag, pointing to deep issues of economic stability, political risk, or regulatory challenges.
    - The **United States** also saw a notable decline, losing capital in the net balance, possibly due to shifting tax policies or reduced attractiveness relative to rapidly growing markets.
    - **Brazil, Canada, France,** and **Argentina** all experienced negative growth, suggesting investors found their markets less appealing for long-term capital deployment during this period.

## Strategic Takeaways

1. **Japan's Policy Success:** The $\mathbf{1,100\%}$ gain for Japan is the single most important finding, highlighting the transformative power of **structural and regulatory reform** on attracting global capital, even in mature economies.
2. **Capital Flight:** The concentration of negative change in major economies like Italy and the United States suggests that global capital is becoming **highly sensitive to risk and returns**, bypassing established markets that show vulnerability or lack compelling growth opportunities.
3. **FDI as a Leading Indicator:** The stark polarization in this chart signals **future economic divergence**. Countries that successfully attracted capital (Group 1) are likely poised for stronger future economic growth, while those losing capital (Group 2) face headwinds in sustaining long-term development.

---


<img width="844" height="371" alt="504560521-175dbe8d-a537-4183-b14d-6cc0b655f6f4" src="https://github.com/user-attachments/assets/642284da-de55-4a00-bb76-9bd8c1d4f3ce" />

This analysis is based on the final uploaded plot, a line chart showing the **Net Export/Import Balance (net_exim_bal)** for three major Latin American economies—**Argentina, Brazil, and Mexico**—from 2015 to 2020. This metric is a proxy for the trade balance, where a positive value indicates a trade surplus and a negative value indicates a trade deficit.

## Net Trade Balance Dynamics in Latin America (2015-2020)

### 1. The Core Trend: Convergence to Trade Surpluses

Despite starting in deficit positions in 2015, all three countries show a strong recovery and end the period with a positive or near-positive trade balance by 2020. This convergence suggests a regional trend of **export-driven recovery or import compression** following global economic instability.

| **Country** | **2015 Balance** | **2020 Balance** | **Key Dynamics** |
| --- | --- | --- | --- |
| **Argentina** | -1.0 | +3.0 | **Highest volatility.** Swings from a deficit to the highest surplus, peaking sharply in 2019. |
| **Brazil** | -1.0 | +0.5 | **Most stable growth.** Consistently improved balance until 2017, dipped, and then recovered. |
| **Mexico** | -2.0 | +1.5 | **Largest initial deficit, strongest sustained recovery.** Steady improvement from a low point. |

---

### 2. Country-Specific Narratives

### **Argentina: The Volatility Story**

Argentina is the most volatile country on the chart:

- **Initial Deficit (2015-2017):** Held a moderate deficit around -1.0, dipping to its lowest point in 2017 (around -2.5).
- **The Sharp Pivot (2018-2019):** Experienced a massive turnaround, skyrocketing from a deficit of -2.0 in 2018 to a peak surplus of over +3.0 in 2019.
- **Analyst Interpretation:** This massive, abrupt shift is highly indicative of an **economic crisis and subsequent currency devaluation** in 2018-2019. A severe currency devaluation makes exports cheap (boosting them) and imports expensive (suppressing them), resulting in a rapid, policy- or crisis-driven improvement in the trade balance.

### **Brazil: The Stagnating Recovery**

Brazil shows a smoother but less pronounced recovery:

- **Gradual Improvement (2015-2017):** Improved its balance from -1.0 to a small surplus ($\approx +0.7$).
- **Reversal and Recovery (2017-2020):** Experienced a downturn to a deficit in 2019 before stabilizing at a small surplus by 2020 ($\approx +0.5$).
- **Analyst Interpretation:** The moderate swings suggest a more **gradual and managed adjustment** to global trade conditions, perhaps less reliant on sudden currency shocks than Argentina.

### **Mexico: The Export-Engine Recovery**

Mexico started with the deepest deficit but achieved the most consistent, positive trajectory:

- **Deep Deficit (2015-2018):** Held a large deficit around -2.0.
- **Strong, Continuous Ascent (2018-2020):** Shows the steepest consistent increase in the latter half of the period, ending with a strong surplus ($\approx +1.5$).
- **Analyst Interpretation:** Given its proximity and integration with the US economy (NAFTA/USMCA), Mexico's steady improvement is likely driven by **robust manufacturing and export growth**, positioning it as a resilient hub for international supply chains.

---

### 3. Strategic Takeaway

- **Risk vs. Stability:** The chart highlights **Argentina's high economic volatility**, making it a riskier market for long-term planning, versus **Mexico's consistent, upward trade performance**, which suggests greater stability for export-oriented businesses.
- **Drivers of Trade Balance:** The data implies that while **Brazil** and **Mexico** achieved gains through organic or managed adjustments, **Argentina's trade surplus was primarily a consequence of severe economic instability** (devaluation) rather than sustained export competitiveness.


---
## Trade Balance Trends: Canada vs. United States (2015-2020)


<img width="858" height="375" alt="fd5bfda2-7bde-4a43-b616-75d806b1101b" src="https://github.com/user-attachments/assets/a4b6d196-8f4a-40f1-a93e-bb36e307570b" />

This line chart illustrates the **Net Export/Import Balance (net_exim_bal)** for **Canada and the United States** from 2015 to 2020. Since the values are all negative, both countries ran a persistent **trade deficit** throughout the period. The chart tracks the size of these deficits relative to each country's GDP

Both North American giants consistently imported more than they exported, but they followed different trajectories and maintained different deficit magnitudes.

### 1. Magnitude: Canada's Larger Deficit

- **Canada's Deficit is Consistently Larger:** Throughout the entire six-year period, Canada's trade deficit (represented by the blue line) was **always larger** than the U.S. deficit (orange line).
    - In 2015, Canada's deficit was around $\mathbf{-2.45}$ while the U.S. deficit was around $\mathbf{-2.85}$. (Note: Since the scale is negative, the higher absolute value, e.g., $-2.85$, represents a smaller deficit relative to GDP).
    - In 2020, Canada's deficit was $\mathbf{-2.2}$ and the U.S. deficit was $\mathbf{-2.95}$.
- **Analyst Insight:** Relative to the size of its economy, Canada relies more heavily on imports or has a lower structural export capacity compared to the U.S.

### 2. Trajectory: Canada's Volatility, U.S. Stability

### **Canada (Blue Line): Volatile, Crisis-Driven Swings**

Canada's trade balance showed significant volatility:

- **Initial Improvement (2015-2019):** The deficit gradually narrowed from $-2.45$ in 2015 to a peak 'best' balance of nearly $\mathbf{-1.4}$ in 2019. This improvement suggests either strong export growth or effective import management during this period.
- **The Sharp Reversal (2019-2020):** The balance experienced a **severe, sharp widening** in 2020, dropping back to $\mathbf{-2.2}$.
- **Interpretation:** The sharp 2020 deterioration is likely attributable to the **initial COVID-19 pandemic shock**, which may have disrupted key Canadian export sectors (e.g., energy, commodities) while reliance on certain imports remained.

### **United States (Orange Line): Small Swings, Persistent Deficit**

The U.S. trade balance was relatively stable, oscillating within a tight range:

- The deficit stayed between $\mathbf{-2.65}$ (best balance in 2016 and 2019) and $\mathbf{-2.95}$ (worst balance in 2020).
- **Interpretation:** The U.S. deficit is structural. It is primarily driven by its role as the world's largest consumer market and the high value of the U.S. dollar, which makes imports cheaper. The minimal volatility suggests that while the economy is massive, the underlying trade imbalance is deeply entrenched and less susceptible to annual policy or minor economic shifts.

### 3. Strategic Takeaway

- **Product & Policy Risk:** **Canada's trade balance is more sensitive to global disruptions** (as seen in the 2020 drop) than the U.S. Policymakers in Canada might need to focus more on diversifying export markets or stabilizing key industries.
- **Investment Opportunity:** Both countries present a massive, import-driven market, but the U.S. offers the **largest and most stable deficit environment**, making it a highly predictable target market for foreign exporters.

---
## Trade Balance Dynamics for India (2015-2020)


<img width="858" height="371" alt="504560663-70c46191-6b9c-4126-a4f3-c9bb4207402a" src="https://github.com/user-attachments/assets/f58a2a12-ed27-42b7-b7a4-62d8e9fb24e2" />

This image is a line chart showing the **Net Export/Import Balance (net_exim_bal)** for **India** from 2015 to 2020. This metric is expressed as a negative value, indicating that India maintained a persistent **trade deficit** throughout the period.

The chart reveals a period of increasing trade deficit followed by a dramatic reversal, culminating in a significant improvement in the balance by 2020.

### 1. The Trend: Deepening Deficit Followed by Sharp Recovery

- **Initial Improvement (2015-2016):** The deficit initially narrowed slightly, moving from $\mathbf{-2.3}$ in 2015 to its best point of $\mathbf{-1.75}$ in 2016.
- **Deepening Deficit (2016-2018):** The deficit then widened significantly for two years, reaching its lowest point (largest deficit) of $\mathbf{-3.7}$ in 2018. This suggests a period where domestic demand for imports outpaced export growth, or a lag in global trade.
- **The Sharp Reversal (2018-2020):** From 2018, the trade balance saw a strong and consistent recovery, dramatically narrowing the deficit to approximately $\mathbf{-0.5}$ by 2020.

### 2. Strategic Interpretation

- **2018 as a Turning Point:** The year 2018 marks a critical inflection point. The sharp narrowing of the trade deficit post-2018 can be attributed to several factors typical in emerging markets, including:
    - **Currency Devaluation:** A decline in the value of the Indian Rupee would make imports more expensive (suppressing them) and exports cheaper (boosting them), rapidly improving the trade balance.
    - **Domestic Policy Shifts:** Government policies aimed at promoting exports (e.g., incentive schemes) or discouraging non-essential imports (e.g., tariff increases).
    - **Global Shock (2020):** The final, significant jump toward zero in 2020 is likely amplified by the **initial COVID-19 pandemic shock**, which simultaneously crashed global demand for oil (a major Indian import) while potentially disrupting local supply chains, limiting the ability to import goods.
- **Goal Proximity:** Ending the period at $\mathbf{-0.5}$ shows India achieved its **smallest trade deficit** in the six-year period, nearing a balanced trade position. This is a positive indicator of economic resilience and export competitiveness.

### 3. Connection to Other Indicators (from uploaded plots)

- **Economic Resilience:** The overall box plot for **Exports/Imports of goods and services** shows a wide interquartile range (IQR), indicating high variability in trade reliance across countries. India's trajectory shows it actively manages this critical balance.
- **Investment Context:** Given India's **strong positive percentage change in FDI** (seen in a prior bar chart), the narrowing trade deficit in 2018-2020, combined with sustained capital inflows, suggests a fundamental strengthening of its external sector.

---

Author & Contact
👨‍💻 Rahul Googikoll

Role: Data Analyst
Email: raulgoogikoll23@gmail.com
LinkedIn: https://www.linkedin.com/in/rahulgoogikoll
Portfolio: https://master--rahulgoogikolll2001.netlify.app/

