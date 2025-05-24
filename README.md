# 🇮🇳 Lok Sabha Election Analytics (2014 & 2019)

## 📌 Project Overview
This project explores structured datasets of India's 2014 and 2019 general elections to uncover key electoral insights, focusing on voter turnout, party-wise performance, vote share trends, and constituency-level dynamics. The goal was to derive data-driven political intelligence from large-scale electoral data using SQL.

## 🧠 Problem Statement
> How did party performance, voter behavior, and turnout evolve between the 2014 and 2019 Indian general elections?  
> Can we identify which parties gained ground, where voter turnout increased, and which constituencies were most contested?

---

## 🎯 Business Objectives
- Track party performance at national and state levels.
- Evaluate changes in voter turnout across constituencies.
- Identify winning margins and closely contested seats.
- Compute party-wise vote share and trends across elections.

---

## 🧭 Data Understanding

### 🗂 Datasets Used
- `candidate_details.csv`: Candidate names, gender, party, and constituency.
- `election_results_2014.csv` & `election_results_2019.csv`: Vote counts, ranks, and outcomes per candidate.
- `constituency_details.csv`: Metadata for constituencies including state association and voter counts.

### 🧩 Key Fields
- `party`, `constituency`, `state`
- `total_votes`, `total_electors`, `voter_turnout_ratio`
- `rank` (to identify winners vs runners-up)

---

## 🔄 Workflow Breakdown

### 1. **Data Profiling**
- Audited both election datasets to confirm schema consistency across years.
- Validated row counts and uniqueness of key fields (e.g., constituency-year pairs).
- Checked for nulls or inconsistent values in rank, vote counts, or party codes.

### 2. **Data Mapping**
- Linked candidate-level data with constituency metadata for both years.
- Mapped vote totals with elector base to compute turnout and compare against official rates.

### 3. **Party-Wise Performance**
- Counted number of seats won per party in both years.
- Calculated gains/losses between 2014 and 2019 for each party.
- Highlighted top-performing parties and emerging regional parties.

### 4. **Voter Turnout Analysis**
- Analyzed changes in turnout percentage at national, state, and constituency levels.
- Flagged constituencies with the highest and lowest voter engagement.
- Derived delta in turnout across years to capture shifting electoral behavior.

### 5. **Vote Margin Insights**
- For each constituency, computed difference in votes between winner and runner-up.
- Identified "swing seats" with narrow victory margins.
- Segmented constituencies based on margin ranges (e.g., <1%, 1–5%, 5–10%).

### 6. **Vote Share Calculation**
- Computed vote share per party within each constituency.
- Aggregated party-wise vote share across all seats and per state.
- Compared vote share vs seat share to identify disproportionality.

---

## 📊 Key Findings

- **BJP** expanded its seat share significantly in some states while declining in others, reflecting **regional volatility**.
- **Voter turnout increased** nationally in 2019, with notable spikes in urban constituencies.
- Multiple constituencies had **margins below 2%**, indicating high electoral competitiveness.
- Vote share analysis revealed cases where parties had **high vote shares but fewer seats**, suggesting **first-past-the-post limitations**.

---

## ✅ Outcomes & Learnings

| Area | Outcome |
|------|---------|
| Electoral Trends | Uncovered high-level shifts in political momentum between elections. |
| Data Strategy | Reinforced importance of schema validation and consistent aggregation. |
| Analytical Rigor | Focused on clean joins, filtered rankings, and normalized metrics. |
| Communication | Delivered election insights in stakeholder-ready format for reports/dashboards. |

---

## 🧰 Tools & Stack
- **SQL (PostgreSQL)** for querying and analytics.
- **Excel** for final validation and summaries.
- **GitHub** for version control and documentation.

---

## 📁 Folder Structure (Recommended)
election-analytics/
│
├── data/
│ ├── raw/ # Source CSV files
│ └── processed/ # Cleaned or merged datasets
│
├── outputs/
│ ├── charts/ # Optional visual summaries
│ └── summary_tables/ # Excel files or .csv with final tables
│
├── notebooks/ # Optional Jupyter or SQL notebooks
│
└── README.md # Documentation (this file)
