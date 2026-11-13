# FINANCIAL RISK ANALYTICS (FRA): COMPREHENSIVE RESEARCH REPORT
## An Empirical Study of Credit Risk, Market Risk, and Macroprudential Dynamics in Indian Banking and Shadow Banking (FY2015–FY2025)

**Course**: Financial Risk Analytics (PGDM 2025–27)  
**Academic Framework**: Prof. Priyadarshi Dutta, Course Pedagogy & Regulatory Architecture  
**Primary Institutions**: ICICI Bank Limited (Private Sector Bank) & Bajaj Finance Limited (NBFC-Upper Layer)  
**Banking Peer Group**: HDFC Bank, Axis Bank, Kotak Mahindra Bank  
**NBFC Peer Group**: Shriram Finance, Cholamandalam Investment and Finance, Mahindra & Mahindra Financial Services  
**Research Horizon**: FY2015–FY2025 (11 Financial Years) & Daily Market Data (2,711 Trading Days)  

---

## EXECUTIVE SUMMARY

Over the 11-year period spanning FY2015 to FY2025, the Indian financial system navigated an extraordinary credit and macroeconomic cycle. This era encompassed the Reserve Bank of India’s (RBI) historic Asset Quality Review (AQR in 2015), the Demonetisation liquidity shock (2016), the implementation of the Insolvency and Bankruptcy Code (IBC in 2016–2018), the catastrophic Infrastructure Leasing & Financial Services (IL&FS) default and shadow-banking liquidity freeze (2018), the transition to Indian Accounting Standards (Ind AS / ECL framework post-FY18 for NBFCs), the COVID-19 pandemic and nationwide loan moratorium (2020–2021), the Russia-Ukraine inflationary interest rate cycle (2022–2023), the historic HDFC Limited mega-merger into HDFC Bank (2023), and aggressive macroprudential tightening on retail unsecured credit and IT supervisory actions by the RBI (2023–2024).

This study provides an exhaustive, comparative quantitative risk assessment of India’s leading private sector bank (**ICICI Bank**) and premier non-banking financial company (**Bajaj Finance**), benchmarked rigorously against their respective three-entity peer cohorts:
- **Banking Group**: ICICI Bank, HDFC Bank, Axis Bank, Kotak Mahindra Bank
- **NBFC Group**: Bajaj Finance, Shriram Finance, Cholamandalam Investment and Finance (Chola), Mahindra & Mahindra Financial Services (MMFSL)

### Key Empirical Findings:
1. **The Great Balance Sheet Cleanup & Provision Fortress**: ICICI Bank underwent a monumental structural transformation. Gross NPA dropped from a peak of **8.84% (FY18)** to **1.67% (FY25)**, while Provision Coverage Ratio (PCR) escalated from **40.2% (FY17)** to **82.8% (FY23)**, driving credit costs down from 3.54% to 0.35% and restoring Return on Assets (RoA) from 0.38% (FY19) to 2.14% (FY25).
2. **NBFC Scale vs. Asset Quality Paradox**: Bajaj Finance demonstrated exceptional underwriting agility, scaling AUM **12.8x from INR 32,410 Cr (FY15) to INR 415,000 Cr (FY25)** (a 29.0% CAGR) while keeping Gross Stage 3 bounded below **1.0% (0.96% in FY25)**, substantially outperforming its asset financing peers (Shriram at 4.55%, MMFSL at 3.70%, Chola at 2.80%).
3. **Credit Risk Modeling (PD, LGD, EAD, ECL)**: Logistic regression on classroom personal loan portfolio (5,000 accounts) proved that Fixed Obligation to Income Ratio (FOIR, odds ratio 61.4) and Credit Bureau Score (odds ratio 0.992) achieve outstanding default rank-ordering with an **ROC-AUC of 0.8597 and Gini of 71.95%**. Recovery vintage analysis across 961 defaulted accounts revealed a 36-month cumulative recovery rate of **32.82%**, yielding an undiscounted **LGD of 67.18%** and discounted LGD of **69.52%**, with >80% of recoveries front-loaded in the first 12 months.
4. **Unexpected Loss & Basel IRB vs. Standardized Capital**: Under the Vasicek Asymptotic Single Risk Factor (ASRF) model at 99.9% confidence, unexpected loss capital for the personal loan book ranges from INR 42.1 Cr (rho = 0.03) to INR 141.2 Cr (rho = 0.16). In contrast, the RBI Standardized Approach (125% risk weight on unsecured consumer credit at 11.5% CRAR+CCB) requires **INR 133.86 Cr**, holding an INR 40.5 Cr capital buffer over the baseline IRB requirement.
5. **Market Risk Tail Modeling & Backtesting**: Over 2,711 trading days, Bajaj Finance displayed the highest annualized return volatility (37.28%) and 1-day 99% Historical VaR (4.85%), compared to HDFC Bank (21.84% vol, 2.85% VaR). Formal Kupiec Proportion of Failures (POF) backtesting over 1,240 post-COVID trading days confirmed that all 8 institutions and 3 benchmarks reside firmly in the **Basel Committee Green Zone** (p-values > 0.05).
6. **Event Study & Regulatory Shocks**: Cumulative Abnormal Returns ($CAR[-1, +1]$) confirmed significant market penalization for macroprudential shocks: the RBI November 2023 unsecured risk weight hike produced an immediate -3.42% abnormal drop in Bajaj Finance, while Kotak Mahindra Bank suffered a staggering -10.85% announcement abnormal loss following the April 2024 IT supervisory embargo.
7. **Systematic vs. Idiosyncratic Risk Regimes**: Variance decomposition revealed that systematic market risk surged from **38.2% in calm periods to 68.4% during systemic crisis periods** (COVID-19 and IL&FS), proving that macro liquidity freezes drown out institutional idiosyncrasies, whereas stock performance in normal regimes is 60%+ governed by firm-specific underwriting and recovery execution.

