Milestone 03 - Validation
Status
🟡 In Progress

Objective
Evaluate whether tracking-derived route execution metrics provide meaningful information beyond traditional NFL Combine measurements.

The primary goal is not to optimize a score, but to determine whether tracking features capture a distinct and potentially valuable dimension of player evaluation.

Research Questions
RQ1
Do route-execution metrics contain information that is not already captured by traditional combine metrics?

RQ2
Do route-execution metrics show any relationship with NFL career outcomes?

RQ3
Which tracking-derived dimensions are most relevant?

Burst
Agility
Efficiency
RQ4
Are the observed relationships consistent across multiple WR route drills?

Starting Point
Datasets available:

Route Features
wr_route_features_v1.csv
wr_route_features_v1_with_code.csv
Aggregated Features
player_features
Combine Data
combine_results.csv
NFL Outcomes
player_career_successes.csv
Baseline Findings from Milestone 02
CODE vs Combine
Correlation:

CODE Score V3 ↔ Forty

r = -0.08
Correlation:

CODE Score V3 ↔ NGS Athleticism Score

r = 0.09
Interpretation:

Tracking-derived route metrics do not appear to be simple reproductions of traditional combine evaluations.

CODE vs NFL Outcomes
Correlation:

CODE Score V3 ↔ Career Games Started

r = 0.256
Correlation:

CODE Score V3 ↔ Career Offensive Snaps

r = 0.239
Interpretation:

A preliminary relationship exists between route-execution metrics and NFL career outcomes.

Validation Tasks
Task 1
Validate tracking metrics against NFL career outcomes.

Metrics:

career_games_started
career_offensive_snaps
pro_bowl_original_ballot
ap_all_pro_1st_team
ap_all_pro_2nd_team
Task 2
Compare tracking metrics against combine metrics.

Metrics:

forty
ten_yd_split
ngs_athleticism_score
Goal:

Determine whether tracking provides incremental information.

Task 3
Move from a single composite score to interpretable dimensions.

Candidate dimensions:

Burst Score
Based on:

burst
avg_acceleration
max_acceleration
Agility Score
Based on:

direction_change
agility_index
Efficiency Score
Based on:

path_efficiency
Task 4
Test reproducibility across drills.

Current drill:

POST_CORNER_ROUTE_RIGHT
Future drills:

COMEBACK_ROUTE_RIGHT
GO_ROUTE
SLANT_ROUTE
GAUNTLET
Goal:

Determine whether findings generalize.

Success Criteria
The milestone will be considered successful if at least one tracking-derived dimension satisfies the following:

Criterion A
Provides information independent from traditional combine metrics.

Criterion B
Shows a measurable relationship with NFL career outcomes.

Criterion C
Remains stable across multiple WR drills.

Deliverables
Expected outputs:

player_features_v2.csv
burst_score
agility_score
efficiency_score
Documentation:

Finding 013
Finding 014
Finding 015
Working Hypothesis
Route-execution characteristics measured through combine tracking represent a distinct dimension of player evaluation that is not fully captured by traditional combine testing and may contribute to explaining differences in early NFL career success.

Risks
Sample size remains limited.
Single-drill conclusions may not generalize.
Observed correlations may be driven by noise.
Career outcomes are influenced by many factors beyond athletic ability.
Next Decision Gate
Proceed to expanded validation only if tracking-derived metrics continue to show:

Low redundancy with combine metrics.
Positive association with NFL outcomes.
Consistent behavior across multiple route drills.
