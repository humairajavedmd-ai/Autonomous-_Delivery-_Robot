# Delivery Robot Requirements

| Requirement ID | Description | Priority |
| :--- | :--- | :--- |
| **R1** | The robot shall initialize in the IDLE state upon startup and remain idle until a delivery request is received. | High |
| **R2** | Upon receiving a delivery request while in the IDLE state, the robot shall start navigating toward the designated destination. | High |
| **R3** | While navigating, if an obstacle is detected, the robot shall temporarily halt normal navigation and transition to obstacle-avoidance mode. | High |
| **R4** | Upon clearing an obstacle during navigation, the robot shall resume navigation toward the destination. | High |
| **R5** | Upon arriving at the designated destination, the robot shall initiate the package delivery process. | High |
| **R6** | Upon completion of the package delivery, the robot shall begin returning to the warehouse. | High |
| **R7** | If the battery level drops below a critical threshold during navigation (either to the destination or back to the warehouse), the robot shall halt its current mission and immediately return to the warehouse. | Critical |
| **R8** | Upon arriving at the warehouse, the robot shall transition to the IDLE state and wait for new delivery requests. | Medium |
| **R9** | The robot shall not transition directly from the IDLE state to the DELIVERING state without first receiving a request and navigating to the destination. | High |
| **R10** | The robot shall not enter the DELIVERING state directly from the AVOIDING_OBSTACLE state. | High |
