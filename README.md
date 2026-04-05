# full-funnel-marketing-analytics
Full-funnel SaaS marketing analytics tracking  5 stages: Awareness → Consideration → Intent →  Conversion → Retention. Python + Power BI dashboard.  LTV:CAC of 87x | 4-week upper-funnel lag effect |  Churn sensitivity &amp; unit economics analysis.


# 📊 Full-Funnel Marketing Analytics
### Company A — SaaS Platform | End-to-End Customer Journey Analysis

---

## 🗂 Project Overview

This project demonstrates a complete **full-funnel marketing analytics framework** for Company A, a SaaS email marketing platform (similar to Constant Contact). The analysis tracks the entire customer journey — from first brand impression through to paid subscription and long-term retention — measuring how upper-funnel media investment drives lower-funnel revenue outcomes.

The project moves beyond single-channel, last-click attribution to provide a **holistic view of how media investment drives growth** across all five funnel stages — directly mirroring the measurement framework described in modern SaaS marketing analytics roles.

> **Note:** Company A is an anonymized SaaS client. All data is simulated to reflect realistic marketing dynamics including seasonality, adstock lag effects, churn behavior, and SaaS unit economics.

---

## 🎯 The Five Funnel Stages

```
AWARENESS          TV | YouTube | Podcast
      ↓            Impressions → Reach → Brand Lift → CPM
      ↓
CONSIDERATION      Paid Search | Social Media | Organic
      ↓            Website Visits → Bounce Rate → Time on Site → CPC
      ↓
INTENT             Email Marketing | Retargeting
      ↓            Trial Signups → Lead Score → Cost per Lead
      ↓
CONVERSION         Full Marketing Investment
      ↓            New Customers → Trial→Paid Rate → CAC → MRR
      ↓
RETENTION          Product & Customer Success
                   Active Customers → Churn → LTV → LTV:CAC → NPS
```

---

## 📦 Dataset Overview

| File | Key Metrics | Rows |
|---|---|---|
| `01_awareness_data.csv` | TV/YouTube/Podcast spend, Impressions, Reach, Brand Lift %, CPM | 104 |
| `02_consideration_data.csv` | Search/Social spend, Website visits, Bounce rate, Pages/session | 104 |
| `03_intent_data.csv` | Email spend, Trial signups, Trial rate %, Lead score, CPL | 104 |
| `04_conversion_data.csv` | New customers, Trial→Paid %, New MRR, CAC, ARPU | 104 |
| `05_retention_data.csv` | Active customers, Churn rate, LTV, LTV:CAC, Expansion MRR, NPS | 104 |
| `06_full_funnel_summary.csv` | All 5 stages combined — 40 metrics across 104 weeks | 104 |

---

## 🔍 Notebook 1 — EDA & Funnel Overview

**Key findings:**

| Stage | Avg Weekly Volume | Stage Conversion Rate |
|---|---|---|
| Awareness | 6,638,815 impressions | — |
| Consideration | 271,569 website visits | 4.09% |
| Intent | 33,685 trial signups | 12.40% |
| Conversion | 7,066 new customers | 20.98% |
| Retention | 397,483 active customers | 95.9% retained weekly |

**Media spend distribution:**

| Stage | Channels | Avg Weekly Spend | % of Total |
|---|---|---|---|
| Awareness | TV + YouTube + Podcast | $47,816 | 50.9% |
| Consideration | Search + Social | $38,021 | 40.5% |
| Intent | Email | $8,053 | 8.6% |

---

## 🔬 Notebook 2 — Stage-by-Stage Deep Dive

### Stage 1 — Awareness
<img width="1008" height="612" alt="image" src="https://github.com/user-attachments/assets/66501ed7-b0d2-461c-ac7c-e06e19820d8a" />


- Average brand lift: **25.0%** — strong awareness impact from TV and YouTube
- TV accounts for ~52% of awareness spend at $25K/week
- YouTube delivers best CPM efficiency among paid channels
- Clear seasonal peaks in Q1 and Q3 aligned with SaaS budget cycles

