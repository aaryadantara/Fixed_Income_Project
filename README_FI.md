# Fixed Income Investment Brief: US Treasury Portfolio Strategy & Immunisation

Coursework project for FBA1013, MSc Finance, Dublin City University.

## Overview

A fixed income investment brief for a risk-averse client with a $50M USD Treasury allocation (part of a larger two-currency, sovereign-only mandate also including a €43M EUR pool). Covers yield curve modelling, portfolio construction, scenario analysis, and liability-driven immunisation for an $8M obligation due in two years.

## Methodology

1. **Yield curve modelling** — fitted a Nelson-Siegel-Svensson (NSS) curve to observed US Treasury yields (1yr–30yr) to capture short-end inversion, mid-curve steepening, and long-end flattening
2. **Portfolio construction** — built a laddered $50M portfolio across six UST maturities (2026–2040) to balance yield, duration, and reinvestment flexibility
3. **Scenario & sensitivity analysis** — stress-tested the portfolio under ±100bps parallel shifts and a bear-steepener scenario; quantified convexity asymmetry using a long-dated bond example
4. **Liability immunisation** — constructed a duration-matched two-bond portfolio (target duration 2.000 years) to fund the $8M liability, stress-tested at ±200bps

## Key findings

- NSS-fitted curve: β₀ = 3.97% (long-run level), with short-end inversion reflecting rate-cut expectations and +125bps of steepening from the 3yr to 10yr point
- Recommended $50M portfolio: 4.19-year duration, 2.248% weighted YTM, laddered across six maturities from 0% UST 2026 to 3% UST 2040
- Scenario impact: approximately −4.0% under a +100bps shock, +4.5% under a −100bps shock; 70% short-end weighting insulates against a bear-steepener
- Convexity advantage demonstrated on the 3% UST 2061: +23.6% gain on −100bps vs. −17.7% loss on +100bps, a 5.9 percentage point asymmetry favouring the long end
- Immunisation portfolio (47.06% in 1% UST 2027, 52.94% in 2% UST 2028) matches the $8M liability's 2-year duration at a current cost of $7.72M, with key risks flagged around convexity mismatch beyond ±200bps

## Tools

Python (yield curve fitting via scipy optimisation, bond pricing and duration/convexity calculations)

## Files

- Analysis notebook/script — NSS curve fitting, portfolio construction, scenario and immunisation analysis
- Investment brief deck — client-facing summary of rationale, recommendation, and risk management
