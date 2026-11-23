# Implementation Plan

The project will be developed in stages. Later stages depend on the earlier ones working reliably.

## Stage 1 — Reliable drive system

**Goal:** Establish dependable control of the left and right motors.

Work items:
- Confirm that the motor and driver can operate in a controlled test.
- Record the power arrangement and control-pin mapping.
- Test forward, reverse, and stop behaviour.
- Test the motors separately before testing them together.

**Acceptance criteria:** The drive system responds consistently to requested commands, and the test setup is documented.

**Status:** Not achieved yet. See [Test Log](TEST-LOG.md).

## Stage 2 — Distance sensing

**Goal:** Read distance measurements from the HC-SR04 and record their behaviour.

Work items:
- Test the sensor independently.
- Compare readings at several measured distances.
- Record unstable or invalid readings.
- Decide how the obstacle response should behave.

**Acceptance criteria:** Readings are repeatable enough for the intended task, with limitations documented.

**Status:** Pending for this robot-car integration.

## Stage 3 — Obstacle-avoidance mode

**Goal:** Use distance readings to control the car around an obstacle.

Work items:
- Define a stop threshold based on tests.
- Define the response when an obstacle is detected.
- Test at low speed in a clear area.
- Record cases where the robot makes the wrong decision.

**Acceptance criteria:** The car detects an obstacle and responds in a repeatable way during documented trials.

**Status:** Planned.

## Stage 4 — Line-following mode

**Goal:** Follow a marked line using reflective sensors.

Work items:
- Select suitable line sensors.
- Test readings over the line and background.
- Decide sensor placement and calibration.
- Develop and test steering corrections.

**Acceptance criteria:** The car follows a defined test track repeatedly, with the track and sensor setup documented.

**Status:** Planned.

## Stage 5 — Wireless control

**Goal:** Control the car remotely using an ESP32-based wireless link.

Work items:
- Choose the communication method.
- Define a small command set, including stop.
- Test communication independently of the motors.
- Connect received commands to the shared motor-control layer.

**Acceptance criteria:** The car responds consistently and stops when a stop command is received or communication is lost.

**Status:** Planned.

## Stage 6 — Mode selection and integration

**Goal:** Combine the separate functions into one platform.

Work items:
- Add a mode-selection method.
- Ensure only the selected mode controls movement.
- Define priority rules for stop and fault conditions.
- Test mode switching and record unexpected behaviour.

**Acceptance criteria:** Each mode can be selected and tested without conflicting control commands.

**Status:** Planned.

## Stage 7 — Final documentation

Add only real evidence:
- Final wiring diagram
- Tested source code
- Component list and versions
- Photos of the actual build
- Test tables and known limitations
- Demonstration video, if available

The project should be described as complete only when the acceptance criteria for its claimed features have been met.
