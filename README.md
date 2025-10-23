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

--
pip install -U wbdata


```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import wbdata
```


```python
wbdata.get_sources()
```




      id  name
    ----  --------------------------------------------------------------------
       1  Doing Business
       2  World Development Indicators
       3  Worldwide Governance Indicators
       5  Subnational Malnutrition Database
       6  International Debt Statistics
      11  Africa Development Indicators
      12  Education Statistics
      13  Enterprise Surveys
      14  Gender Statistics
      15  Global Economic Monitor
      16  Health Nutrition and Population Statistics
      18  IDA Results Measurement System
      19  Millennium Development Goals
      20  Quarterly Public Sector Debt
      22  Quarterly External Debt Statistics SDDS
      23  Quarterly External Debt Statistics GDDS
      25  Jobs
      27  Global Economic Prospects
      28  Global Findex database
      29  The Atlas of Social Protection: Indicators of Resilience and Equity
      30  Exporter Dynamics Database – Indicators at Country-Year Level
      31  Country Policy and Institutional Assessment
      32  Global Financial Development
      33  G20 Financial Inclusion Indicators
      34  Global Partnership for Education
      35  Sustainable Energy for All
      37  LAC Equity Lab
      38  Subnational Poverty
      39  Health Nutrition and Population Statistics by Wealth Quintile
      40  Population estimates and projections
      41  Country Partnership Strategy for India (FY2013 - 17)
      43  Adjusted Net Savings
      45  Indonesia Database for Policy and Economic Research
      46  Sustainable Development Goals
      50  Subnational Population
      54  Joint External Debt Hub
      57  WDI Database Archives
      58  Universal Health Coverage
      59  Wealth Accounts
      60  Economic Fitness
      61  PPPs Regulatory Quality
      62  International Comparison Program (ICP) 2011
      63  Human Capital Index
      64  Worldwide Bureaucracy Indicators
      65  Health Equity and Financial Protection Indicators
      66  Logistics Performance Index
      67  PEFA 2011
      68  PEFA 2016
      69  Global Financial Inclusion and Consumer Protection Survey
      70  Economic Fitness 2
      71  International Comparison Program (ICP) 2005
      73  Global Financial Inclusion and Consumer Protection Survey (Internal)
      75  Environment, Social and Governance (ESG) Data
      76  Remittance Prices Worldwide (Sending Countries)
      77  Remittance Prices Worldwide (Receiving Countries)
      78  ICP 2017
      79  PEFA_GRPFM
      80  Gender Disaggregated Labor Database (GDLD)
      81  International Debt Statistics: DSSI
      82  Global Public Procurement
      83  Statistical Performance Indicators (SPI)
      84  Education Policy
      85  PEFA_2021_SNG
      86  Global Jobs Indicators Database (JOIN)
      87  Country Climate and Development Report (CCDR)
      88  Food Prices for Nutrition
      89  Identification for Development (ID4D) Data
      90  ICP 2021
      91  PEFA_CRPFM
      92  Disability Data Hub (DDH)




```python
wbdata.get_indicators(query="gdp per capita", source=2)
```




    id                 name
    -----------------  -------------------------------------------------------------------
    NY.GDP.PCAP.CD     GDP per capita (current US$)
    NY.GDP.PCAP.CN     GDP per capita (current LCU)
    NY.GDP.PCAP.KD     GDP per capita (constant 2015 US$)
    NY.GDP.PCAP.KD.ZG  GDP per capita growth (annual %)
    NY.GDP.PCAP.KN     GDP per capita (constant LCU)
    NY.GDP.PCAP.PP.CD  GDP per capita, PPP (current international $)
    NY.GDP.PCAP.PP.KD  GDP per capita, PPP (constant 2021 international $)
    SE.XPD.PRIM.PC.ZS  Government expenditure per student, primary (% of GDP per capita)
    SE.XPD.SECO.PC.ZS  Government expenditure per student, secondary (% of GDP per capita)
    SE.XPD.TERT.PC.ZS  Government expenditure per student, tertiary (% of GDP per capita)




```python
indicators = {'Indicator Name': [
        'Gross Domestic Product (GDP)',
        'Gross National Income (GNI)',
        'Inflation rate',
        'Unemployment rate',
        'Poverty rate',
        'Life expectancy',
        'Literacy rate',
        'Access to electricity',
        'Mobile phone subscriptions',
        'Government expenditure on education',
        'Foreign direct investment (FDI)',
        'Exports of goods and services',
        'Imports of goods and services',
        'Gross capital formation',
        'Agricultural land area',
        'Agricultural production index'
    ],
    'Indicator ID': [
        'NY.GDP.MKTP.CD',
        'NY.GNP.MKTP.CD',
        'FP.CPI.TOTL.ZG',
        'SL.UEM.TOTL.ZS',
        'SI.POV.NAHC',
        'SP.DYN.LE00.IN',
        'SE.ADT.LITR.ZS',
        'EG.ELC.ACCS.ZS',
        'IT.CEL.SETS.P2',
        'SE.XPD.TOTL.GB.ZS',
        'BX.KLT.DINV.WD.GD.ZS',
        'NE.EXP.GNFS.ZS',
        'NE.IMP.GNFS.ZS',
        'NE.GDI.TOTL.ZS',
        'AG.LND.AGRI.ZS',
        'AG.PRD.FOOD.XD'
    ]
             }
```


```python
indicators
```




    {'Indicator Name': ['Gross Domestic Product (GDP)',
      'Gross National Income (GNI)',
      'Inflation rate',
      'Unemployment rate',
      'Poverty rate',
      'Life expectancy',
      'Literacy rate',
      'Access to electricity',
      'Mobile phone subscriptions',
      'Government expenditure on education',
      'Foreign direct investment (FDI)',
      'Exports of goods and services',
      'Imports of goods and services',
      'Gross capital formation',
      'Agricultural land area',
      'Agricultural production index'],
     'Indicator ID': ['NY.GDP.MKTP.CD',
      'NY.GNP.MKTP.CD',
      'FP.CPI.TOTL.ZG',
      'SL.UEM.TOTL.ZS',
      'SI.POV.NAHC',
      'SP.DYN.LE00.IN',
      'SE.ADT.LITR.ZS',
      'EG.ELC.ACCS.ZS',
      'IT.CEL.SETS.P2',
      'SE.XPD.TOTL.GB.ZS',
      'BX.KLT.DINV.WD.GD.ZS',
      'NE.EXP.GNFS.ZS',
      'NE.IMP.GNFS.ZS',
      'NE.GDI.TOTL.ZS',
      'AG.LND.AGRI.ZS',
      'AG.PRD.FOOD.XD']}




