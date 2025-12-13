# Memo: Executive Summary of FX Hedging Strategy for EUR Receivable

**To:** Senior Management

**From:** Treasury Analyst

**Date:** December 12, 2025

**Subject:** FX Risk Mitigation for €8,000,000 Receivable

**Version:** [1.0] **LLM Used:"" [Gemini]

---

### A. Exposure Summary

Our firm holds a significant foreign currency exposure: a **€8,000,000 receivable** due in **one year**. Since our functional currency is the USD, any weakening of the Euro against the Dollar over the next 12 months will negatively impact our final cash flows. This FX risk is substantial, as an unhedged position exposes us to a potential range of outcomes from a low of $8,800,000 (if EUR/USD drops to $1.10) to a high of $9,760,000 (if EUR/USD reaches $1.22).

### B. Summary of Hedge Outcomes

The analysis compares three distinct hedging strategies against the Unhedged position, utilizing the current spot rate ($S_0 = 1.16$), forward rate ($F_0 = 1.0890$), and current interest rates ($r_{USD} = 3.55\%$, $r_{EUR} = 2.15\%$).

| Strategy | USD Proceeds (Fixed or Minimum) | Key Feature |
| :--- | :--- | :--- |
| **Unhedged** | Highly Variable ($8,800,000 to $9,760,000) | Full exposure to market fluctuations. |
| **Forward Hedge** | **$8,712,000** | Lowest **fixed** proceeds. Locks in exchange rate $F_0 = 1.0890$. |
| **Money Market (MM) Hedge** | **$9,407,186** | Highest **fixed** proceeds. Based on Interest Rate Parity. |
| **Put Option Hedge** | **$9,106,038** (Net Minimum) | Provides a floor while retaining upside potential. |

*Note: The difference between the Forward Hedge $(8,712,000) and the Money Market Hedge $(9,407,186) suggests that the market-quoted Forward Rate (F_0 = 1.0890) is **inconsistent** with the calculated Interest Rate Parity using the given interest rates. The MM Hedge is theoretically sounder, as it applies the covered interest rate parity theorem.*

### C. Sensitivity Interpretation

The sensitivity analysis, shown in the table's "Winner of Hedges" column, reveals the core trade-off between certainty and flexibility:

| Scenario | EUR Depreciation ($S_T \leq 1.15$) | EUR Appreciation ($S_T \geq 1.17$) | Cost/Flexibility |
| :--- | :--- | :--- | :--- |
| **Money Market Hedge** | **Definitive Winner**. Guarantees high fixed proceeds of $\$9,407,186$ regardless of market fall. | Underperforms Unhedged and Put Option. Forfeits market gains. | **Certainty** is maximized; **flexibility** is zero. Free to execute (no premium). |
| **Put Option Hedge** | Offers a floor of $\$9,106,038$ (based on $K_{put}=1.16$ and premium cost of $\$168,000$). | **Outperforms MM Hedge**. Payoff increases directly with $S_T$ above the strike. | **Flexibility** is maximized; requires an upfront **Premium Cost** of $\$168,000$. |

---
**Hedge Payoff Visual Comparison**


### D. Strategic Recommendation

**Recommendation: Implement the Money Market Hedge (MM Hedge) Strategy.**

The Money Market Hedge is mathematically and economically the most advantageous **fixed** hedging strategy in this scenario, providing the highest certain USD proceeds of **$\$9,407,186$**.

### E. Executive Justification

The MM Hedge is the recommended strategy, aligning with core financial management priorities:

1.  **Cash Flow Stability and Budget Certainty:** The MM Hedge fixes the receivable cash flow at a high level ($\$9,407,186$). This provides the highest degree of certainty for financial planning, budgeting, and liquidity forecasts, mitigating the risk of a significant USD shortfall.
2.  **Risk Profile (Elimination of Downside):** This strategy completely eliminates the risk of an unfavorable rate movement. Given the goal of hedging a receivable, prioritizing downside protection is paramount.
3.  **Superiority Over Forward Contract:** By utilizing the MM Hedge (which is derived from Interest Rate Parity), we secure **$\$695,186$ more** than the market-quoted Forward Contract (the difference between $\$9,407,186$ and $\$8,712,000$). This avoids locking in a potentially unfavorable market rate.
4.  **Cost:** Unlike the Put Option, which requires an upfront premium, the MM Hedge is executed through a series of interbank transactions (borrowing and lending) and has no explicit premium cost, maximizing the net proceeds.