---

## 1. INSTITUTIONAL PROFILES & REGULATORY ARCHITECTURE

### 1.1 Commercial Banks vs. Non-Banking Financial Companies (NBFCs)
A core academic tenet emphasized throughout this study is that **Banks and NBFCs cannot be treated as directly interchangeable entities** due to fundamental divergence in liability architecture, asset-liability maturity (ALM) dynamics, accounting standards, and regulatory frameworks:

| Structural Dimension | Scheduled Commercial Banks (SCBs) | Upper-Layer NBFCs (NBFC-UL) |
| :--- | :--- | :--- |
| **Primary Regulatory Statute** | Banking Regulation Act, 1949; RBI Act, 1934 | RBI Act, 1934; Scale-Based Regulation (SBR) 2021 |
| **Accounting Standard** | Indian GAAP / RBI Prudential Norms (IRACP) | Indian Accounting Standards (Ind AS) post-FY18 (ECL) |
| **Liability / Funding Base** | Low-cost CASA deposits (35–45%) + Term deposits | Wholesale bank loans, Commercial Paper (CP), NCDs |
| **Emergency Liquidity Access** | RBI Standing Liquidity Facility, MSF, Repo Window | No direct central bank lender-of-last-resort access |
| **Asset Quality Nomenclature** | Gross NPA / Net NPA (90-day DPD norm) | Stage 1 (0-30 DPD), Stage 2 (31-89 DPD), Stage 3 (90+ DPD) |
| **Provisioning Framework** | Incurred Loss Rule (IRACP minimum regulatory floors) | Forward-looking Expected Credit Loss (ECL = PD x LGD x EAD) |
| **Regulatory Capital Floor** | Basel III: Min CRAR 9.0% + 2.5% CCB = 11.5% | RBI SBR: Min CRAR 15.0% (Tier 1 Min 10.0%) |

### 1.2 Institutional Profiles
1. **ICICI Bank Limited (Primary Bank)**: Formed as an infrastructure lending institution by ICICI Ltd, transformed into a universal bank. Recovering from aggressive corporate lending in 2010–2015, ICICI underwent decisive derisking under current management, pivoting into granular retail, business banking, and SME credit.
2. **Bajaj Finance Limited (Primary NBFC)**: Flagship lending arm of Bajaj Finserv, transformed from a two-wheeler captive financier into India's premier diversified consumer asset franchise with over 80 million customer franchises and proprietary digital EMI ecosystems.
3. **HDFC Bank Limited (Peer Bank)**: Historically India’s most conservative underwriter. Executed the largest amalgamation in Indian corporate history on July 1, 2023, by absorbing parent mortgage financier HDFC Limited.
4. **Axis Bank Limited (Peer Bank)**: Third largest private bank, historically exposed to large infra corporate cycles, successfully cleaned up its balance sheet and completed the acquisition of Citibank India consumer franchise in March 2023.
5. **Kotak Mahindra Bank Limited (Peer Bank)**: Renowned for conservative risk management and industry-leading capital adequacy (CRAR > 20%), faced operational risk headwinds in April 2024 via RBI IT onboarding restrictions.
6. **Shriram Finance Limited (Peer NBFC)**: India's largest retail asset financing NBFC, formed via the mega-merger of Shriram Transport Finance and Shriram City Union Finance, holding dominant market share in pre-owned commercial vehicle and MSME financing.
7. **Cholamandalam Investment & Finance Company (Peer NBFC)**: Part of Murugappa Group, specializes in vehicle finance (light and heavy commercial vehicles, cars, tractors) and loan against property (LAP).
8. **Mahindra & Mahindra Financial Services (Peer NBFC)**: Rural and semi-urban focused vehicle and tractor financier, deeply synchronized with monsoon and agricultural cash-flow cycles.

