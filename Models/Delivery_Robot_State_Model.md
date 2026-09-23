# Delivery Robot State Model

| State ID | State Name | Description | Entry Condition | Exit Condition |
| :--- | :--- | :--- | :--- | :--- |
| **S1** | `IDLE` | The robot is stationary at the warehouse waiting for a new assignment. | System startup OR arrival at warehouse (`Warehouse Reached`). | Reception of a valid delivery request (`Delivery Request Received`). |
| **S2** | `NAVIGATING` | The robot is actively moving toward the target destination or returning to the warehouse. | Reception of delivery request OR clearance of obstacle (`Obstacle Avoided`). | Reaching destination (`Destination Reached`), obstacle detection (`Obstacle Detected`), or critical battery (`Critical Battery`). |
| **S3** | `AVOIDING_OBSTACLE` | The robot executes maneuver protocols to bypass a detected obstacle in its path. | Detection of an obstacle while navigating (`Obstacle Detected`). | Successful clearance of the obstacle (`Obstacle Avoided`). |
| **S4** | `DELIVERING` | The robot is at the destination handing over or unloading the package. | Arrival at the destination (`Destination Reached`). | Completion of delivery process (`Delivery Successful`). |
| **S5** | `RETURNING` | The robot is actively moving back toward the warehouse. | Delivery completion (`Delivery Successful`) OR critical battery event (`Critical Battery`). | Arrival at the warehouse (`Warehouse Reached`). |
