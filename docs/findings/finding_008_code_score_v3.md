Finding 008
Title
CODE Score V3 Produced a Balanced Route Ranking

Method
direction_change and path_efficiency were standardized using z-scores.

CODE Score V3 was defined as:

code_score_v3 = direction_change_z + path_efficiency_z

Observation
The resulting score ranks players who simultaneously:

execute large direction changes
maintain efficient route geometry
Outcome
CODE Score V3 appears more balanced than CODE Score V2.

Status
Promising Candidate Metric
Validation
The metric generates a near-normal distribution with:

Mean ≈ 0

Std ≈ 1

The ranking identifies players who simultaneously:

achieve large directional transitions
maintain efficient route geometry
This behavior was not observed using the raw multiplication approach.
