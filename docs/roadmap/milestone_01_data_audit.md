Milestone 01 - Data Audit
Status
✅ Completed

Objectives
Understand competition datasets.
Explore player distribution.
Identify target position group.
Explore combine tracking structure.
Completed Tasks
Dataset Loading
Successfully loaded:

players.csv
combine_results.csv
combine_tracking.csv
Position Analysis
Wide Receivers (WR) identified as the largest position group.
Total WR players: 106.
Tracking Exploration
Analyzed:

x
y
s
a
dir
movement variables.

Route Drill Discovery
Identified the most common WR route drills:

GAUNTLET_DRILL
POST_CORNER_ROUTE_RIGHT
DAGGER_ROUTE_LEFT
GO_ROUTE_RIGHT
SLOT_SAIL_ROUTE_RIGHT
COMEBACK_ROUTE_RIGHT
Tracking Validation
Validated that tracking contains:

PLAYER
BALL
entities.

Route analysis requires filtering:

entity_type == "PLAYER"

Route Visualization

Visualized a full WR route from:
POST_CORNER_ROUTE_RIGHT


