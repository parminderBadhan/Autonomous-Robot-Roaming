# Autonomous-Robot-Roaming robot 🤖

**📌 Overview**

This project implements a fully autonomous navigation system for the EEBot mobile robot using HCS12 (9S12) assembly language. The robot is capable of exploring and solving a maze by following a guide line, making decisions at intersections, detecting dead ends, and learning the correct path. Once the destination is reached, the robot retraces its steps back to the starting point — demonstrating basic memory, decision-making, and state machine design.

--------------------------
**🧭 Key Features:**

- 🧭 Line Following – Uses guider sensors to follow a maze path in real time.
- 🔀 Intersection Detection & Decision-Making – Recognizes L and T junctions and chooses a branch.
- 🔄 Dead-End Detection & Recovery – Detects obstacles via bumper sensors and performs a 180° turn.
- 🧠 Maze Learning – Records incorrect and correct branches to learn the maze structure.
- 🔙 Reverse Navigation – Retraces the correct path back to the start without error.
- 📊 System Feedback – Displays sensor readings, battery voltage, and current state on an LCD.

--------------------------

**⚙️ State Machine Design:**

The robot’s behavior is controlled by a finite state machine with the following states:

| State          | Description                                      |
|---------------|--------------------------------------------------|
| `START`       | Initial state, waits for bumper input to begin.  |
| `FWD`         | Follows the line forward.                        |
| `ALL_STP`     | Stops all motors.                                |
| `LEFT_TRN`    | Executes a left turn.                            |
| `RIGHT_TRN`   | Executes a right turn.                           |
| `REV_TRN`     | Performs a 180° turn when a dead end is detected.|
| `LEFT_ALIGN`  | Fine alignment left adjustment.                 |
| `RIGHT_ALIGN` | Fine alignment right adjustment.                |

--------------------------

**🔌 Hardware Components:**

- HCS12 Microcontroller (9S12C32)
- EEBot Platform with dual DC motors
- Line Guider Sensor Array (5 IR photodiodes)
- Bumper Sensors (Front and Rear)
- 16x2 LCD Display
- ADC (Analog-to-Digital Converter) for sensor readings