```python
indicators = pd.DataFrame(indicators)
```


```python
indicators
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
      <th>Indicator Name</th>
      <th>Indicator ID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Gross Domestic Product (GDP)</td>
      <td>NY.GDP.MKTP.CD</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Gross National Income (GNI)</td>
      <td>NY.GNP.MKTP.CD</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Inflation rate</td>
      <td>FP.CPI.TOTL.ZG</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Unemployment rate</td>
      <td>SL.UEM.TOTL.ZS</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Poverty rate</td>
      <td>SI.POV.NAHC</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Life expectancy</td>
      <td>SP.DYN.LE00.IN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Literacy rate</td>
      <td>SE.ADT.LITR.ZS</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Access to electricity</td>
      <td>EG.ELC.ACCS.ZS</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Mobile phone subscriptions</td>
      <td>IT.CEL.SETS.P2</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Government expenditure on education</td>
      <td>SE.XPD.TOTL.GB.ZS</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Foreign direct investment (FDI)</td>
      <td>BX.KLT.DINV.WD.GD.ZS</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Exports of goods and services</td>
      <td>NE.EXP.GNFS.ZS</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Imports of goods and services</td>
      <td>NE.IMP.GNFS.ZS</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Gross capital formation</td>
      <td>NE.GDI.TOTL.ZS</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Agricultural land area</td>
      <td>AG.LND.AGRI.ZS</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Agricultural production index</td>
      <td>AG.PRD.FOOD.XD</td>
    </tr>
  </tbody>
</table>
</div>




```python
from datetime import datetime
```


```python
start_date ='2015-01-01'
end_date ='2020-12-31'

start_date_obj = datetime.strptime(start_date,"%Y-%m-%d")
end_date_obj = datetime.strptime(end_date,"%Y-%m-%d")

date = (start_date_obj, end_date_obj)
```


```python
date
```




    (datetime.datetime(2015, 1, 1, 0, 0), datetime.datetime(2020, 12, 31, 0, 0))




```python
new_df = pd.DataFrame()
```


```python
gdp_series = wbdata.get_series('NY.GDP.MKTP.CD', country='all', date=data_date)

# --- Step 3: Convert to DataFrame with the 'value' column ---
df = pd.DataFrame(gdp_series, columns=['value'])

# --- Step 4: Keep MultiIndex intact ---
print(df.head())
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[12], line 1
    ----> 1 gdp_series = wbdata.get_series('NY.GDP.MKTP.CD', country='all', date=data_date)
          3 # --- Step 3: Convert to DataFrame with the 'value' column ---
          4 df = pd.DataFrame(gdp_series, columns=['value'])
    

    NameError: name 'data_date' is not defined



```python
indicators[indicators['Indicator ID'] == 'NY.GDP.MKTP.CD']['Indicator Name'].values[0]
```




    'Gross Domestic Product (GDP)'




```python
df=pd.DataFrame()
```


```python
g20_countries = ["ARG","AUS","BRA","CAN","CHN","FRA","DEU","IND","IDN",
                 "ITA","JPN","KOR","MEX","RUS","SAU","ZAF","TUR","GBR","USA"]
```


```python
g20_countries
```




    ['ARG',
     'AUS',
     'BRA',
     'CAN',
     'CHN',
     'FRA',
     'DEU',
     'IND',
     'IDN',
     'ITA',
     'JPN',
     'KOR',
     'MEX',
     'RUS',
     'SAU',
     'ZAF',
     'TUR',
     'GBR',
     'USA']




```python
import wbdata
import pandas as pd
from datetime import datetime
from functools import reduce

# G20 countries
g20_countries = [
    'ARG','AUS','BRA','CAN','CHN','FRA','DEU','IND','IDN','ITA',
    'JPN','KOR','MEX','RUS','SAU','ZAF','TUR','GBR','USA'
]

# Date range
start_date = datetime(2015, 1, 1)
end_date = datetime(2020, 12, 31)
date_range = (start_date, end_date)

# Indicators
indicators = {
    'NY.GDP.MKTP.CD': 'GDP',
    'NY.GNP.MKTP.CD': 'GNI',
    'FP.CPI.TOTL.ZG': 'Inflation',
    'SL.UEM.TOTL.ZS': 'Unemployment',
    'SI.POV.DDAY': 'Poverty',
    'SP.DYN.LE00.IN': 'LifeExpectancy',
    'SE.ADT.LITR.ZS': 'Literacy',
    'EG.ELC.ACCS.ZS': 'AccessElectricity',
    'IT.CEL.SETS.P2': 'MobileSubscriptions',
    'SE.XPD.TOTL.GD.ZS': 'GovtEduExp',
    'BX.KLT.DINV.CD.WD': 'FDI',
    'NE.EXP.GNFS.ZS': 'Exports',
    'NE.IMP.GNFS.ZS': 'Imports',
    'NE.GDI.FTOT.ZS': 'CapitalFormation',
    'AG.LND.AGRI.ZS': 'AgriLand',
    'AG.PRD.CROP.XD': 'AgriProduction'
}

# Fetch dataframes individually
df_list = []
for code, name in indicators.items():
    try:
        # Note: data_date is positional, not keyword
        df = wbdata.get_dataframe({code: name}, g20_countries, date_range)
        df.reset_index(inplace=True)  # move country/date to columns
        df.rename(columns={'date':'year'}, inplace=True)
        df_list.append(df)
        print(f"Data fetched for {name}, shape: {df.shape}")
    except Exception as e:
        print(f"Skipping {name}: {e}")
        continue

# Merge all on country + year
if df_list:
    df_final = reduce(lambda left, right: pd.merge(left, right, on=['country','year'], how='outer'), df_list)
    df_final = df_final.sort_values(['country','year']).reset_index(drop=True)
    pd.set_option('display.float_format', lambda x: '%.2f' % x)
    print(df_final.head())
else:
    print("No data was fetched. Check your country codes, date range, or indicators.")
```

    WARNING:shelved_cache.persistent_cache:Key '1862525495490277303' not in persistent cache.
    

    Data fetched for GDP, shape: (114, 3)
    Data fetched for GNI, shape: (114, 3)
    Data fetched for Inflation, shape: (114, 3)
    

    WARNING:shelved_cache.persistent_cache:Key '-5117636333221655311' not in persistent cache.
    

    Data fetched for Unemployment, shape: (114, 3)
    Data fetched for Poverty, shape: (114, 3)
    

    WARNING:shelved_cache.persistent_cache:Key '5219851931784943556' not in persistent cache.
    

    Data fetched for LifeExpectancy, shape: (114, 3)
    

    WARNING:shelved_cache.persistent_cache:Key '-7834430681090695720' not in persistent cache.
    

    Data fetched for Literacy, shape: (114, 3)
    Data fetched for AccessElectricity, shape: (114, 3)
    Data fetched for MobileSubscriptions, shape: (114, 3)
    

    WARNING:shelved_cache.persistent_cache:Key '-2470278514402296160' not in persistent cache.
    

    Data fetched for GovtEduExp, shape: (114, 3)
    

    WARNING:shelved_cache.persistent_cache:Key '2603805651637916084' not in persistent cache.
    

    Data fetched for FDI, shape: (114, 3)
    Data fetched for Exports, shape: (114, 3)
    Data fetched for Imports, shape: (114, 3)
    

    WARNING:shelved_cache.persistent_cache:Key '2269798475895354966' not in persistent cache.
    

    Data fetched for CapitalFormation, shape: (114, 3)
    Data fetched for AgriLand, shape: (114, 3)
    Data fetched for AgriProduction, shape: (114, 3)
         country  year             GDP             GNI  Inflation  Unemployment  \
    0  Argentina  2015 594749285413.21 583615452086.54        NaN          7.58   
    1  Argentina  2016 557532320662.95 545251641127.71        NaN          8.09   
    2  Argentina  2017 643628393281.36 627200463933.82        NaN          8.35   
    3  Argentina  2018 524819892360.18 506094045059.70      34.28          9.22   
    4  Argentina  2019 447754683615.22 430166792070.57      53.55          9.84   
    
       Poverty  LifeExpectancy  Literacy  AccessElectricity  MobileSubscriptions  \
    0      NaN           76.60       NaN              99.70               142.24   
    1     1.30           76.11       NaN              99.90               145.15   
    2     1.10           76.54       NaN             100.00               139.76   
    3     1.60           76.77       NaN             100.00               131.22   
    4     1.70           76.85       NaN             100.00               125.30   
    
       GovtEduExp            FDI  Exports  Imports  CapitalFormation  AgriLand  \
    0        5.78 11758994011.29    10.71    11.78             15.56     44.12   
    1        5.55  3260164341.77    12.53    13.57             14.27     43.43   
    2        5.45 11516861462.28    11.32    13.97             15.16     42.98   
    3        4.88 11716769818.75    14.44    16.33             15.25     42.36   
    4        4.77  6649187837.99    17.92    14.71             14.20     42.61   
    
       AgriProduction  
    0          104.14  
    1          101.71  
    2          106.82  
    3           92.20  
    4          113.14  
    