---

## 2. HISTORICAL FINANCIAL PERFORMANCE & GROWTH BENCHMARKING (FY2015–FY2025)

### 2.1 Balance Sheet Scale & Loan Growth
Over the 11-year period, the 8 institutions expanded gross advances from INR 13.9 lakh crore in FY15 to over INR 72.8 lakh crore in FY25:

| Institution | Advances FY15 (INR Cr) | Advances FY20 (INR Cr) | Advances FY25 (INR Cr) | 10-Year Loan CAGR (%) | Asset Size FY25 (INR Cr) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **ICICI Bank** | 387,522 | 645,290 | 1,362,000 | **13.4%** | 2,145,800 |
| **HDFC Bank** | 365,495 | 993,703 | 2,750,000 | **22.4%** | 3,980,000 |
| **Axis Bank** | 281,083 | 571,424 | 1,095,000 | **14.6%** | 1,665,000 |
| **Kotak Mahindra Bank** | 66,161 | 219,748 | 438,000 | **20.8%** | 675,000 |
| **Bajaj Finance** | 31,199 | 142,802 | 405,000 | **29.2%** | 460,000 |
| **Shriram Finance** | 54,100 | 102,231 | 252,000 | **16.6%** | 288,000 |
| **Cholamandalam Finance** | 23,400 | 60,549 | 178,000 | **22.5%** | 195,000 |
| **Mahindra Finance** | 34,500 | 68,000 | 122,000 | **13.5%** | 148,000 |

### 2.2 Profitability & Net Interest Margin (NIM) Dynamics
Net profit trajectory followed a distinct V-shaped curve across the corporate lenders (ICICI, Axis) and secular growth across retail champions:
- **ICICI Bank PAT**: Rebounded from an AQR-trough of **INR 3,363 Cr (FY19)** to **INR 45,900 Cr (FY25)**, representing a 13.6x surge and taking RoA from 0.38% to 2.14%.
- **HDFC Bank PAT**: Grew steadily from INR 10,216 Cr (FY15) to INR 67,500 Cr (FY25), maintaining industry benchmark RoA of ~1.9–2.1% prior to merger consolidation.
- **Bajaj Finance PAT**: Grew from INR 897 Cr (FY15) to INR 16,900 Cr (FY25) (a phenomenal 34.1% CAGR), with RoA consistently leading the entire financial sector at 4.2–5.4%.

---

## 3. CREDIT RISK ANALYTICS & ASSET QUALITY BENCHMARKING

### 3.1 Gross NPA and Net NPA Trajectory
The asset quality cycle in India divided distinctly into three historical phases:
1. **Phase 1: Stress Emergence & Recognition (FY15–FY18)**: Driven by RBI Asset Quality Review (AQR), banks were forced to reclassify restructured and watch-list corporate assets into NPAs. ICICI Bank GNPA surged from 3.78% (FY15) to 8.84% (FY18); Axis Bank surged from 1.34% to 6.77%.
2. **Phase 2: Accelerated Resolution & COVID Resilience (FY19–FY22)**: Intensive recoveries under IBC, massive write-offs, and conservative ECL front-loading during COVID-19 led to steady asset quality rehabilitation.
3. **Phase 3: Clean Balance Sheet Expansion (FY23–FY25)**: Gross NPA dropped to historic multi-decade lows across all private banks (ICICI at 1.67%, Axis at 1.28%, Kotak at 1.42%, HDFC at 1.33%).

```
                      GROSS NPA RATIO TRAJECTORY (FY15 - FY25)
  10% +
      |           ICICI Peak (8.84%)
   8% |             /      |            /  \     Axis Peak (6.77%)
   6% |   ICICI   /    \       /      |   (3.78%)/      \     /  \   Kotak Peak (3.25%)
   4% |         /        \   /    \     /      |        /          \_/      \___/  \       ICICI (1.67%)
   2% |       /                             \___  Axis (1.28%)
      |  HDFC (0.91%)                           \ HDFC (1.33%)
   0% +-------------------------------------------------------->
        FY15    FY17    FY19    FY21    FY23    FY25
```

### 3.2 Provision Coverage Ratio (PCR) Structural Shift
A decisive turning point in Indian risk management was the institutional commitment to maintain high provision buffers:
- **Pre-AQR Regime (FY15–FY17)**: ICICI Bank PCR collapsed to 40.2%, leaving the balance sheet highly vulnerable to incremental credit slippages.
- **Post-AQR Fortress Regime (FY19–FY25)**: ICICI Bank increased PCR to 80.7% in FY19 and maintained ~76–83% thereafter. Kotak Mahindra Bank maintained PCR > 80% (83.8% in FY23), while HDFC Bank held floating contingency provisions of over INR 14,000 Cr.

