# Executive Memo

**Created by:** [Mason Pritts]  
**Updated by:** [Mason Pritts]  
**Date Created:** [10/23/2025]  
**Date Updated:** [10/24/2025]  
**Version:** [1.0]
**LLM Used:"" [ChatGPT]

---

## Executive Summary 
Our U.S.-based pharmaceutical company expects to receive €8,000,000 in one year from a European client. With the current market conditions of spot rate EUR/USD = 1.16 and one-year forward = 1.0890, the U.S. dollar value of this receivable is exposed to exchange rate fluctuations. If the euro depreciates against the dollar, the USD proceeds will decline, potentially decreasing our profit margins. To mitigate this risk, we will be taking a look at three hedging strategies: 1. a forward contract, 2. money market hedge, and 3. an option-based hedge (using EUR puts or calls). Each strategy provides varying levels of protection, flexibility, and cost. This memo outlines the exposure, the rationale for hedging, and the pros and cons of each approach to help make the most informed decision on FX risk management.

---

## Background & Objectives
Our company knows it has a €8 million receivable due in one year, which represents revenue from European pharmaceutical sales. Since our financial reporting and operating currency is the U.S. dollar, the future USD value of this receivable depends on the EUR/USD exchange rate at the time of payment.

The risk arises because the euro may weaken relative to the dollar during the year. At the current spot rate (1.16), the receivable is worth $9.28 million USD, but if the rate falls to the forward rate of 1.09 or lower, proceeds could drop by nearly $560,000 or more.

Our objective is to protect USD cash flows while balancing cost, flexibility, and potential upside if the euro appreciates. Hedging ensures more predictable outcomes and helps stabilize earnings against currency volatility.

---

## Methods
To address our foreign exchange exposure, we will conduct a comparative analysis of three hedging techniques, each using the current market data provided.

Forward Contract
A forward contract locks in a fixed exchange rate of 1.0890 for converting the future €8,000,000 receivable into U.S. dollars in one year. This provides full protection against currency depreciation risk and eliminates exchange rate uncertainty. The drawback is that if the euro strengthens beyond 1.0890, the company cannot participate in any favorable movement, so the gain is capped.

Money Market Hedge
For a money market hedge, we would borrow the present value of €8,000,000 at the current 1-year Euribor euro interest rate of 2.15%, convert the funds into dollars at the spot rate (1.16), and invest the proceeds in the U.S. at the 1 year Treasury 3.55% interest rate. After one year, the investment will mature into a known dollar amount that matches the euro receivable, which will then be used to repay the euro loan. This approach synthetically locks in the forward rate implied by interest rate parity but requires more complex cash flow management and potential borrowing costs which would reduce proceeds.

Option Hedge (Put on EUR)
A put option on EUR/USD with a strike price near 1.16 would give the company the right, but not the obligation, to sell euros at that rate in one year. The option provides downside protection if the euro depreciates while allowing full participation if the euro appreciates. The downside is the upfront premium cost of approximately $0.021 per euro, or about $168,000 for the full exposure. 

These methods will be evaluated quantitatively using spreadsheet modeling and scenario analysis to compare their outcomes under different exchange rate conditions.

---

## Limitations & Next Steps
This initial assessment assumes that interest rates (USD 3.55% and EUR 2.15%) remain stable over the one-year horizon, transaction costs are limited to option premiums, and counterparty credit risk is negligible. Market volatility, shifts in monetary policy, or unexpected geopolitical events could also affect both option pricing and forward rates, which will be addressed in later stages of analysis.

Next Steps:

Technical Specification - Develop a detailed quantitative plan outlining inputs (spot rate, forward rate, interest rates, option premiums), formulas for each hedge strategy, and output metrics such as net USD proceeds and effective exchange rate.

Excel Model Build - Create a spreadsheet implementing these formulas to compute and compare hedged versus unhedged outcomes.

Prompt Engineering - Draft a structured AI prompt that, when given the key input variables, automatically generates the spreadsheet according to the technical specification.

Final Analysis & Recommendation - Use the completed model to test exchange rate scenarios, assess sensitivity to rate changes, and recommend the most cost-effective hedge strategy.

These next steps will provide a clear, data-driven framework for selecting the best hedge structure, ensuring informed and defensible financial decision-making.

---

## References
“EUR/USD (EURUSD=X) Live Rate, Chart & News - Yahoo Finance.” Finance.yahoo.com, finance.yahoo.com/quote/EURUSD=X/.
“Check out U.S. 1 Year Treasury’s Stock Price (US1Y) in Real Time.” CNBC, www.cnbc.com/quotes/US1Y.
Trading Economics. “Euro Area Interest Rate.” Tradingeconomics.com, TRADING ECONOMICS, 2025, tradingeconomics.com/euro-area/interest-rate.