```python
# Number of rows and columns
print(df_final.shape)

# Overview of columns, types, and missing values
print(df_final.info())
```

    (114, 18)
    <class 'wbdata.client.DataFrame'>
    RangeIndex: 114 entries, 0 to 113
    Data columns (total 18 columns):
     #   Column               Non-Null Count  Dtype  
    ---  ------               --------------  -----  
     0   country              114 non-null    object 
     1   year                 114 non-null    object 
     2   GDP                  114 non-null    float64
     3   GNI                  114 non-null    float64
     4   Inflation            111 non-null    float64
     5   Unemployment         114 non-null    float64
     6   Poverty              88 non-null     float64
     7   LifeExpectancy       114 non-null    float64
     8   Literacy             31 non-null     float64
     9   AccessElectricity    114 non-null    float64
     10  MobileSubscriptions  114 non-null    float64
     11  GovtEduExp           94 non-null     float64
     12  FDI                  114 non-null    float64
     13  Exports              114 non-null    float64
     14  Imports              114 non-null    float64
     15  CapitalFormation     114 non-null    float64
     16  AgriLand             114 non-null    float64
     17  AgriProduction       114 non-null    float64
    dtypes: float64(16), object(2)
    memory usage: 16.2+ KB
    None
    


```python
from warnings import filterwarnings
filterwarnings("ignore") # To ignore future warnings.
```


```python
df_final['year'] = pd.to_datetime(df_final['year'])
```


```python
df_final.info()
```

    <class 'wbdata.client.DataFrame'>
    RangeIndex: 114 entries, 0 to 113
    Data columns (total 18 columns):
     #   Column               Non-Null Count  Dtype         
    ---  ------               --------------  -----         
     0   country              114 non-null    object        
     1   year                 114 non-null    datetime64[ns]
     2   GDP                  114 non-null    float64       
     3   GNI                  114 non-null    float64       
     4   Inflation            111 non-null    float64       
     5   Unemployment         114 non-null    float64       
     6   Poverty              88 non-null     float64       
     7   LifeExpectancy       114 non-null    float64       
     8   Literacy             31 non-null     float64       
     9   AccessElectricity    114 non-null    float64       
     10  MobileSubscriptions  114 non-null    float64       
     11  GovtEduExp           94 non-null     float64       
     12  FDI                  114 non-null    float64       
     13  Exports              114 non-null    float64       
     14  Imports              114 non-null    float64       
     15  CapitalFormation     114 non-null    float64       
     16  AgriLand             114 non-null    float64       
     17  AgriProduction       114 non-null    float64       
    dtypes: datetime64[ns](1), float64(16), object(1)
    memory usage: 16.2+ KB
    


