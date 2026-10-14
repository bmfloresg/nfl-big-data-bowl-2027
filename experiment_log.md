Experiment Log
2026-10-14
Project initialized.

Goal: Top 10 placement in NFL Big Data Bowl 2027.

Primary Research Focus: Wide Receivers (WR).

Initial Hypothesis: Change-of-Direction Efficiency predicts future NFL separation more effectively than traditional combine metrics such as the 40-yard dash.

Dataset Audit
Players dataset loaded successfully.

Next objective: Evaluate position distribution to determine the best position group for analysis.

Pending:

nfl_position
WR     106
CB      60
G       51
T       50
DT      47
TE      42
DE      36
OLB     30
SS      28
FS      25
C       20
NT       5
DB       5
ILB      2
RB       1
MLB      1
FB       1
Name: count, dtype: int64

Dataset Audit Results
Date: 2026-10-14

Findings:

WR is the largest position group with 106 players.
Tracking data contains positional coordinates, speed, acceleration and movement direction.
Combine results contain traditional metrics (40-yard dash, three-cone drill, shuttle).
The dataset appears suitable for constructing custom movement metrics.
Decision:

Proceed with WR-focused analysis.
Observation

Tracking events contain both PLAYER and BALL entities.

Implication

Trajectory analysis must be performed exclusively on PLAYER records to avoid distortions caused by ball tracking.

Action

Filter entity_type == "PLAYER" before creating movement metrics.

2026-10-14
Milestone 02 completed.

Created:

WR_ROUTE_FEATURES_V1
Scope:

POST_CORNER_ROUTE_RIGHT

Records:

110 route attempts

Validated Features:

avg_speed
max_speed
avg_acceleration
max_acceleration
burst
direction_change
path_length
straight_line
path_efficiency
route_duration
Key Methodological Fixes:

PLAYER-only filtering
Circular direction calculations
Geometric path reconstruction
Outcome:

First route-level feature dataset successfully generated.