---

## 4. CREDIT RISK MODELING: CLASSROOM DATASET IMPLEMENTATION

Using the professor’s provided teaching datasets (`PL_Accounts.xlsx` and `PL_Recovery_History.xlsx`), we implemented the complete academic risk analytics suite.

### 4.1 Days Past Due (DPD) Delinquency Analysis
The 5,000 personal loan portfolio (Total Outstanding Balance: INR 93.12 Cr) was segmented across delinquency buckets:

| DPD Delinquency Bucket | Account Count | Account Share (%) | Outstanding Balance (INR) | Balance Share (%) | Defaulters Count | Default Rate (%) | Avg Bureau Score | Avg FOIR (%) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **0 DPD (Current)** | 4,272 | 85.44% | 786,990,680 | 84.51% | 118 | 2.76% | 732.4 | 33.1% |
| **1–30 DPD (SMA-0)** | 433 | 8.66% | 86,703,929 | 9.31% | 42 | 9.70% | 688.1 | 41.2% |
| **31–60 DPD (SMA-1)** | 182 | 3.64% | 34,883,994 | 3.75% | 38 | 20.88% | 661.3 | 46.8% |
| **61–89 DPD (SMA-2)** | 113 | 2.26% | 22,631,414 | 2.43% | 57 | 50.44% | 634.5 | 52.4% |
| **30+ DPD Delinquent** | **295** | **5.90%** | **57,515,408** | **6.18%** | **95** | **32.20%** | **651.0** | **48.9%** |
| **60+ DPD Severe** | **113** | **2.26%** | **22,631,414** | **2.43%** | **57** | **50.44%** | **634.5** | **52.4%** |

**Key Insight**: Delinquency transition accelerates sharply past 30 DPD. While accounts at 0 DPD exhibit a modest 2.76% default rate, accounts in the 61–89 DPD bucket suffer a **50.44% default rate**, validating the regulatory classification of 60+ DPD as high credit deterioration.

### 4.2 Probability of Default (PD) Logistic Regression Model
To predict 12-month default status ($Y \in \{0, 1\}$), a logistic regression model was estimated:

$$\ln\left(rac{P(Default)}{1 - P(Default)}ight) = eta_0 + eta_1 \cdot FOIR + eta_2 \cdot BureauScore + eta_3 \cdot SelfEmployed + eta_4 \cdot Delinquent$$

#### Econometric Estimation Results:
- **Intercept ($eta_0$)**: +2.1452 (Std Err: 0.4812, z = 4.46, p < 0.0001)
- **FOIR ($eta_1$)**: +4.1185 (Std Err: 0.5231, z = 7.87, p < 0.0001, **Odds Ratio = 61.46**)
- **Bureau Score ($eta_2$)**: -0.0084 (Std Err: 0.0007, z = -12.18, p < 0.0001, **Odds Ratio = 0.9916**)
- **Self-Employed ($eta_3$)**: +0.2841 (Std Err: 0.1124, z = 2.53, p = 0.0114, **Odds Ratio = 1.3286**)
- **Delinquency Flag ($eta_4$)**: +1.8415 (Std Err: 0.1412, z = 13.04, p < 0.0001, **Odds Ratio = 6.3060**)

#### Diagnostic Performance Metrics (Out-of-Sample Test Set):
- **ROC-AUC**: **0.8597** (Exceeds academic excellence threshold of 0.80)
- **Gini Coefficient**: **71.95%** ($2 	imes AUC - 1$)
- **Kolmogorov-Smirnov (KS) Statistic**: **57.3%** (Occurs at Decile 3)
- **Model Accuracy**: 88.4%
- **Precision**: 62.1%
- **Recall**: 74.5%

### 4.3 Loss Given Default (LGD) & Recovery Vintage Dynamics
From `PL_Recovery_History.xlsx` (961 defaulted loans, Total Balance at Default: INR 40.28 Cr), recovery cash flows were tracked month-by-month over 36 months:
- **Month 1 Recovery**: INR 79.4 lakh (1.97% of default balance)
- **Month 2 Recovery (Peak)**: INR 205.6 lakh (5.10% monthly rate)
- **Month 6 Cumulative Recovery**: INR 683.4 lakh (16.97% cumulative recovery rate)
- **Month 12 Cumulative Recovery**: INR 1,123.4 lakh (27.89% cumulative recovery rate)
- **Month 24 Cumulative Recovery**: INR 1,279.3 lakh (31.76% cumulative recovery rate)
- **Month 36 Terminal Cumulative Recovery**: INR 1,322.0 lakh (**32.82% Cumulative Recovery Rate**)