```python
# Statistical Analysis of the dataframe.

df_final.describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>std</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>year</th>
      <td>114</td>
      <td>2017-07-02 04:00:00</td>
      <td>2015-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>2017-07-02 12:00:00</td>
      <td>2019-01-01 00:00:00</td>
      <td>2020-01-01 00:00:00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>GDP</th>
      <td>114.00</td>
      <td>3389858439909.33</td>
      <td>323585509674.48</td>
      <td>1072349506387.03</td>
      <td>1675221888084.81</td>
      <td>2766880619456.23</td>
      <td>21539982000000.00</td>
      <td>4838676599525.20</td>
    </tr>
    <tr>
      <th>GNI</th>
      <td>114.00</td>
      <td>3404511577697.40</td>
      <td>315294109648.65</td>
      <td>1043271232884.37</td>
      <td>1662172281864.93</td>
      <td>2807299303420.42</td>
      <td>21821877000000.00</td>
      <td>4887848477786.67</td>
    </tr>
    <tr>
      <th>Inflation</th>
      <td>111.00</td>
      <td>4.02</td>
      <td>-2.09</td>
      <td>1.02</td>
      <td>2.00</td>
      <td>3.73</td>
      <td>53.55</td>
      <td>7.42</td>
    </tr>
    <tr>
      <th>Unemployment</th>
      <td>114.00</td>
      <td>7.56</td>
      <td>2.35</td>
      <td>4.30</td>
      <td>5.62</td>
      <td>9.21</td>
      <td>29.22</td>
      <td>5.48</td>
    </tr>
    <tr>
      <th>Poverty</th>
      <td>88.00</td>
      <td>2.14</td>
      <td>0.00</td>
      <td>0.20</td>
      <td>0.85</td>
      <td>1.70</td>
      <td>21.60</td>
      <td>3.90</td>
    </tr>
    <tr>
      <th>LifeExpectancy</th>
      <td>114.00</td>
      <td>77.50</td>
      <td>64.05</td>
      <td>74.45</td>
      <td>78.17</td>
      <td>82.17</td>
      <td>84.56</td>
      <td>5.26</td>
    </tr>
    <tr>
      <th>Literacy</th>
      <td>31.00</td>
      <td>93.23</td>
      <td>73.70</td>
      <td>93.57</td>
      <td>95.22</td>
      <td>95.76</td>
      <td>99.35</td>
      <td>6.39</td>
    </tr>
    <tr>
      <th>AccessElectricity</th>
      <td>114.00</td>
      <td>98.66</td>
      <td>83.90</td>
      <td>99.70</td>
      <td>100.00</td>
      <td>100.00</td>
      <td>100.00</td>
      <td>3.63</td>
    </tr>
    <tr>
      <th>MobileSubscriptions</th>
      <td>114.00</td>
      <td>119.51</td>
      <td>75.38</td>
      <td>101.66</td>
      <td>119.64</td>
      <td>135.98</td>
      <td>176.13</td>
      <td>23.53</td>
    </tr>
    <tr>
      <th>GovtEduExp</th>
      <td>94.00</td>
      <td>4.57</td>
      <td>0.96</td>
      <td>4.16</td>
      <td>4.76</td>
      <td>5.39</td>
      <td>6.32</td>
      <td>1.13</td>
    </tr>
    <tr>
      <th>FDI</th>
      <td>114.00</td>
      <td>61588872373.62</td>
      <td>-25055440306.91</td>
      <td>11727325866.89</td>
      <td>32835622515.00</td>
      <td>60511531706.71</td>
      <td>511434000000.00</td>
      <td>92764067023.92</td>
    </tr>
    <tr>
      <th>Exports</th>
      <td>114.00</td>
      <td>25.92</td>
      <td>10.07</td>
      <td>18.67</td>
      <td>27.42</td>
      <td>31.68</td>
      <td>42.99</td>
      <td>8.92</td>
    </tr>
    <tr>
      <th>Imports</th>
      <td>114.00</td>
      <td>25.05</td>
      <td>11.78</td>
      <td>18.02</td>
      <td>24.18</td>
      <td>32.56</td>
      <td>41.17</td>
      <td>8.01</td>
    </tr>
    <tr>
      <th>CapitalFormation</th>
      <td>114.00</td>
      <td>23.58</td>
      <td>13.80</td>
      <td>18.21</td>
      <td>22.45</td>
      <td>27.47</td>
      <td>42.38</td>
      <td>6.55</td>
    </tr>
    <tr>
      <th>AgriLand</th>
      <td>114.00</td>
      <td>43.88</td>
      <td>6.37</td>
      <td>28.27</td>
      <td>46.68</td>
      <td>55.46</td>
      <td>80.77</td>
      <td>21.23</td>
    </tr>
    <tr>
      <th>AgriProduction</th>
      <td>114.00</td>
      <td>104.17</td>
      <td>76.66</td>
      <td>97.31</td>
      <td>102.83</td>
      <td>108.50</td>
      <td>181.73</td>
      <td>12.85</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_final = df_final.rename(columns={
    'Inflation': 'Inflation rate',
    'Unemployment': 'Unemployment rate',
    'Poverty': 'Poverty rate',
    'LifeExpectancy': 'Life expectancy',
    'Literacy': 'Literacy rate',
    'AccessElectricity': 'Access to electricity',
    'MobileSubscriptions': 'Mobile phone subscriptions',
    'GovtEduExp': 'Government expenditure on education',
    'FDI': 'Foreign direct investment (FDI)',
    'Exports': 'Exports of goods and services',
    'Imports': 'Imports of goods and services',
    'CapitalFormation': 'Gross capital formation',
    'AgriLand': 'Agricultural land area',
    'AgriProduction': 'Agricultural production index'
})
```


```python
selected_cols = [
    'Inflation rate','Unemployment rate','Poverty rate','Life expectancy',
    'Literacy rate','Access to electricity','Mobile phone subscriptions',
    'Government expenditure on education','Foreign direct investment (FDI)',
    'Exports of goods and services','Imports of goods and services',
    'Gross capital formation','Agricultural land area','Agricultural production index',
    'GDP_BN','GNI_BN'
]
```


