Finding 001
Title
Wide Receiver Route Drills May Be More Informative Than Traditional Combine Drills

Date
2026-10-14

Objective
Identify which NFL Combine drills provide the most representative movement patterns for studying future NFL receiver performance.

Background
The initial project hypothesis assumed that traditional Combine drills such as:

FORTY_YARD_DASH
THREE_CONE_DRILL
SHORT_SHUTTLE
would provide the strongest signals for evaluating future receiver success.

However, the available tracking dataset contains several route-specific wide receiver drills that more closely resemble real game situations.

Dataset Audit Findings
Number of Wide Receivers (WR):

106
GAUNTLET_DRILL                18,081
POST_CORNER_ROUTE_RIGHT       10,454
DAGGER_ROUTE_LEFT              9,827
GO_ROUTE_RIGHT                 9,767
SLOT_SAIL_ROUTE_RIGHT          9,394
COMEBACK_ROUTE_RIGHT           9,212
OVER_SHOULDER_ADJUST           8,642
SLOT_STRIKE_ROUTE_LEFT         8,389
CURL_ROUTE_RIGHT               7,935
RED_ZONE_FADE_RIGHT            6,168

Route Visualization Analysis

A complete trajectory from:

Plain Text
POST_CORNER_ROUTE_RIGHT

was visualized using tracking coordinates.

Initial observation:

The route contains a progressive directional transition.
The movement is clearly non-linear.
The player accelerates while changing direction.
The movement pattern resembles a realistic NFL route.

This behavior appears substantially different from the movement observed in generic speed drills.

Tracking Validation

A route instance was validated to contain:

Plain Text
1 nfl_id
1 event_id

confirming that a single player and a single drill attempt were being analyzed.

An additional data quality issue was identified:

Tracking records contain both:

Plain Text
PLAYER
BALL

entities.

This required filtering:

Python
entity_type == "PLAYER"

before performing route analysis.

Preliminary Metrics

Statistics extracted from the analyzed route:

Speed
Plain Text
Mean Speed: 7.52 yd/s
Maximum Speed: 9.42 yd/s
Acceleration
Plain Text
Mean Acceleration: 2.93 yd/s²
Maximum Acceleration: 4.88 yd/s²
Direction
Plain Text
Minimum Direction: 70°
Maximum Direction: 145°

Approximate directional transition:

Plain Text
75°

indicating a substantial route adjustment.

Research Implications

The analyzed route suggests that receiver-specific drills contain richer information than traditional Combine metrics.

Potentially valuable signals include:

Directional transitions
Speed conservation during a cut
Acceleration recovery after direction changes
Route smoothness
Route efficiency

These characteristics cannot be directly measured using traditional Combine metrics such as the 40-Yard Dash.

New Research Direction

The project focus will shift from generic agility testing toward route-specific movement analysis.

Primary candidate drills:

POST_CORNER_ROUTE_RIGHT
COMEBACK_ROUTE_RIGHT
SLANT_ROUTE_LEFT
CURL_ROUTE_RIGHT
Candidate Feature
CODE Score

Change Of Direction Efficiency

Concept:

Plain Text
Large directional change
+
High retained speed
=
High CODE Score

First prototype:

Python
direction_change = (
sample_player["dir"]
.diff()
.abs()
.sum()
)
 
avg_speed = sample_player["s"].mean()
 
code_score = avg_speed * direction_change
Status

✅ Confirmed Finding

This finding will be used as the foundation for Feature Engineering Phase 1.

Next Steps
Extract all WR route drill attempts.
Compute movement features for every route.
Build a WR feature dataset.
Compare route-derived metrics against traditional Combine measurements.
Evaluate their relationship with NFL separation metrics.
