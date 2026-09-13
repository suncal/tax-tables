# tax-tables — 2026 income tax, sales tax, VAT and mortgage-rate data

Machine-readable tax tables behind the calculators at **[paysums.com](https://paysums.com/)**, republished here for developers, analysts and journalists.

Canonical page, file descriptions and update log: **https://paysums.com/open-data/**

## What's in `data/`

| File | Contents |
|---|---|
| `us-federal-income-tax-brackets-2026.csv` | Federal brackets by filing status (IRS inflation adjustments) |
| `us-federal-2026.json` | Brackets, standard deduction, FICA rates/wage base, 401(k)/HSA limits |
| `us-state-income-tax-2026.csv` | All 50 states + DC: type, top rate, bracket count, standard deduction, exemption, as-of year, local-tax flag, source |
| `us-states-2026.json` | Full state tables: brackets, deductions, credits, local taxes, payroll programs |
| `us-sales-tax-by-state-2026.csv` | Statutory state rate and the state's official address-level lookup URL |
| `us-sales-tax-cities-2026.csv` | Combined rate in 40 major cities |
| `vat-gst-rates-2026.csv` | Standard and reduced VAT/GST rates, 39 countries |
| `mortgage-rates-weekly.csv` | Weekly 30- and 15-year fixed averages (Freddie Mac PMMS), last 104 weeks |
| `uk|ca|au|in|de|fr-tax-2026.json` | Country data files: UK PAYE/NI, Canada federal+provincial/CPP/EI, Australia, India, Germany §32a/Sozialversicherung, France cotisations/barème |

`brackets` are arrays of `[upper_bound, rate]`, `null` = top band. Every file carries its official source and as-of year.

## How it stays current

A weekly automated check reads the official sources (IRS, SSA, state revenue departments, HMRC, CRA, ATO, incometax.gov.in, BMF, URSSAF/DGFiP) and the files are regenerated and pushed here whenever a figure changes. Mortgage rates refresh every Thursday.

## Licence and provenance

Our compilation is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Cite as: *paysums.com, 2026 tax tables, https://paysums.com/open-data/*.

The figures themselves are government publications: US federal and state tax tables and statutes are public domain; UK figures are Crown copyright under the Open Government Licence v3; EU Commission VAT tables are CC BY 4.0; Canadian, Australian, Indian, German and French figures are statutory rates and thresholds. No restriction of ours applies to them.

`mortgage-rates-weekly.csv` reproduces Freddie Mac Primary Mortgage Market Survey averages, which Freddie Mac makes available "with proper attribution" — credit *Source: Freddie Mac* when you reuse it; it is not part of the CC BY grant.

Statutory tables, not tax advice.