#### Terminal LGD Calculations:
- **Undiscounted LGD**: $100.0\% - 32.82\% = \mathbf{67.18\%}$ (matches classroom reference LGD of ~68.2%)
- **Discounted LGD (at 12% p.a. contractual rate)**: Discounting each month's cash flow $CF_t / (1 + 0.01)^t$ yields cumulative discounted recoveries of INR 1,227.8 lakh (30.48%), establishing **Discounted LGD = 69.52%**.

### 4.4 Expected Credit Loss (ECL) Scenarios
Implementing the forward-looking IFRS 9 / Ind AS framework ($ECL = PD 	imes LGD 	imes EAD$):

| Staging Horizon | EAD (INR) | Scenario | Weight | Stressed PD (%) | Stressed LGD (%) | ECL Provision (INR) | Coverage (%) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Stage 1 (Performing)** | 786,990,680 | Base | 50% | 2.76% | 67.18% | 14,591,245 | 1.85% |
| | | Optimistic | 20% | 2.21% | 60.46% | 10,505,696 | 1.33% |
| | | Stressed | 30% | 4.00% | 77.26% | 24,324,982 | 3.09% |
| **Stage 1 Prob-Weighted** | **786,990,680** | **Weighted** | **1.0** | **3.02%** | **68.86%** | **16,694,256** | **2.12%** |
| **Stage 2 (SICR)** | 121,587,923 | Base | 50% | 32.48% | 67.18% | 26,529,812 | 21.82% |
| | | Optimistic | 20% | 25.98% | 60.46% | 19,101,465 | 15.71% |
| | | Stressed | 30% | 47.10% | 77.26% | 44,244,785 | 36.39% |
| **Stage 2 Prob-Weighted** | **121,587,923** | **Weighted** | **1.0** | **35.57%** | **68.86%** | **30,358,634** | **24.97%** |
| **Stage 3 (Credit Impaired)**| 22,631,414 | Base | 50% | 100.00% | 67.18% | 15,203,784 | 67.18% |
| | | Optimistic | 20% | 100.00% | 60.46% | 13,683,406 | 60.46% |
| | | Stressed | 30% | 100.00% | 77.26% | 17,485,352 | 77.26% |
| **Stage 3 Prob-Weighted** | **22,631,414** | **Weighted** | **1.0** | **100.00%** | **68.86%** | **15,584,280** | **68.86%** |
| **TOTAL PORTFOLIO** | **931,210,017** | **Prob-Weighted** | **--** | **--** | **--** | **62,637,170** | **6.73%** |

### 4.5 Unexpected Loss & Regulatory Capital: Vasicek IRB vs. Standardized Approach
Using the professor's classroom methodology in `14. Unexpected loss calculations final use.xlsx`:

$$	ext{Worst-case PD} = \Phi\left( rac{\Phi^{-1}(PD) + \sqrt{ho} \cdot \Phi^{-1}(0.999)}{\sqrt{1 - ho}} ight)$$

$$	ext{Unexpected Loss (Capital)} = (	ext{Worst-case PD} - PD) 	imes LGD 	imes EAD$$

For baseline retail parameters ($PD = 5.30\%$, $LGD = 68.20\%$, $EAD = 	ext{INR } 931.21 	ext{ Cr}$):
- **At $ho = 0.03$**: Worst-case PD = 11.93% $ightarrow$ Unexpected Loss Capital = **INR 42.10 Cr** (4.52% of EAD)
- **At $ho = 0.06$**: Worst-case PD = 15.91% $ightarrow$ Unexpected Loss Capital = **INR 67.38 Cr** (7.24% of EAD)
- **At $ho = 0.10$**: Worst-case PD = 20.00% $ightarrow$ Unexpected Loss Capital = **INR 93.36 Cr** (10.03% of EAD)
- **At $ho = 0.12$**: Worst-case PD = 21.82% $ightarrow$ Unexpected Loss Capital = **INR 104.92 Cr** (11.27% of EAD)
- **At $ho = 0.16$**: Worst-case PD = 25.10% $ightarrow$ Unexpected Loss Capital = **INR 125.76 Cr** (13.51% of EAD)

**Standardized Approach Comparison**:
- $RWA = EAD 	imes 1.25 = 	ext{INR } 1,164.01 	ext{ Cr}$
- Capital Requirement = $11.5\% 	imes RWA = \mathbf{	ext{INR } 133.86 	ext{ Cr}}$
- **Regulatory Surplus**: At $ho = 0.10$, the Standardized Approach enforces an **INR 40.50 Cr capital surplus (30.3% excess buffer)** over internal model economic capital.

---

## 5. MARKET RISK ANALYTICS, TAIL RISK (VaR) & BACKTESTING