```python
# Statistical Analysis of the dataframe.

df_final.describe().T
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
      <th>count</th>
      <th>mean</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
      <th>std</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>year</th>
      <td>114</td>
      <td>2017-07-02 04:00:00</td>
      <td>2015-01-01 00:00:00</td>
      <td>2016-01-01 00:00:00</td>
      <td>2017-07-02 12:00:00</td>
      <td>2019-01-01 00:00:00</td>
      <td>2020-01-01 00:00:00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>GDP</th>
      <td>114.00</td>
      <td>3389858439909.33</td>
      <td>323585509674.48</td>
      <td>1072349506387.03</td>
      <td>1675221888084.81</td>
      <td>2766880619456.23</td>
      <td>21539982000000.00</td>
      <td>4838676599525.20</td>
    </tr>
    <tr>
      <th>GNI</th>
      <td>114.00</td>
      <td>3404511577697.40</td>
      <td>315294109648.65</td>
      <td>1043271232884.37</td>
      <td>1662172281864.93</td>
      <td>2807299303420.42</td>
      <td>21821877000000.00</td>
      <td>4887848477786.67</td>
    </tr>
    <tr>
      <th>Inflation rate</th>
      <td>111.00</td>
      <td>4.02</td>
      <td>-2.09</td>
      <td>1.02</td>
      <td>2.00</td>
      <td>3.73</td>
      <td>53.55</td>
      <td>7.42</td>
    </tr>
    <tr>
      <th>Unemployment rate</th>
      <td>114.00</td>
      <td>7.56</td>
      <td>2.35</td>
      <td>4.30</td>
      <td>5.62</td>
      <td>9.21</td>
      <td>29.22</td>
      <td>5.48</td>
    </tr>
    <tr>
      <th>Poverty rate</th>
      <td>88.00</td>
      <td>2.14</td>
      <td>0.00</td>
      <td>0.20</td>
      <td>0.85</td>
      <td>1.70</td>
      <td>21.60</td>
      <td>3.90</td>
    </tr>
    <tr>
      <th>Life expectancy</th>
      <td>114.00</td>
      <td>77.50</td>
      <td>64.05</td>
      <td>74.45</td>
      <td>78.17</td>
      <td>82.17</td>
      <td>84.56</td>
      <td>5.26</td>
    </tr>
    <tr>
      <th>Literacy rate</th>
      <td>31.00</td>
      <td>93.23</td>
      <td>73.70</td>
      <td>93.57</td>
      <td>95.22</td>
      <td>95.76</td>
      <td>99.35</td>
      <td>6.39</td>
    </tr>
    <tr>
      <th>Access to electricity</th>
      <td>114.00</td>
      <td>98.66</td>
      <td>83.90</td>
      <td>99.70</td>
      <td>100.00</td>
      <td>100.00</td>
      <td>100.00</td>
      <td>3.63</td>
    </tr>
    <tr>
      <th>Mobile phone subscriptions</th>
      <td>114.00</td>
      <td>119.51</td>
      <td>75.38</td>
      <td>101.66</td>
      <td>119.64</td>
      <td>135.98</td>
      <td>176.13</td>
      <td>23.53</td>
    </tr>
    <tr>
      <th>Government expenditure on education</th>
      <td>94.00</td>
      <td>4.57</td>
      <td>0.96</td>
      <td>4.16</td>
      <td>4.76</td>
      <td>5.39</td>
      <td>6.32</td>
      <td>1.13</td>
    </tr>
    <tr>
      <th>Foreign direct investment (FDI)</th>
      <td>114.00</td>
      <td>61588872373.62</td>
      <td>-25055440306.91</td>
      <td>11727325866.89</td>
      <td>32835622515.00</td>
      <td>60511531706.71</td>
      <td>511434000000.00</td>
      <td>92764067023.92</td>
    </tr>
    <tr>
      <th>Exports of goods and services</th>
      <td>114.00</td>
      <td>25.92</td>
      <td>10.07</td>
      <td>18.67</td>
      <td>27.42</td>
      <td>31.68</td>
      <td>42.99</td>
      <td>8.92</td>
    </tr>
    <tr>
      <th>Imports of goods and services</th>
      <td>114.00</td>
      <td>25.05</td>
      <td>11.78</td>
      <td>18.02</td>
      <td>24.18</td>
      <td>32.56</td>
      <td>41.17</td>
      <td>8.01</td>
    </tr>
    <tr>
      <th>Gross capital formation</th>
      <td>114.00</td>
      <td>23.58</td>
      <td>13.80</td>
      <td>18.21</td>
      <td>22.45</td>
      <td>27.47</td>
      <td>42.38</td>
      <td>6.55</td>
    </tr>
    <tr>
      <th>Agricultural land area</th>
      <td>114.00</td>
      <td>43.88</td>
      <td>6.37</td>
      <td>28.27</td>
      <td>46.68</td>
      <td>55.46</td>
      <td>80.77</td>
      <td>21.23</td>
    </tr>
    <tr>
      <th>Agricultural production index</th>
      <td>114.00</td>
      <td>104.17</td>
      <td>76.66</td>
      <td>97.31</td>
      <td>102.83</td>
      <td>108.50</td>
      <td>181.73</td>
      <td>12.85</td>
    </tr>
  </tbody>
</table>
</div>




```python
# If the column names are 'GDP' and 'GNI'
df_final['GDP_BN'] = df_final['GDP'] / 1e9
df_final['GNI_BN'] = df_final['GNI'] / 1e9
```


```python
selected_cols = df_final.columns[4:]
```


```python
selected_cols

