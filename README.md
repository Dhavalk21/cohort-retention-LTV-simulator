# 📊 Interactive Cohort Retention & LTV Simulator

An interactive analytics dashboard built to model user retention curves, simulate onboarding optimizations, and project compounding Customer Lifetime Value (LTV) across various digital business models.

### 🔗 Live Link: [Launch the Interactive Simulator Here](https://dhavalk21.github.io/Cohort-Retention-LTV-Simulator/)

## 🌟 Core PM Competencies Demonstrated

* **SaaS & Subscription Analytics:** Models user cohort decay trends over a 12-month lifecycle, distinguishing between high-retention SaaS models and high-volume Consumer application dynamics.
* **Financial Modeling & ROI Projections:** Translates user behavior metrics (such as a 10% increase in onboarding activation) directly into Customer Lifetime Value (LTV) improvements and Net Annual Profit Expansion.
* **LTV:CAC Health Analysis:** Evaluates the vital relationship between customer acquisition costs and lifetime value, signaling whether product economics are healthy (target index $\geq 3.0x$) or need adjustments.
* **Executive Communication:** Features a built-in automated strategy brief generator that summarizes complex cohort models into plain-English executive memos ready for leadership review.

## ⚙️ How the Economics are Calculated

This simulator computes user lifecycle value and growth using industry-standard SaaS formulas:

1. **Continuous Cohort Decay:** User retention at Month $t$ is modeled log-logistically between standard milestone anchors (Month 1, 3, 6, and 12 baseline inputs) to create a smooth, realistic customer retention curve:
   $$\text{Retention Rate } (R_t) \in [0, 100\%]$$

2. **Customer Lifetime Value (LTV):** Sum of the expected revenue contribution of a user over their first year:
   $$\mathrm{LTV} = \sum_{t=0}^{12} (R_t \times \mathrm{ARPU})$$
   *Where **ARPU** is the Average Revenue Per User per month.*

3. **LTV to CAC Ratio:** Evaluates business sustainability:
   $$\text{Ratio} = \frac{\text{LTV}}{\text{CAC}}$$

4. **Net Enterprise Value Delta:** Calculates the compounding annual benefit of a product change:
   $$\Delta \text{Annual Revenue} = \text{Monthly Signups} \times 12 \times (\text{Optimized LTV} - \text{Baseline LTV})$$

## 🚀 Technical Architecture

* **Responsive SVG Graphs:** Features an interactive vector line chart mapping baseline vs. optimized retention curves using smooth cubic Bezier paths.
* **Client-Side Calculations:** Run completely on highly responsive, vanilla JavaScript with zero tracking cookies or database dependencies.
* **Tailwind CSS Styling:** Crafted using a clean, accessible layout designed for high-resolution widescreen monitors and mobile screens alike.
* **Interactive Tooltips:** Friendly, built-in documentation overlays next to every metric, helping stakeholders understand complex product operations terms on hover.