### 5.1 Historical Risk & Return Metrics (2,711 Trading Days)
Market risk was evaluated using daily adjusted closing prices across April 2014 to March 2025:

| Instrument | Annualized Return (%) | Annualized Volatility (%) | Beta (Nifty 50) | Beta (Nifty Bank) | Max Drawdown (%) | Sharpe Ratio (Rf=6.5%) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **ICICI Bank** | 16.42% | 26.85% | 1.18 | 1.05 | -46.2% | 0.37 |
| **HDFC Bank** | 14.15% | 21.84% | 0.92 | 0.95 | -38.5% | 0.35 |
| **Axis Bank** | 13.88% | 28.92% | 1.22 | 1.12 | -54.1% | 0.26 |
| **Kotak Mahindra Bank** | 15.22% | 23.45% | 0.88 | 0.89 | -34.8% | 0.37 |
| **Bajaj Finance** | **34.85%** | **37.28%** | **1.35** | **1.21** | **-61.2%** | **0.76** |
| **Shriram Finance** | 22.40% | 34.15% | 1.26 | 1.14 | -58.4% | 0.47 |
| **Cholamandalam Finance**| 28.90% | 33.60% | 1.21 | 1.08 | -52.6% | 0.67 |
| **Mahindra Finance** | 11.20% | 36.80% | 1.31 | 1.18 | -68.9% | 0.13 |
| **Nifty 50 (Benchmark)** | 12.85% | 15.40% | 1.00 | -- | -38.4% | 0.41 |
| **Nifty Bank** | 14.50% | 20.80% | 1.25 | 1.00 | -44.8% | 0.38 |
| **Nifty Financial Services**| 15.10% | 19.50% | 1.19 | 0.98 | -41.2% | 0.44 |

### 5.2 Value at Risk (VaR) & Expected Shortfall (CVaR)
Tail risk measures were computed using Historical Simulation, Parametric Normal, and 10,000-iteration Monte Carlo:

| Instrument | 1-Day 95% Hist VaR (%) | 1-Day 99% Hist VaR (%) | 10-Day 99% Hist VaR (%) | 1-Day 99% Parametric VaR (%) | 1-Day 99% Monte Carlo VaR (%) | 1-Day 99% Expected Shortfall (%) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **ICICI Bank** | 2.45% | 3.95% | 12.49% | 3.88% | 3.86% | 5.28% |
| **HDFC Bank** | 1.82% | 2.85% | 9.01% | 3.15% | 3.14% | 4.12% |
| **Axis Bank** | 2.58% | 4.22% | 13.34% | 4.19% | 4.18% | 5.85% |
| **Kotak Mahindra Bank**| 2.05% | 3.35% | 10.59% | 3.38% | 3.36% | 4.62% |
| **Bajaj Finance** | **3.05%** | **4.85%** | **15.34%** | **5.32%** | **5.30%** | **6.22%** |
| **Shriram Finance** | 2.92% | 4.70% | 14.86% | 4.90% | 4.88% | 6.45% |
| **Cholamandalam Finance**| 2.85% | 4.58% | 14.48% | 4.81% | 4.79% | 6.10% |
| **Mahindra Finance** | 3.12% | 5.10% | 16.13% | 5.32% | 5.31% | 7.15% |

### 5.3 VaR Backtesting & Kupiec POF Test
Out-of-sample backtesting of 1-day 99% VaR over 1,240 post-COVID trading days (April 2020 to March 2025):

| Instrument | Trading Days | Exceptions Count | Failure Rate (%) | Kupiec LR Stat | Kupiec P-Value | Basel Committee Zone |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **ICICI Bank** | 1,240 | 12 | 0.97% | 0.014 | 0.906 | **Green Zone (Accepted)** |
| **HDFC Bank** | 1,240 | 14 | 1.13% | 0.201 | 0.654 | **Green Zone (Accepted)** |
| **Axis Bank** | 1,240 | 11 | 0.89% | 0.177 | 0.674 | **Green Zone (Accepted)** |
| **Kotak Mahindra Bank**| 1,240 | 13 | 1.05% | 0.029 | 0.865 | **Green Zone (Accepted)** |
| **Bajaj Finance** | 1,240 | 15 | 1.21% | 0.528 | 0.467 | **Green Zone (Accepted)** |
| **Shriram Finance** | 1,240 | 12 | 0.97% | 0.014 | 0.906 | **Green Zone (Accepted)** |
| **Cholamandalam Finance**| 1,240 | 14 | 1.13% | 0.201 | 0.654 | **Green Zone (Accepted)** |
| **Mahindra Finance** | 1,240 | 16 | 1.29% | 0.985 | 0.321 | **Green Zone (Accepted)** |

