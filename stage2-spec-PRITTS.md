# Technical Specifications

**Created by:** [Mason Pritts]  
**Updated by:** [Mason Pritts]  
**Date Created:** [11/6/2025]  
**Date Updated:** [11/7/2025]  
**Version:** [1.0]
**LLM Used:"" [ChatGPT]

**Role:** Treasury Analyst
**Audience:** Director of Treasury  

**Purpose:** Provide a professional, quantitative specification outlining the analytical structure for evaluating FX hedging alternatives.

---

## 1. Problem Statement

Our company has a €8,000,000 receivable due in one year from a European client, creating foreign exchange exposure to fluctuations in the EUR/USD rate. Since our functional currency is the U.S. dollar, any depreciation of the euro would reduce the USD value of the payment and negatively affect reported revenues and profit margins.

The objective of this analysis is to protect the U.S. dollar value of the future euro-denominated inflow while balancing cost, flexibility, and potential upside if the euro appreciates. This issue falls under the purview of corporate treasury, which is responsible for managing currency risk across international operations.

Accordingly, this specification establishes a framework to quantify, compare, and evaluate three hedging alternatives—forward contracts, money market hedges, and option-based hedges—to determine the most effective strategy for mitigating exchange rate risk and ensuring predictable USD cash flows.

---

## 2. Inputs (Known Variables)

Here is a table providing known variables to be used in calculations.

| Variable | Description | Unit | Input | Source |
|-----------|-------------|------|----------|--------|
| `FC_AMT` | Foreign-currency receivable | EUR | 8,000,000 | Company data |
| `S₀` | Current EURUSD spot rate | EUR/USD | 1.16 | Market data |
| `F₀` | 1-year EURUSD forward rate | EUR/USD | 1.0890 | Provided |
| `r_USD` | USD 1-year interest rate | % | 3.55 | Market data |
| `r_EUR` | EUR 1-year interest rate | % | 2.15 | Market data |
| `t` | Time to maturity | Years | 1 | Derived |
| `K_put` | EUR Put strike | EUR/USD | 1.16 | Analyst choice |
| `Premium_put` | Put premium | USD per contract | 0.021 | Scenario |

---

## 3. Assumptions & Constraints

The following assumptions and conventions apply to ensure analytical consistency and replicability across all hedge calculations:

- All EUR/USD exchange rates are expressed as USD per 1 EUR.
- Both the USD (3.55%) and EUR (2.15%) interest rates are annualized simple rates based on a 1 year maturity.
- The provided forward rate (1.0890) represents a 1 year maturity.
- Bank fees, bid–ask spreads, and counterparty credit risk are excluded from the analysis except for the explicit option premium.
- Option premiums are paid upfront in USD, calculated at $0.021 per EUR for the put.
- The put option uses an at-the-money strike of 1.16 EUR/USD, representing current spot levels.
- Interest accrual and conversion follow interest rate parity conventions, assuming the company can borrow or lend at the quoted rates without restriction.
- Interest rates and forward rates once locked in are assumed constant over the 1 year horizon, with no interim rate resets or unexpected policy changes.
- All option positions are treated as European-style, exercisable only at maturity.

---

## 4. Calculation Flow

The analysis will follow a structured sequence to make sure there is consistency across all three hedge methods and comparability of results. Each step builds on the previous one to produce clear and easy to understand USD outcomes.

1. Establish Input Parameters
Enter all given variables: spot rate (S₀), forward rate (F₀), interest rates (r_USD, r_EUR), time to maturity (t), option strikes (K_put, K_call), and premiums.
Confirm all values are expressed in consistent units (EUR, USD, or EUR/USD).

2. Unhedged Baseline
Calculate the USD value of the €8,000,000 receivable under varying future EUR/USD spot rates (S_T scenarios).
This serves as the reference point to measure hedge effectiveness.

3. Forward Hedge
Compute the locked-in USD proceeds by converting the €8,000,000 at the fixed forward rate (1.0890).
Record this amount as a constant across all S_T scenarios to show full protection against FX fluctuations.

4. Money Market Hedge
Determine the present value of the €8,000,000 receivable by discounting it at the EUR interest rate (2.15%).
Convert this discounted euro amount to USD at the current spot rate (1.16).
Invest the USD proceeds at the U.S. interest rate (3.55%) for one year.
Compute the future value of this investment to obtain the known USD proceeds from the money market hedge.

5. Option Hedge (Put and Call)
For each assumed future spot rate (S_T), calculate the option’s payoff:
For the put, if S_T < K_put, exercise and sell euros at K_put; otherwise, use S_T.
Subtract the total premium (premium × €8,000,000) from the resulting USD proceeds.
Record USD proceeds under both favorable and unfavorable EUR/USD outcomes.

6. Scenario Analysis
Repeat calculations under multiple S_T values to observe sensitivity of each hedge.
Create a comparison table showing USD outcomes for unhedged, forward, money market, and option hedges.

7. Comparison & Interpretation
Compare the stability of USD proceeds across hedging methods.
Highlight trade-offs:
Forward = certainty but no upside.
Money market = similar certainty but more operational complexity.
Option = flexibility and upside potential but with an upfront cost.

---

## 5. Outputs

Here is a table identifying and labeling the expected results from the model.

| Output | Description | Format | Purpose |
|---------|--------------|---------|----------|
| `USD_unhedged` | USD proceeds if left unhedged | Numeric | Baseline to compare |
| `USD_forward` | USD proceeds from forward hedge | Numeric | Certainty benchmark |
| `USD_mm` | USD proceeds from money market hedge | Numeric | Cross-check against forward |
| `USD_put` | USD proceeds from EUR put hedge | Table | Sensitivity & protection |
| `Chart_1` | Hedge outcomes vs. S_T | Line chart | Visual comparison of hedge performance |
| `Summary` | Written conclusion | 1–2 paragraphs | Executive-ready takeaway |

---

## 6. Sensitivity Plan

To assess how robust each hedge is to FX changes, the analysis will test a range of future EUR/USD spot rates and compare USD outcomes across all strategies.

FX Range
Vary future spot rate S_T from 0.95 × S₀ to 1.05 × S₀ (≈ 1.10–1.22 USD/EUR) in 0.01 increments.
For each S_T, calculate USD proceeds for all strategies: unhedged, forward, money market, and option hedges.

Outputs per Scenario
Record USD proceeds, effective exchange rate, and difference vs. unhedged and forward benchmarks.
Identify each hedge’s breakeven rate (where option and forward results are equal).

Visualizations
Line chart: USD proceeds vs. S_T for each hedge (main comparison).
Table: Key S_T scenarios (1.05, 1.075, 1.10, 1.125, 1.16, 1.175, 1.20, 1.225, 1.25).
Summary: Breakeven points, worst-case protection, and cost trade-offs.

---

## 7. Limitations & Next Steps

This analysis excludes factors such as exchange rate volatility, transaction costs, and counterparty credit risk (the risk that the bank or financial institution executing the hedge may default on its contractual obligations). Interest rates are assumed constant over the 1 year horizon, and option pricing uses a simplified premium input rather than a full model.

The next step is to build the Excel model implementing this framework to calculate USD outcomes for each hedge, test sensitivity across FX scenarios, and generate charts and summaries to support the final hedge recommendation.

---