# Verification Activity Report

## Check 1 — Invalid Transition (`IDLE` → `DELIVERING`)
* **Can this happen?** No.
* **Requirement Violated:** **R9**
* **Analysis:** An IDLE robot cannot start delivering immediately without receiving a request and navigating to the destination.

## Check 2 — Missing Transition (`NAVIGATING` → `AVOIDING_OBSTACLE` with no return)
* **Can the robot continue its delivery?** No.
* **Analysis:** Without a transition from `AVOIDING_OBSTACLE` back to `NAVIGATING` (Transition T3), the robot causes a system deadlock and remains stuck in obstacle-avoidance mode indefinitely.

## Check 3 — Obstacle During Delivery (`AVOIDING_OBSTACLE` → `DELIVERING`)
* **Can the robot move directly from `AVOIDING_OBSTACLE` to `DELIVERING`?** No.
* **Requirement Violated:** **R10**
* **Analysis:** Obstacle avoidance is a navigation maneuver. Once resolved, the robot must return to `NAVIGATING` to verify its trajectory before entering the `DELIVERING` state.