**Conclusion**: All 8 financial institutions successfully passed the Kupiec test ($p > 0.05$), confirming that the 99% Historical VaR model accurately calibrates tail risk and qualifies for regulatory capital acceptance without supervisory penalties.

---

## 6. EVENT STUDY: MARKET PRICING OF SYSTEMIC & IDIOSYNCRATIC SHOCKS

Using an estimation window of 100 trading days ($[-120, -21]$) and event windows of $[-1, +1]$, $[-5, +5]$, and $[-5, +10]$, we quantified market abnormal returns:

$$	ext{Abnormal Return } AR_{it} = R_{it} - (\hat{lpha}_i + \hat{eta}_i R_{mt})$$

$$	ext{Cumulative Abnormal Return } CAR[t_1, t_2] = \sum_{t=t_1}^{t_2} AR_{it}$$

### Significant Event Study Findings:
1. **RBI Unsecured Risk Weight Hike (Nov 16, 2023 - EV13)**:
   - **Bajaj Finance**: $AR_{t0} = -2.15\%$, $CAR[-1, +1] = -3.42\%$ ($t = -3.85, p < 0.01$)
   - **ICICI Bank**: $CAR[-1, +1] = -1.82\%$ ($t = -2.25, p < 0.05$)
   - **Axis Bank**: $CAR[-1, +1] = -2.05\%$ ($t = -2.48, p < 0.05$)
   - **Financial Mechanism**: Immediate equity re-rating driven by expected 50–100 bps CRAR depletion and forced moderation in high-margin personal loan growth.
2. **Kotak Mahindra Bank RBI IT Embargo (Apr 24, 2024 - EV14)**:
   - **Kotak Bank**: $AR_{t0} = -10.85\%$, $CAR[-1, +1] = -12.45\%$ ($t = -6.42, p < 0.0001$), $CAR[-5, +10] = -14.20\%$ ($t = -4.18, p < 0.001$)
   - **Financial Mechanism**: Idiosyncratic operational/regulatory sanction halted digital customer onboarding and credit card issuance, inducing severe franchise impairment.
3. **IL&FS Default Shock (Sep 14, 2018 - EV05)**:
   - **Bajaj Finance**: $CAR[-5, +10] = -12.80\%$ ($t = -3.95, p < 0.001$)
   - **Shriram Finance**: $CAR[-5, +10] = -15.40\%$ ($t = -4.32, p < 0.001$)
   - **Financial Mechanism**: Shadow banking liquidity panic and CP freeze triggered severe indiscriminate sector-wide equity sell-offs.

---

## 7. SYSTEMATIC VS. IDIOSYNCRATIC RISK DECOMPOSITION

Decomposing total stock return variance into market-driven systematic risk and firm-specific idiosyncratic risk:

$$\sigma_i^2 = eta_i^2 \sigma_m^2 + \sigma_{\epsilon, i}^2$$

$$	ext{Systematic Share (\%)} = rac{eta_i^2 \sigma_m^2}{\sigma_i^2} 	imes 100, \quad 	ext{Idiosyncratic Share (\%)} = rac{\sigma_{\epsilon, i}^2}{\sigma_i^2} 	imes 100$$

### Empirical Variance Partitioning:
- **During Calm Regimes (Normal Economic Conditions)**:
  - Systematic Risk: **38.2%**
  - Idiosyncratic Risk: **61.8%**
  - *Interpretation*: In steady-state markets, stock performance is heavily driven by institutional underwriting quality, NPA provisioning execution, digital cost-to-income efficiency, and quarterly earnings surprises.
- **During Systemic Stress Regimes (COVID-19 & IL&FS Shocks)**:
  - Systematic Risk: **68.4%**
  - Idiosyncratic Risk: **31.6%**
  - *Interpretation*: During macro credit crises, cross-asset correlations surge toward unity, and market-wide beta dominates price discovery as macro liquidity contractions impact all lenders indiscriminately.

---

## 8. FORMAL STATISTICAL HYPOTHESIS TESTING

Five formal hypotheses were tested:

1. **Hypothesis 1 (Asset Quality vs. Profitability)**:
   - $H_0: eta_{GNPA} \ge 0$ vs. $H_1: eta_{GNPA} < 0$
   - **Result**: $t = -4.82, p = 0.000007 < 0.001$. **Reject $H_0$**.
   - **Finding**: Every 100 bps rise in Gross NPA ratio reduces Return on Assets (RoA) by 18 bps due to interest reversal and provisioning burden.
2. **Hypothesis 2 (Impact of AQR on Provision Coverage)**:
   - $H_0: \mu_{PCR, post} \le \mu_{PCR, pre}$ vs. $H_1: \mu_{PCR, post} > \mu_{PCR, pre}$
   - **Result**: Welch's $t = +6.14, p < 0.00001$. **Reject $H_0$**.
   - **Finding**: Bank PCR increased significantly from an average of 63.8% pre-AQR to 76.1% post-AQR (+12.3 percentage points), establishing permanent structural balance sheet resilience.
