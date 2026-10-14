Finding 001
Title
Wide Receiver Route Drills May Be More Informative Than Traditional Combine Drills

Date
2026-10-14

Objective
Identify which NFL Combine drills provide the most representative movement patterns for studying future NFL receiver performance.

Evidence
Number of WRs
106
Most Frequent WR Drills
GAUNTLET_DRILL              18081
POST_CORNER_ROUTE_RIGHT     10454
DAGGER_ROUTE_LEFT            9827
GO_ROUTE_RIGHT               9767
SLOT_SAIL_ROUTE_RIGHT        9394
COMEBACK_ROUTE_RIGHT         9212
Route Visualization
Analyzed drill:

POST_CORNER_ROUTE_RIGHT
Observations:

Route is not linear.
Route contains a clear directional transition.
Player continues accelerating during the movement.
Movement resembles a real NFL route.
Data Quality Finding
Tracking records contain two entity types:

PLAYER
BALL
For route analysis, records must be filtered using:

sample_player = sample[
    sample["entity_type"] == "PLAYER"
]
Preliminary Metrics
Speed
Mean Speed = 7.52 yd/s
Max Speed  = 9.42 yd/s
Acceleration
Mean Acceleration = 2.93 yd/s²
Max Acceleration  = 4.88 yd/s²
Direction
Minimum Direction = 70°
Maximum Direction = 145°
Approximate directional transition:

75°
Interpretation
Route-specific receiver drills appear to contain richer movement information than traditional Combine drills.

Potential signals:

Direction changes
Speed preservation
Acceleration recovery
Route smoothness
Route efficiency
Candidate Metric
CODE Score
Change Of Direction Efficiency

Concept:

Large directional change
+
High retained speed
=
High CODE Score
Prototype:

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

Next Steps
Extract all WR route attempts.
Compute movement metrics for every route.
Build a WR feature dataset.
Compare route metrics against traditional Combine metrics.
Evaluate NFL separation relationships.

