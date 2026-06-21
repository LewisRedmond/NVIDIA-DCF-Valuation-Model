# Methodology

## 1. Forecast Period and Structure
- Why 5 years (FY2027E–FY2031E) was chosen as the explicit forecast horizon
- Note on the Capex/D&A ratio (5.5x in FY2027E, 1.5x by FY2031E) and why this 
  suggests steady-state may not be fully reached within 5 years — an explicit 
  limitation, not an oversight

## 2. Revenue Build
- Top-down vs bottom-up rationale: explain you used a top-down growth-rate fade 
  (10%→9%→8%→6.5%→5%) rather than segment-level bottom-up, and why (data 
  availability at the public-filing level)
- Bear/Base/Bull construction logic

## 3. Margin Assumptions
- Why gross margin reverts to 75% (matches FY2025A actual) rather than holding 
  flat at FY2026A's depressed 71.1%
- SG&A/R&D held as flat % of revenue — acknowledge this likely understates 
  operating leverage NVIDIA would realistically achieve at scale

## 4. Working Capital
- DSO/DIO/DPO methodology: derived from FY2026A actuals (65/125/57 days), 
  held flat rather than assuming further efficiency gains
- Explain why DIO is unusually high for a tech company (GPU supply chain buffer 
  stock, not typical SaaS-style working capital profile)

## 5. PP&E and Reinvestment
- Capex as % of revenue (6.5%) vs. the historical depreciation-implied rate (45%) 
  vs. the conservative 27% rate actually used — explain the judgment call
- The Capex/D&A ratio finding and what it implies about terminal year FCF quality

## 6. WACC Construction
- Full CAPM walkthrough: Rf, ERP, beta sourcing
- Why debt is economically irrelevant to WACC at NVIDIA's capital structure 
  (0.26% of total capital) — explain this is a structural feature of mega-cap 
  tech balance sheets, not a modelling simplification

## 7. Terminal Value — Dual Method Cross-Check
- Why both perpetuity growth and exit multiple are calculated
- The implied-growth back-solve check (3.40% from the 11x exit multiple) and 
  what exceeding the 3% ceiling tells you about multiple assumption tension

## 8. Known Simplifications (Be Explicit)
- Debt held flat (no dynamic paydown/cash sweep)
- Dividends not projected forward despite historical precedent
- SBC added back without separate dilution adjustment
- Several balance sheet lines (leases, intangibles, goodwill, APIC, AOCI) held flat

## 9. Sensitivity Methodology
- Explain the WACC × terminal growth Data Table mechanism
- Note the override-cell architecture (Sensitivity!K2/K3) required to make 
  Excel Data Tables work around cross-sheet formula limitations — this is 
  worth including because it demonstrates you understand a genuine Excel 
  technical constraint, not just DCF theory
