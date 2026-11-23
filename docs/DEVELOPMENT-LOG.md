# Development Log

This file records the work completed so far and the lessons learned. Exact dates were not recorded for the early experiments, so no dates have been invented.

## Initial goal

The original idea was to develop a single car with four capabilities: obstacle avoidance, line following, wireless control, and combined operation through selectable modes.

## Early hardware work

The first development period involved working with and learning about:

- Arduino Uno and basic sketch uploading
- L298N motor-driver terminals and control inputs
- DC geared motors and motor polarity
- Jumper caps and driver enable connections
- Shared ground between the controller and motor driver
- Soldering wires to motor terminals
- The signal path from a microcontroller to a motor driver

The builder reported spending roughly 25 days on this attempt. The exact day-by-day timeline was not maintained.

## Motor integration attempt

The motor and L298N were connected for a basic movement test. The Arduino control pins were connected to the driver's input pins, and a common ground was used between the Arduino and driver.

The motor did not rotate during the test. Basic test code was also tried, but the system still did not produce the expected movement.

The cause remains unknown. Without measurements that isolate the power supply, driver, motor, and control signals, it would not be accurate to say that a particular component was definitely defective.

## What was learned

The attempt provided practical exposure to reading motor-driver labels, understanding the signal path, using a shared ground, working with motor wires and soldering, separating a design into subsystems, and documenting a failed test without claiming success.

## Current position

The integrated robot is not complete. Reliable motor movement has not yet been demonstrated, so the higher-level modes remain planned.

The next development effort should establish a known and repeatable motor-control result before adding more features.

## Update format

For future entries, use this structure:

### YYYY-MM-DD — Short title

**Goal:** What was being tested?

**Setup:** Which board and components were used?

**Result:** What happened?

**Conclusion:** What can be said from this test, and what remains uncertain?

**Next step:** What will be tested next?
