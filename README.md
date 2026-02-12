# Revenue Intelligence & Leakage Detection Engine

## 📌 Problem Framing

Modern sales teams generate large volumes of deal data, but most organizations lack a structured way to identify:

- Which sales reps truly drive lift
- Where revenue leakage occurs in the pipeline
- Which lead sources underperform expectations
- How much revenue is being left on the table

The objective of this project is to build a **decision-support engine** that identifies performance gaps and quantifies revenue improvement opportunities.

Rather than just reporting win rates, this solution translates performance differences into **estimated revenue impact**, enabling actionable business decisions.

---

# 🧠 Approach

The solution was built in four layers:

## 1️⃣ Aggregation Layer
Grouped deal-level data into:

- Sales Rep level
- Deal Stage level
- Lead Source level

Metrics computed:
- Total Deals
- Win Rate
- Average Deal Size
- Total Revenue
- Revenue per Deal

---

## 2️⃣ Global Benchmark

A global win rate was calculated across the full dataset and used as a performance baseline.

Lift was computed as:

Lift = Entity Win Rate – Global Win Rate

This standardizes comparisons across reps, stages, and channels.

---

## 3️⃣ Revenue Leakage Estimation

To translate performance gaps into business impact:

Revenue Gap Estimate =
(Global Win Rate – Entity Win Rate)  
× Number of Deals  
× Average Deal Size

This converts underperformance into estimated lost revenue.

---

## 4️⃣ Decision Engine

Entities were categorized into:

- ✅ Positive Lift Drivers (Top Performers)
- ⚠️ Underperformers (Revenue Leakage Drivers)
- 🔎 Stage-Level Bottlenecks
- 📉 Lead Source Risk Areas

This transforms descriptive analytics into strategic insights.

---

# 📊 Key Insights

### 🔥 Top Revenue Leakage – Sales Reps
- Rep_22: ₹239K potential recovery
- Rep_18: ₹197K potential recovery
- Rep_7: ₹195K potential recovery

### 🔍 Stage-Level Leakage
- Qualified Stage: ~₹766K estimated leakage
- Proposal Stage: ~₹141K estimated leakage

### 📉 Lead Source Leakage
- Partner Channel: ~₹419K estimated improvement opportunity

These insights indicate that pipeline efficiency improvements may drive more impact than individual rep optimization.

---

# ⚙️ How to Run the Project

1. Clone repository: `gh repo clone suryamr2002/SkyGeni-Sales-Intelligence-Challenge`
2. Install dependencies: `pip install python pandas numpy matplotlib`
3. Run notebook


---

# 🏗 Key Decisions

### Why Use Global Win Rate as Benchmark?
It provides a simple, interpretable baseline for identifying lift across different entities.

### Why Translate Lift into Revenue?
Executives respond to financial impact, not percentages.

### Why Keep the Model Simple?
For business decision support:
- Interpretability > complexity
- Transparency > black-box modeling

This solution is designed for clarity and actionability.

---

# 🚀 What Makes This Different?

Most sales dashboards stop at:
- Conversion rates
- Revenue totals

This system adds:
- Lift normalization
- Quantified revenue opportunity
- Structured decision categories

It moves from reporting to decision intelligence.

---

# 🔮 Future Improvements

If extended further, I would:

- Build a difficulty-adjusted predictive win model
- Add expected vs actual performance scoring
- Implement rolling benchmarks for drift monitoring
- Deploy as a Streamlit decision dashboard

---

# 🏁 Conclusion

This project demonstrates:

- Business-first problem framing
- Clear metric design
- Decision-oriented analytics
- Practical engineering structure

The system provides a structured, financially interpretable framework for improving sales performance.

