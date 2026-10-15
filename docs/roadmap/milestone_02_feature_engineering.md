Milestone 02 - Feature Engineering
Status
✅ COMPLETED

Objective
Transform raw WR tracking data into a route-level analytical dataset suitable for statistical analysis and metric design.

Scope
Drill analyzed:

POST_CORNER_ROUTE_RIGHT
Population:

Wide Receivers (WR)
Entity Filter:

PLAYER only
Dataset Created
wr_route_features_v1.csv
Final size:

110 route attempts
12 engineered features
Features Engineered
Speed
avg_speed
max_speed
Acceleration
avg_acceleration
max_acceleration
burst
Direction
direction_change
Route Geometry
path_length
straight_line
path_efficiency
Time
route_duration
Key Technical Validations
Tracking Validation
Confirmed that tracking events contain:

PLAYER
BALL
All feature calculations were restricted to:

entity_type == "PLAYER"
Temporal Validation
Tracking frequency validated:

10 Hz
Equivalent to:

0.1 seconds per frame
Direction Validation
Implemented circular directional changes using:

circular_diff()
to correctly handle the 0° / 360° boundary.

Path Length Validation
The official tracking variable:

dis
produced invalid path efficiency values.

Final implementation reconstructs travelled distance from:

x
y
coordinates.

Result:

path_efficiency <= 1
for all observations.

Experimental Metrics
CODE Score V2
Defined as:

path_efficiency * direction_change
Observation:

The metric was dominated by direction_change.

CODE Score V3
Defined as:

direction_change_z + path_efficiency_z
Observation:

Produces a balanced ranking and approximately normal distribution.

Status:

🟡 Experimental

Deliverables
Created:

wr_route_features_v1.csv
wr_route_features_v1_with_code.csv
Documented Findings:

Finding 004
Finding 005
Finding 006
Finding 007
Finding 008
Outcome
A validated route-level feature dataset was successfully created and is ready for player-level aggregation and NFL relevance testing.

Next Milestone
Milestone 03 - Validation

Goals:

Aggregate route metrics at player level.
Compare route metrics with traditional combine metrics.
Assess the usefulness of CODE Score.
Connect movement metrics with football outcomes.