### Stage 2 — Consideration
- Average website visits: **271,569/week**
- Bounce rate: **50.3%** — primary opportunity for optimization
- Pages per session: **3.1** — engaged visitors once they land
- CPC remains stable — no significant media inflation

### Stage 3 — Intent
- Trial signup rate: **12.0%** of website visitors
- Average lead score: **67/100**
- Cost per lead: **$2.63** — highly efficient
- Email spend of $8K/week drives 33K+ trial signups

### Stage 4 — Conversion
- Trial → Paid conversion rate: **19.8%**
- Average new MRR per week: driven by 7K new customers at $51 ARPU
- CAC of $19 — exceptionally low for SaaS

### Stage 5 — Retention
- Average weekly churn rate: **4.1%** — below 5% warning threshold
- NPS average: **46** — above the 40 benchmark
- Active customer base growing consistently week over week

---

## 💰 Notebook 3 — LTV/CAC Analysis

### SaaS Unit Economics

| Metric | Value | Benchmark | Status |
|---|---|---|---|
| Avg CAC | $19 | < $500 | ✅ Excellent |
| Avg LTV | $1,120 | > $1,000 | ✅ Healthy |
| LTV:CAC Ratio | 87.4x | > 3x | ✅ Exceptional |
| CAC Payback Period | ~14 weeks | < 52 weeks | ✅ Excellent |
| Weekly Churn Rate | 4.1% | < 5% | ✅ Healthy |
| NPS | 46 | > 40 | ✅ Good |

### Churn Sensitivity Analysis
Reducing churn by just 1% increases LTV by approximately **$275 per customer** — making retention investment highly ROI-positive. At 7,000 new customers per week, a 1% churn reduction is worth ~$1.9M in additional LTV annually.

### Payback Period
At ~14 weeks payback, Company A recovers its CAC in under 4 months — well below the 12-month (52-week) industry warning threshold. This gives the business significant flexibility to invest aggressively in growth.

---

## 💡 Notebook 4 — Key Insights & Recommendations

### Insight 1 — Upper Funnel Drives Lower Funnel (4-Week Lag)

Brand lift today predicts trial signups **4 weeks later** (r=0.68). This confirms the adstock effect operates across funnel stages — awareness spend has a delayed but measurable causal impact on conversion downstream.

```
Week 1:  TV campaign runs → Brand lift +25%
Week 2:  Brand lift lingers (adstock decay)
Week 3:  Aided awareness drives search behavior
Week 4:  Trial signups increase +18% above baseline
```

> **Action:** Never cut awareness budget when trial signups dip — the effect takes 4-6 weeks to materialize. Budget awareness spend 4-6 weeks ahead of growth targets.

---

### Insight 2 — Consideration is the Biggest Bottleneck

**95.9% drop-off** at the Awareness→Consideration stage. While normal for impressions→visits, there is significant room to improve the visit→trial conversion from 12% toward industry-leading 15%+.

| If trial rate improves to | Additional weekly trials | Additional weekly customers |
|---|---|---|
| 13% (+1pp) | +2,716 | +538 |
| 15% (+3pp) | +8,147 | +1,613 |
| 18% (+6pp) | +16,294 | +3,226 |

> **Action:** Invest in landing page optimization, SEO improvements, and retargeting to convert more website visitors into trial signups.

---

### Insight 3 — Unit Economics Are Exceptional

LTV:CAC of **87.4x** significantly exceeds the 3x minimum and 5x good thresholds. The business is in a very strong financial position.

> **Action:** Invest aggressively in growth — the unit economics easily justify increased spend across all funnel stages. Primary focus should be reducing churn from 4.1% to below 3% to further improve LTV and margin.

---

### Insight 4 — Seasonality Requires Proactive Budgeting

Q1 (Jan-Mar) and Q3 (Jul-Sep) show the strongest new customer acquisition, aligned with small business budget planning cycles — the core Constant Contact customer base.

