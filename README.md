# NVIDIA (NVDA) Discounted Cash Flow Valuation Model

A fully integrated, ground-up DCF valuation of NVIDIA Corporation, built independently 
in Excel to test whether a standard 5-year intrinsic valuation framework can reconcile 
with NVIDIA's current market price.

**Key finding:** Across a full WACC × terminal growth sensitivity grid — including the 
most optimistic defensible combination of inputs — implied share price tops out well 
below NVIDIA's current trading price, highlighting the gap between intrinsic-value 
frameworks and market pricing for platform-scale AI businesses.

---

## Overview

This project is a fully integrated three-statement DCF model for NVIDIA Corporation, 
built from public 10-K filings with no use of pre-built templates. The model projects 
five years of financial statements (FY2027E–FY2031E) from a FY2026A historical base, 
derives unlevered free cash flow, and discounts it back to a present enterprise and 
equity value using a first-principles WACC calculation.

The objective was not to produce a price target, but to understand — mechanically — 
how sensitive a rigorous intrinsic valuation is to terminal value assumptions, and what 
that sensitivity implies about how the market is actually pricing high-growth, 
platform-style businesses.

## Key Findings

| Metric | Value |
|---|---|
| WACC | 9.49% |
| Base case implied share price (Perpetuity Growth) | $68.08 |
| Base case implied share price (Exit Multiple, 11x EV/EBITDA) | $75.80 |
| Terminal Value as % of Enterprise Value | 73.8% |
| Sensitivity range (WACC 7.5%–11.5%, g 1.5%–3.5%) | ~$53 – ~$121 |
| Current market price (as of valuation date) | $207.41 |

Even the most optimistic corner of the sensitivity grid — the lowest defensible WACC 
paired with the highest defensible terminal growth rate — does not close the gap to 
the market price. This is explored further in [docs/methodology.md](docs/methodology.md).

## Model Structure

| Tab | Purpose |
|---|---|
| Cover | Methodology summary, scope, valuation date |
| Assumptions | All scenario drivers (Bear/Base/Bull), sourced and documented |
| Income Statement | 5yr historical + 5yr projected, full margin build |
| Balance Sheet | 5yr historical + 5yr projected, fully linked |
| Cash Flow Statement | CFO/CFI/CFF, linked to all schedules |
| Working Capital Schedule | DSO/DIO/DPO-driven AR, Inventory, AP |
| PP&E Schedule | Capex and depreciation roll-forward |
| Debt Schedule | Interest expense build |
| WACC | Cost of equity (CAPM), after-tax cost of debt, capital weights |
| DCF | FCFF build, discounting, EV-to-equity bridge |
| Terminal Value | Perpetuity growth and exit multiple methods, cross-checked |
| Sensitivity | WACC × terminal growth data table |
| Football Field | Summary valuation range vs. market price |

## Key Assumptions

| Driver | Bear | Base | Bull | Basis |
|---|---|---|---|---|
| FY2027E Revenue Growth | 6.0% | 10.0% | 14.0% | Consensus estimates, 10-K guidance |
| Gross Margin (steady-state) | 70.0% | 75.0% | 80.0% | FY2025A actual = 75.0% |
| Terminal Growth Rate | — | 2.5% | — | Long-run nominal US GDP growth |
| Exit Multiple (EV/EBITDA) | — | 11.0x | — | Semiconductor peer median |

Full assumption list with sourcing is documented on the Assumptions tab and in 
[docs/data_sources.md](docs/data_sources.md).

## Sensitivity Analysis

![Sensitivity Grid](assets/sensitivity_grid.png)

## Limitations

This model deliberately excludes or simplifies several factors, documented here for 
transparency rather than treated as oversights:

- Stock-based compensation is added back as a non-cash item without a separate 
  dilution adjustment to share count
- Debt is held flat across the forecast period (no dynamic cash sweep / paydown)
- Operating lease assets and certain non-core balance sheet items are held flat
- A single 5-year explicit forecast may understate the duration of NVIDIA's 
  current capital investment cycle, which the Capex/D&A ratio in the model 
  suggests has not reached steady state by the terminal year

## Skills Demonstrated

- Three-statement financial modeling and full statement linkage
- WACC derivation from first principles (CAPM, capital structure weighting, 
  unlevered/relevered beta methodology)
- FCFF-based intrinsic valuation
- Terminal value cross-validation (perpetuity growth vs. exit multiple)
- Two-variable sensitivity analysis (Excel Data Tables)
- Financial statement analysis from primary source filings (10-K)

## How to Use

1. Download `model/NVDA_DCF_Model.xlsx`
2. Open in Excel (2016 or later recommended for Data Table and Waterfall chart support)
3. The Assumptions tab scenario switch (cell C2) toggles between Bear (1), Base (2), 
   and Bull (3) scenarios — all downstream tabs update automatically
4. All blue-font cells are hardcoded inputs; black-font cells are formulas; 
   green-font cells link to other tabs

## Sources

- NVIDIA Corporation Form 10-K filings, FY2022–FY2026 (SEC EDGAR)
- Damodaran Online (NYU Stern) — Equity Risk Premium and industry beta data
- US Treasury — 10-Year Treasury yield
- Market data as of valuation date: January 25, 2026

## Disclaimer

This model was built for educational and portfolio purposes. It does not constitute 
investment advice or a recommendation to buy or sell any security. All projections 
are estimates based on publicly available information and involve significant 
uncertainty.

---

*Built by Lewis Redmond | https://www.linkedin.com/in/lewis-redmond1/ | 21/06/2026*