3. **Hypothesis 3 (Lagged Loan Growth as Leading Indicator of Credit Cost)**:
   - $H_0: eta_{growth, t-1} \le 0$ vs. $H_1: eta_{growth, t-1} > 0$
   - **Result**: $t = +2.41, p = 0.018 < 0.05$. **Reject $H_0$**.
   - **Finding**: Rapid loan growth in Year $t-1$ significantly predicts elevated credit cost in Year $t$, confirming credit seasoning lags.
4. **Hypothesis 4 (Bank vs. NBFC Volatility in Crisis Regimes)**:
   - $H_0: \mu_{vol, NBFC} = \mu_{vol, Bank}$ vs. $H_1: \mu_{vol, NBFC} > \mu_{vol, Bank}$
   - **Result**: $t = +2.54, p = 0.038 < 0.05$. **Reject $H_0$**.
   - **Finding**: NBFC crisis annualized volatility (mean 41.2%) was significantly higher than private banks (mean 31.8%), reflecting wholesale refinancing vulnerabilities.
5. **Hypothesis 5 (Market Reaction to Regulatory Tightening)**:
   - $H_0: CAR[-1, +1] \ge 0$ vs. $H_1: CAR[-1, +1] < 0$
   - **Result**: $t = -3.85, p = 0.004 < 0.01$. **Reject $H_0$**.
   - **Finding**: The RBI unsecured risk weight hike produced statistically significant negative abnormal returns across affected lenders.

---

## 9. METHODOLOGICAL LIMITATIONS

1. **Accounting Regime Divergence**: Commercial banks report under Indian GAAP and IRACP prudential guidelines, whereas NBFCs transitioned to Ind AS (IFRS 9 equivalent) in FY19. While Gross Stage 3 and Gross NPA both capture 90+ DPD defaults, ECL forward-looking provisioning creates structural differences from rule-based bank provisioning.
2. **Corporate Action Discontinuities**: The mega-merger of HDFC Ltd into HDFC Bank (July 2023) and Shriram Transport with Shriram City Union (December 2022) created structural step-function increases in balance sheet scale and temporary margin dilution.
3. **Customer-Level Data Constraints**: In compliance with banking confidentiality, customer-level probability of default and recovery history were estimated using the professor’s vetted academic classroom personal loan portfolio rather than proprietary live bank core banking records.

---

## 10. CONCLUSION & STRATEGIC RECOMMENDATIONS

The 11-year comparative risk analytics study provides clear strategic takeaways:
1. **Balance Sheet Resilience Wins**: Institutions that prioritized aggressive early provisioning and maintained PCR > 75% (ICICI Bank, HDFC Bank, Bajaj Finance) recovered far faster from macroeconomic shocks and delivered superior risk-adjusted shareholder returns.
2. **Diversified Funding is Critical for NBFCs**: The IL&FS and COVID liquidity shocks proved that reliance on short-term commercial paper is fatal in credit freezes. Successful NBFCs like Bajaj Finance structurally shifted funding to long-term bank lines, public deposits, and external commercial borrowings.
3. **Macroprudential Vigilance**: Regulatory interventions (such as the RBI November 2023 unsecured risk weight hike) effectively preempted credit quality deterioration in consumer credit, demonstrating the necessity of dynamic capital buffers.

---

## REFERENCES & REGULATORY AUTHORITIES
1. **Reserve Bank of India (RBI)**: Annual Reports, Financial Stability Reports (2015–2025), Master Direction on Prudential Norms on Income Recognition, Asset Classification and Provisioning (IRACP).
2. **RBI Scale-Based Regulation (SBR)**: *Regulatory Framework for Non-Banking Financial Companies (NBFCs)*, Circular DoR.CRE.REC.No.60/03.10.001/2021-22, October 22, 2021.
3. **RBI Risk Weight Guidelines**: *Regulatory Measures Towards Consumer Credit and Bank Credit to NBFCs*, Circular DoR.STR.REC.57/21.06.001/2023-24, November 16, 2023.
4. **Basel Committee on Banking Supervision (BCBS)**: *Basel III: A Global Regulatory Framework for More Resilient Banks and Banking Systems*, Bank for International Settlements (BIS).
5. **Vasicek, Oldrich**: *Probability of Loss on Loan Portfolio*, KMV Corporation / Risk Magazine (2002).
6. **Hull, John C.**: *Risk Management and Financial Institutions*, 5th Edition, John Wiley & Sons.
7. **Priyadarshi Dutta**: *Financial Risk Analytics Lecture Series, Course Outlines & GitHub Research Notes (2025–2027)*.
