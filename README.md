# econ5200-lab06-experiment-audit
# Experiment Design Audit — Power, Selection & Weighting

## Objective
I evaluated statistical power, selection bias, and inverse probability weighting to understand how experiment design and sample selection affect statistical estimates.

## Methodology
- Audited an A/B test with 2% traffic allocation and 1,000 treatment users to assess its power to detect a 0.8 percentage-point lift.
- Wrote my own `power_check` function and checked its results against `statsmodels`.
- Compared the naive estimate from a wellness-program comparison with the true treatment effect.
- Applied inverse probability weighting (IPW) to reduce selection bias.
- Calculated Meng's data defect correlation for a biased poll and compared its effective information with that of a random sample.

## Key Findings
- The A/B test had 19.8% power to detect a 0.8 percentage-point lift. Achieving 80% power required 12,514 users per group.
- With 50,000 users split evenly between the two groups, the test would have had 97.7% power.
- The naive wellness-program estimate was -$1,396, compared with the true effect of -$500.
- IPW brought the estimate closer to the true effect, reducing it to -$467.
- In the optional extension, 2.3 million biased poll responses provided about as much information as 402 random responses.