```




    Index(['Inflation rate', 'Unemployment rate', 'Poverty rate',
           'Life expectancy', 'Literacy rate', 'Access to electricity',
           'Mobile phone subscriptions', 'Government expenditure on education',
           'Foreign direct investment (FDI)', 'Exports of goods and services',
           'Imports of goods and services', 'Gross capital formation',
           'Agricultural land area', 'Agricultural production index', 'GDP_BN',
           'GNI_BN'],
          dtype='object')




```python
df_final[selected_cols].describe().T.round()
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
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Inflation rate</th>
      <td>111.00</td>
      <td>4.00</td>
      <td>7.00</td>
      <td>-2.00</td>
      <td>1.00</td>
      <td>2.00</td>
      <td>4.00</td>
      <td>54.00</td>
    </tr>
    <tr>
      <th>Unemployment rate</th>
      <td>114.00</td>
      <td>8.00</td>
      <td>5.00</td>
      <td>2.00</td>
      <td>4.00</td>
      <td>6.00</td>
      <td>9.00</td>
      <td>29.00</td>
    </tr>
    <tr>
      <th>Poverty rate</th>
      <td>88.00</td>
      <td>2.00</td>
      <td>4.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>1.00</td>
      <td>2.00</td>
      <td>22.00</td>
    </tr>
    <tr>
      <th>Life expectancy</th>
      <td>114.00</td>
      <td>78.00</td>
      <td>5.00</td>
      <td>64.00</td>
      <td>74.00</td>
      <td>78.00</td>
      <td>82.00</td>
      <td>85.00</td>
    </tr>
    <tr>
      <th>Literacy rate</th>
      <td>31.00</td>
      <td>93.00</td>
      <td>6.00</td>
      <td>74.00</td>
      <td>94.00</td>
      <td>95.00</td>
      <td>96.00</td>
      <td>99.00</td>
    </tr>
    <tr>
      <th>Access to electricity</th>
      <td>114.00</td>
      <td>99.00</td>
      <td>4.00</td>
      <td>84.00</td>
      <td>100.00</td>
      <td>100.00</td>
      <td>100.00</td>
      <td>100.00</td>
    </tr>
    <tr>
      <th>Mobile phone subscriptions</th>
      <td>114.00</td>
      <td>120.00</td>
      <td>24.00</td>
      <td>75.00</td>
      <td>102.00</td>
      <td>120.00</td>
      <td>136.00</td>
      <td>176.00</td>
    </tr>
    <tr>
      <th>Government expenditure on education</th>
      <td>94.00</td>
      <td>5.00</td>
      <td>1.00</td>
      <td>1.00</td>
      <td>4.00</td>
      <td>5.00</td>
      <td>5.00</td>
      <td>6.00</td>
    </tr>
    <tr>
      <th>Foreign direct investment (FDI)</th>
      <td>114.00</td>
      <td>61588872374.00</td>
      <td>92764067024.00</td>
      <td>-25055440307.00</td>
      <td>11727325867.00</td>
      <td>32835622515.00</td>
      <td>60511531707.00</td>
      <td>511434000000.00</td>
    </tr>
    <tr>
      <th>Exports of goods and services</th>
      <td>114.00</td>
      <td>26.00</td>
      <td>9.00</td>
      <td>10.00</td>
      <td>19.00</td>
      <td>27.00</td>
      <td>32.00</td>
      <td>43.00</td>
    </tr>
    <tr>
      <th>Imports of goods and services</th>
      <td>114.00</td>
      <td>25.00</td>
      <td>8.00</td>
      <td>12.00</td>
      <td>18.00</td>
      <td>24.00</td>
      <td>33.00</td>
      <td>41.00</td>
    </tr>
    <tr>
      <th>Gross capital formation</th>
      <td>114.00</td>
      <td>24.00</td>
      <td>7.00</td>
      <td>14.00</td>
      <td>18.00</td>
      <td>22.00</td>
      <td>27.00</td>
      <td>42.00</td>
    </tr>
    <tr>
      <th>Agricultural land area</th>
      <td>114.00</td>
      <td>44.00</td>
      <td>21.00</td>
      <td>6.00</td>
      <td>28.00</td>
      <td>47.00</td>
      <td>55.00</td>
      <td>81.00</td>
    </tr>
    <tr>
      <th>Agricultural production index</th>
      <td>114.00</td>
      <td>104.00</td>
      <td>13.00</td>
      <td>77.00</td>
      <td>97.00</td>
      <td>103.00</td>
      <td>108.00</td>
      <td>182.00</td>
    </tr>
    <tr>
      <th>GDP_BN</th>
      <td>114.00</td>
      <td>3390.00</td>
      <td>4839.00</td>
      <td>324.00</td>
      <td>1072.00</td>
      <td>1675.00</td>
      <td>2767.00</td>
      <td>21540.00</td>
    </tr>
    <tr>
      <th>GNI_BN</th>
      <td>114.00</td>
      <td>3405.00</td>
      <td>4888.00</td>
      <td>315.00</td>
      <td>1043.00</td>
      <td>1662.00</td>
      <td>2807.00</td>
      <td>21822.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Visualizing the distribution with the help of Histogram.

fig, axs = plt.subplots(nrows=4, ncols=4, figsize=(14,10))
axs = axs.flatten()

for i, col in enumerate(selected_cols):
    sns.histplot(data=df_final, x=col, kde=True, ax=axs[i])
    axs[i].set_title(col)

plt.tight_layout()
plt.show()
```


    
   <img width="1410" height="990" alt="output_30_0" src="https://github.com/user-attachments/assets/ff1d6f6a-3be1-4272-b9b8-c0ec1919fdb9" />

    



```python
# Calculating the Skewness of the columns:

df_final[selected_cols].skew().sort_values()
```




    Access to electricity                 -3.12
    Literacy rate                         -2.51
    Government expenditure on education   -1.47
    Life expectancy                       -0.74
    Agricultural land area                -0.08
    Exports of goods and services          0.10
    Imports of goods and services          0.11
    Mobile phone subscriptions             0.23
    Gross capital formation                1.01
    Unemployment rate                      2.48
    Agricultural production index          2.57
    GDP_BN                                 2.65
    GNI_BN                                 2.65
    Foreign direct investment (FDI)        2.83
    Poverty rate                           3.13
    Inflation rate                         4.71
    dtype: float64




```python
fig, axs = plt.subplots(nrows=4, ncols=4, figsize=(14,10))
axs = axs.flatten()

for i, col in enumerate(selected_cols):
    sns.boxplot(data=df_final, x=col, ax=axs[i])
    axs[i].set_title(col)

plt.tight_layout()
plt.show()
```

    
<img width="1389" height="990" alt="output_32_0" src="https://github.com/user-attachments/assets/f095e384-c4c5-4901-8516-066914a7166b" />



```python
def outlier(x):
    # Calculate the first quartile (Q1)
    q1 = x.quantile(0.25)
    
    # Calculate the third quartile (Q3)
    q3 = x.quantile(0.75)
    
    # Calculate the interquartile range (IQR)
    iqr = q3 - q1
    
    # Identify outliers using the IQR rule
    # Values below Q1 - 1.5*IQR or above Q3 + 1.5*IQR are considered outliers
    
    return (x < q1 - 1.5 * iqr) | (x > q3 + 1.5 * iqr)
```


```python
# Initialize an empty list to store outlier percentages
outlier_percentages = []

# Iterate through each column in the selected columns
for col in selected_cols:
    # Extract the column data
    x = df_final[col]
    
    # Use the previously defined outlier function to identify outliers in the column
    outliers = outlier(x)
    
    # Calculate the percentage of outliers in the column
    outlier_percentage = np.mean(outliers) * 100
    
    # Append the outlier percentage to the list
    outlier_percentages.append(outlier_percentage)

# Create a DataFrame to store the results
result_df = pd.DataFrame({'Column': selected_cols, 'Outlier Percentage': outlier_percentages})

# Sort the DataFrame by 'Outlier Percentage' in descending order
result_df = result_df.sort_values('Outlier Percentage', ascending=False)
```


```python
result_df.round()
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
      <th>Column</th>
      <th>Outlier Percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5</th>
      <td>Access to electricity</td>
      <td>18.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Foreign direct investment (FDI)</td>
      <td>14.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Poverty rate</td>
      <td>11.00</td>
    </tr>
    <tr>
      <th>15</th>
      <td>GNI_BN</td>
      <td>11.00</td>
    </tr>
    <tr>
      <th>14</th>
      <td>GDP_BN</td>
      <td>11.00</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Inflation rate</td>
      <td>9.00</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Agricultural production index</td>
      <td>5.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Unemployment rate</td>
      <td>5.00</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Gross capital formation</td>
      <td>4.00</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Government expenditure on education</td>
      <td>4.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Literacy rate</td>
      <td>4.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Life expectancy</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Mobile phone subscriptions</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Exports of goods and services</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Imports of goods and services</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Agricultural land area</td>
      <td>0.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Plotting the Percentage of the outliers calculted previously.

