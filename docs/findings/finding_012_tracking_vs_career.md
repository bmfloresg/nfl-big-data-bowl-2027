# Finding 012

## Title

Tracking-Derived Route Metrics Show Preliminary Association with Early NFL Career Success

## Context

After creating route-level and player-level tracking metrics from the
POST_CORNER_ROUTE_RIGHT drill, an exploratory validation was performed
against NFL career outcomes.

The objective was to determine whether tracking-derived route execution
metrics contain information beyond traditional combine measurements.

---

## Metrics Evaluated

Tracking Metrics:

- CODE Score V3
- Path Efficiency
- Direction Change

Traditional Metrics:

- Forty Yard Dash
- NGS Athleticism Score

Career Outcomes:

- Career Games Started
- Career Offensive Snaps

---

## Results

### Correlation with Career Games Started

| Metric | Correlation |
|----------|----------:|
| CODE Score V3 | 0.256 |
| NGS Athleticism Score | 0.205 |
| Forty Yard Dash | -0.174 |

### Correlation with Career Offensive Snaps

| Metric | Correlation |
|----------|----------:|
| CODE Score V3 | 0.239 |

---

## Additional Validation

Players were divided into quintiles based on CODE Score V3.

Average NFL Games Started:

| CODE Quintile | Avg Games Started |
|---------------|------------------:|
| Q1 | 2.68 |
| Q2 | 9.21 |
| Q3 | 5.63 |
| Q4 | 7.47 |
| Q5 | 9.68 |

The relationship is not perfectly monotonic, but players in the highest
CODE quintile accumulated substantially more starts than players in the
lowest quintile.

---

## Interpretation

The observed relationships are modest and should not be interpreted as
proof of predictive power.

However, two findings are noteworthy:

1. CODE Score V3 appears largely independent from traditional combine
   metrics.

2. CODE Score V3 exhibits a slightly stronger association with NFL usage
   metrics than the Forty Yard Dash and NGS Athleticism Score in this
   sample.

These results suggest that route-execution characteristics derived from
tracking data may capture a dimension of player evaluation not fully
represented by traditional combine testing.

---

## Limitations

- Analysis limited to a single drill:
  POST_CORNER_ROUTE_RIGHT

- Sample size:
  95 wide receivers

- CODE Score V3 remains experimental.

- No control for draft capital, team context, injuries, or playing opportunity.

- Correlation does not imply causation.

---

## Next Steps

1. Replicate the analysis across additional WR route drills.
2. Separate route execution into Burst, Agility, and Efficiency dimensions.
3. Validate against additional NFL performance outcomes.
4. Control for draft position and athletic testing variables.
5. Evaluate whether tracking metrics provide incremental value over existing combine metrics.

---

## Status

🟡 Preliminary Evidence

