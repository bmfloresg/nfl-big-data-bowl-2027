Finding 007
Observation
Path efficiency and direction change capture distinct dimensions of route execution.

Implication
A composite metric may better represent route-running effectiveness.

Candidate Metric
CODE Score V2

path_efficiency × direction_change

Status
Exploratory

Finding 007 Observation Path efficiency and direction change capture different dimensions of route execution.

Evidence Top performers in path efficiency are not necessarily top performers in direction change.

Implication A combined metric may better identify route-running effectiveness.

Candidate Metric CODE Score V2

code_score_v2 = path_efficiency * direction_change

Status Exploratory

Observation:

Raw multiplication between path_efficiency and direction_change is dominated by direction_change because the variables operate on different scales.

Next step:

Standardize both variables before constructing composite metrics.