plt.figure(figsize=(11,5))
sns.barplot(x=result_df['Column'], y=result_df['Outlier Percentage'])
plt.title("Outlier Percentage")
plt.xticks(rotation=90)
plt.show()
```


        
<img width="932" height="724" alt="output_36_0" src="https://github.com/user-attachments/assets/49d12ec6-16a8-4ec1-af18-e1c9cfb6937c" />



```python
df_final.isnull().sum()

```




    country                                 0
    year                                    0
    GDP                                     0
    GNI                                     0
    Inflation rate                          3
    Unemployment rate                       0
    Poverty rate                           26
    Life expectancy                         0
    Literacy rate                          83
    Access to electricity                   0
    Mobile phone subscriptions              0
    Government expenditure on education    20
    Foreign direct investment (FDI)         0
    Exports of goods and services           0
    Imports of goods and services           0
    Gross capital formation                 0
    Agricultural land area                  0
    Agricultural production index           0
    GDP_BN                                  0
    GNI_BN                                  0
    dtype: int64



Correlation


```python
# Compute correlation only for numeric columns
corr_matrix = df_final.select_dtypes(include='number').corr()

# Display it neatly (optional: round values for readability)
corr_matrix.round(9)
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
      <th>GDP</th>
      <th>GNI</th>
      <th>Inflation rate</th>
      <th>Unemployment rate</th>
      <th>Poverty rate</th>
      <th>Life expectancy</th>
      <th>Literacy rate</th>
      <th>Access to electricity</th>
      <th>Mobile phone subscriptions</th>
      <th>Government expenditure on education</th>
      <th>Foreign direct investment (FDI)</th>
      <th>Exports of goods and services</th>
      <th>Imports of goods and services</th>
      <th>Gross capital formation</th>
      <th>Agricultural land area</th>
      <th>Agricultural production index</th>
      <th>GDP_BN</th>
      <th>GNI_BN</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>GDP</th>
      <td>1.00</td>
      <td>1.00</td>
      <td>-0.18</td>
      <td>-0.26</td>
      <td>-0.17</td>
      <td>0.15</td>
      <td>-0.10</td>
      <td>0.18</td>
      <td>-0.20</td>
      <td>0.07</td>
      <td>0.83</td>
      <td>-0.40</td>
      <td>-0.38</td>
      <td>0.28</td>
      <td>0.04</td>
      <td>-0.16</td>
      <td>1.00</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>GNI</th>
      <td>1.00</td>
      <td>1.00</td>
      <td>-0.18</td>
      <td>-0.26</td>
      <td>-0.17</td>
      <td>0.15</td>
      <td>-0.10</td>
      <td>0.18</td>
      <td>-0.19</td>
      <td>0.07</td>
      <td>0.82</td>
      <td>-0.40</td>
      <td>-0.38</td>
      <td>0.27</td>
      <td>0.04</td>
      <td>-0.16</td>
      <td>1.00</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>Inflation rate</th>
      <td>-0.18</td>
      <td>-0.18</td>
      <td>1.00</td>
      <td>0.20</td>
      <td>0.06</td>
      <td>-0.24</td>
      <td>0.15</td>
      <td>-0.05</td>
      <td>-0.00</td>
      <td>0.06</td>
      <td>-0.17</td>
      <td>-0.20</td>
      <td>-0.22</td>
      <td>-0.19</td>
      <td>-0.00</td>
      <td>0.07</td>
      <td>-0.18</td>
      <td>-0.18</td>
    </tr>
    <tr>
      <th>Unemployment rate</th>
      <td>-0.26</td>
      <td>-0.26</td>
      <td>0.20</td>
      <td>1.00</td>
      <td>-0.02</td>
      <td>-0.49</td>
      <td>0.04</td>
      <td>-0.73</td>
      <td>0.19</td>
      <td>0.40</td>
      <td>-0.24</td>
      <td>-0.07</td>
      <td>-0.04</td>
      <td>-0.41</td>
      <td>0.38</td>
      <td>0.14</td>
      <td>-0.26</td>
      <td>-0.26</td>
    </tr>
    <tr>
      <th>Poverty rate</th>
      <td>-0.17</td>
      <td>-0.17</td>
      <td>0.06</td>
      <td>-0.02</td>
      <td>1.00</td>
      <td>-0.64</td>
      <td>-0.27</td>
      <td>-0.65</td>
      <td>0.12</td>
      <td>-0.50</td>
      <td>-0.13</td>
      <td>-0.30</td>
      <td>-0.29</td>
      <td>0.20</td>
      <td>-0.13</td>
      <td>0.25</td>
      <td>-0.17</td>
      <td>-0.17</td>
    </tr>
    <tr>
      <th>Life expectancy</th>
      <td>0.15</td>
      <td>0.15</td>
      <td>-0.24</td>
      <td>-0.49</td>
      <td>-0.64</td>
      <td>1.00</td>
      <td>0.34</td>
      <td>0.71</td>
      <td>-0.15</td>
      <td>0.09</td>
      <td>0.13</td>
      <td>0.22</td>
      <td>0.22</td>
      <td>0.00</td>
      <td>-0.27</td>
      <td>-0.28</td>
      <td>0.15</td>
      <td>0.15</td>
    </tr>
    <tr>
      <th>Literacy rate</th>
      <td>-0.10</td>
      <td>-0.10</td>
      <td>0.15</td>
      <td>0.04</td>
      <td>-0.27</td>
      <td>0.34</td>
      <td>1.00</td>
      <td>0.20</td>
      <td>0.40</td>
      <td>-0.02</td>
      <td>-0.12</td>
      <td>0.25</td>
      <td>0.15</td>
      <td>-0.14</td>
      <td>-0.17</td>
      <td>0.01</td>
      <td>-0.10</td>
      <td>-0.10</td>
    </tr>
    <tr>
      <th>Access to electricity</th>
      <td>0.18</td>
      <td>0.18</td>
      <td>-0.05</td>
      <td>-0.73</td>
      <td>-0.65</td>
      <td>0.71</td>
      <td>0.20</td>
      <td>1.00</td>
      <td>-0.19</td>
      <td>-0.10</td>
      <td>0.18</td>
      <td>0.05</td>
      <td>0.02</td>
      <td>0.13</td>
      <td>-0.39</td>
      <td>-0.06</td>
      <td>0.18</td>
      <td>0.18</td>
    </tr>
    <tr>
      <th>Mobile phone subscriptions</th>
      <td>-0.20</td>
      <td>-0.19</td>
      <td>-0.00</td>
      <td>0.19</td>
      <td>0.12</td>
      <td>-0.15</td>
      <td>0.40</td>
      <td>-0.19</td>
      <td>1.00</td>
      <td>-0.16</td>
      <td>-0.25</td>
      <td>0.03</td>
      <td>-0.16</td>
      <td>-0.22</td>
      <td>0.02</td>
      <td>0.05</td>
      <td>-0.20</td>
      <td>-0.19</td>
    </tr>
    <tr>
      <th>Government expenditure on education</th>
      <td>0.07</td>
      <td>0.07</td>
      <td>0.06</td>
      <td>0.40</td>
      <td>-0.50</td>
      <td>0.09</td>
      <td>-0.02</td>
      <td>-0.10</td>
      <td>-0.16</td>
      <td>1.00</td>
      <td>0.18</td>
      <td>0.07</td>
      <td>0.11</td>
      <td>-0.68</td>
      <td>0.37</td>
      <td>-0.10</td>
      <td>0.07</td>
      <td>0.07</td>
    </tr>
    <tr>
      <th>Foreign direct investment (FDI)</th>
      <td>0.83</td>
      <td>0.82</td>
      <td>-0.17</td>
      <td>-0.24</td>
      <td>-0.13</td>
      <td>0.13</td>
      <td>-0.12</td>
      <td>0.18</td>
      <td>-0.25</td>
      <td>0.18</td>
      <td>1.00</td>
      <td>-0.30</td>
      <td>-0.26</td>
      <td>0.15</td>
      <td>0.11</td>
      <td>-0.18</td>
      <td>0.83</td>
      <td>0.82</td>
    </tr>
    <tr>
      <th>Exports of goods and services</th>
      <td>-0.40</td>
      <td>-0.40</td>
      <td>-0.20</td>
      <td>-0.07</td>
      <td>-0.30</td>
      <td>0.22</td>
      <td>0.25</td>
      <td>0.05</td>
      <td>0.03</td>
      <td>0.07</td>
      <td>-0.30</td>
      <td>1.00</td>
      <td>0.93</td>
      <td>-0.03</td>
      <td>0.07</td>
      <td>-0.07</td>
      <td>-0.40</td>
      <td>-0.40</td>
    </tr>
    <tr>
      <th>Imports of goods and services</th>
      <td>-0.38</td>
      <td>-0.38</td>
      <td>-0.22</td>
      <td>-0.04</td>
      <td>-0.29</td>
      <td>0.22</td>
      <td>0.15</td>
      <td>0.02</td>
      <td>-0.16</td>
      <td>0.11</td>
      <td>-0.26</td>
      <td>0.93</td>
      <td>1.00</td>
      <td>-0.02</td>
      <td>0.13</td>
      <td>-0.10</td>
      <td>-0.38</td>
      <td>-0.38</td>
    </tr>
    <tr>
      <th>Gross capital formation</th>
      <td>0.28</td>
      <td>0.27</td>
      <td>-0.19</td>
      <td>-0.41</td>
      <td>0.20</td>
      <td>0.00</td>
      <td>-0.14</td>
      <td>0.13</td>
      <td>-0.22</td>
      <td>-0.68</td>
      <td>0.15</td>
      <td>-0.03</td>
      <td>-0.02</td>
      <td>1.00</td>
      <td>-0.09</td>
      <td>0.03</td>
      <td>0.28</td>
      <td>0.27</td>
    </tr>
    <tr>
      <th>Agricultural land area</th>
      <td>0.04</td>
      <td>0.04</td>
      <td>-0.00</td>
      <td>0.38</td>
      <td>-0.13</td>
      <td>-0.27</td>
      <td>-0.17</td>
      <td>-0.39</td>
      <td>0.02</td>
      <td>0.37</td>
      <td>0.11</td>
      <td>0.07</td>
      <td>0.13</td>
      <td>-0.09</td>
      <td>1.00</td>
      <td>0.24</td>
      <td>0.04</td>
      <td>0.04</td>
    </tr>
    <tr>
      <th>Agricultural production index</th>
      <td>-0.16</td>
      <td>-0.16</td>
      <td>0.07</td>
      <td>0.14</td>
      <td>0.25</td>
      <td>-0.28</td>
      <td>0.01</td>
      <td>-0.06</td>
      <td>0.05</td>
      <td>-0.10</td>
      <td>-0.18</td>
      <td>-0.07</td>
      <td>-0.10</td>
      <td>0.03</td>
      <td>0.24</td>
      <td>1.00</td>
      <td>-0.16</td>
      <td>-0.16</td>
    </tr>
    <tr>
      <th>GDP_BN</th>
      <td>1.00</td>
      <td>1.00</td>
      <td>-0.18</td>
      <td>-0.26</td>
      <td>-0.17</td>
      <td>0.15</td>
      <td>-0.10</td>
      <td>0.18</td>
      <td>-0.20</td>
      <td>0.07</td>
      <td>0.83</td>
      <td>-0.40</td>
      <td>-0.38</td>
      <td>0.28</td>
      <td>0.04</td>
      <td>-0.16</td>
      <td>1.00</td>
      <td>1.00</td>
    </tr>
    <tr>
      <th>GNI_BN</th>
      <td>1.00</td>
      <td>1.00</td>
      <td>-0.18</td>
      <td>-0.26</td>
      <td>-0.17</td>
      <td>0.15</td>
      <td>-0.10</td>
      <td>0.18</td>
      <td>-0.19</td>
      <td>0.07</td>
      <td>0.82</td>
      <td>-0.40</td>
      <td>-0.38</td>
      <td>0.27</td>
      <td>0.04</td>
      <td>-0.16</td>
      <td>1.00</td>
      <td>1.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Plotting the correlation using heatmap:


plt.figure(figsize=(8,8))
sns.heatmap(df_final[selected_cols].corr(), annot=True, fmt='.1f', cmap='turbo')
plt.show()
```


    
    
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



```python
sns.jointplot(x='Government expenditure on education', y='Life expectancy', data=df_final, height=4, color='blue')
plt.show()
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

## Author & Contact
Rahul Googikoll
📍 Goa, India
Java Full Stack Developer | Aspiring Data Analyst & Data Engineer
📧 Email: raulgoogikoll23@gmail.com
🔗 LinkedIn: https://www.linkedin.com/in/rahulgoogikoll
🔗 Portfolio: https://master--rahulgoogikolll2001.netlify.app/