> **Action:** Front-load awareness spend in December/January and June/July to capture peak demand windows. Reduce brand spend in Q4 when churn risk peaks and reallocate to retention initiatives.

---

### Priority Action Plan

| Priority | Action | Expected Impact |
|---|---|---|
| 1 | Maintain awareness spend — 4-6 week lag | Sustained trial pipeline |
| 2 | Optimize landing pages — target 15% trial rate | +8K trials/week |
| 3 | Reduce churn below 3% | +$275 LTV per customer |
| 4 | Front-load Q1 and Q3 budgets | Capture peak demand |
| 5 | Expand personalization across all touchpoints | Lift across all stages |

---

## 📊 Power BI Dashboard

### 5 Dashboard Pages

**Page 1 — Executive Overview**
<img width="1422" height="795" alt="image" src="https://github.com/user-attachments/assets/f7825210-910f-417c-91a5-fe1f626c877c" />

- Full funnel volume KPI cards
- Stage-to-stage conversion rates
- Spend distribution by funnel stage
- Total MRR growth trend

**Page 2 — Awareness**
<img width="1439" height="803" alt="image" src="https://github.com/user-attachments/assets/9676f4b4-9fbc-4cff-b89a-5ffd785c8373" />

- Brand lift % trend
- Weekly impressions over time
- Spend by channel (TV/YouTube/Podcast)
- Awareness spend vs brand lift scatter

**Page 3 — Consideration & Intent**
<img width="1412" height="801" alt="image" src="https://github.com/user-attachments/assets/5e875adf-388e-4738-af67-c96b6d1ecc42" />

- Website visits trend
- Bounce rate with 50% warning line
- Trial signups trend
- Channel spend breakdown

**Page 4 — Conversion & Retention**
<img width="1430" height="799" alt="image" src="https://github.com/user-attachments/assets/6e6d03c7-daac-47aa-b57e-49c54eb6415c" />

- New customers and MRR growth
- Trial→Paid conversion rate
- Churn rate with 5% warning line
- Active customer base growth

**Page 5 — SaaS Health Metrics**
<img width="1430" height="791" alt="image" src="https://github.com/user-attachments/assets/e2fe5121-cb62-47c1-9f3e-be1b77a36392" />

- LTV:CAC gauge (87x vs 3x benchmark)
- CAC payback period trend
- SaaS health benchmarks table
- NPS vs churn scatter

---

## 🛠 Tech Stack

| Tool | Purpose |
|---|---|
| Python | Primary analysis language |
| pandas / numpy | Data manipulation and simulation |
| matplotlib / seaborn | Data visualization |
| scipy | Statistical analysis and correlation |
| Power BI Desktop | Interactive 5-page dashboard |
| DAX | Custom measures and calculations |

---

## 🚀 How to Run

1. Clone the repository
2. Install Python dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy
```
3. Upload CSV files to Google Colab or Jupyter
4. Run notebooks in order:
```
01_data_loading_eda.ipynb
02_funnel_analysis.ipynb
03_ltv_cac_analysis.ipynb
04_insights_recommendations.ipynb
```
5. Open Power BI Desktop
6. Load all 4 files from `powerbi_data/` folder
7. Build dashboard following page structure above

---

## 🔗 Related Projects

This project is part of a complete marketing analytics portfolio:

👉 [Marketing Mix Modeling with Robyn](https://github.com/azar2020/marketing-mix-modeling-robyn) — MMM, Incrementality Testing, Geo-Lift

👉 [Marketing Performance Dashboard](https://github.com/azar2020/marketing-dashboard-powerbi) — Power BI, DAX, Channel ROAS

👉 [Email A/B Testing Analysis](https://github.com/azar2020/email-ab-testing-analysis) — Z-Test, T-Test, Bayesian Testing

---

## 👤 Author

**Azar Taheri**
 
[LinkedIn](https://linkedin.com/in/azar-taheri)  
