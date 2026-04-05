# Decoding Steam: A Strategic Data Audit of 6.4M Reviews
**Advanced Python Analytics | Big Data Pipeline & Market Intelligence**

---

## 🚀 Overview
[cite_start]This project performs a comprehensive strategic audit of a massive dataset containing **6,417,106 user reviews** from the Steam platform[cite: 171]. [cite_start]The primary objective is to extract high-level business intelligence, establish player engagement metrics, and quantify market concentration [cite: 3-5]. By decoding millions of data points, this analysis identifies the "Quality Floor" for titles, measures brand hazard through controversy modeling, and explores consumer psychology within the gaming ecosystem.

---

## 🛠 Tech Stack & Configuration
* [cite_start]**Core Libraries:** **Pandas** for high-volume data engineering, **NumPy** for mathematical modeling, and **Scipy** for correlation analysis[cite: 6, 9].
* [cite_start]**Visualization:** **Seaborn** and **Matplotlib** for strategic matrices and distribution plots [cite: 7-8].
* [cite_start]**Infrastructure:** Custom axis formatters designed for professional business reporting (M/K scale) and optimized memory management for multi-million row processing [cite: 16-18].

---

## 📊 Project Phases & Technical Implementation

### Phase 1: Data Ingestion & Professional Quality Audit
* [cite_start]**Bulk Loading:** Processed 6.4 million records from raw CSV into a structured analytical environment [cite: 21-22].
* [cite_start]**Integrity Screening:** Performed a deep-clean by analyzing null counts and zero-value distributions across numerical columns [cite: 30-39].
* [cite_start]**Automated Sanitization:** Identified and removed **183,234 invalid rows** missing essential metadata to ensure statistical validity[cite: 41, 184].

### Phase 2: Strategic Business Analysis
* [cite_start]**Market Concentration (Pareto):** Executed a cumulative distribution analysis to test the 80/20 rule [cite: 61-63, 208].
* [cite_start]**Controversy Modeling:** Engineered the **Polarization Index** ($|approval\_rate - 50|$) to identify "Brand Hazards" [cite: 77-78].
* [cite_start]**Success Penalty Analysis:** Analyzed satisfaction trends across market tiers—from Indie (<1K reviews) to Major titles (>10K reviews) [cite: 108-111].

---

## 💻 Technical Logic & Strategic Summary
*The following block contains the core pipeline and a technical summary of findings:*

```python
# --- 1. DATA PIPELINE ---
import pandas as pd
df = pd.read_csv("dataset.csv") 

# Cleaning 183K rows with missing data for statistical integrity [cite: 41, 184]
df_clean = df.dropna(subset=['app_name', 'review_score', 'review_votes']).copy()

# --- 2. ANALYTICAL LOGIC ---
# Pareto Analysis: Top 5% of games capture 80% of reviews 
pareto_df['cum_perc'] = 100 * (pareto_df['total_reviews'].cumsum() / pareto_df['total_reviews'].sum())

# --- STRATEGIC INSIGHTS & MARKET REALITIES ---
# QUALITY FLOOR: Baseline 84.1%. 70% is failure. Aim for 85%+ [cite: 59, 194-197].
# WINNER-TAKES-ALL: Top 5% games capture 80% reviews. UA required [cite: 72, 216-218].
# LOSS AVERSION: Negative reviews are 2x more visible. QA is key [cite: 106, 288-290].
# SUCCESS PENALTY: 2-4% satisfaction drop when scaling to 'Major' [cite: 120, 312-314].
# OPINION MONOPOLY: Top 1% control 35.1% of helpful votes .

# --- CONTACT INFO ---
# NAME: Asaf Chechik | ROLE: Analyst 
# LINKEDIN: [https://www.linkedin.com/in/asaf-chechik-737a62204/](https://www.linkedin.com/in/asaf-chechik-737a62204/)
# EMAIL: Asafchechik9@gmail.com
