# Test Log

Only observed test results belong here. A planned test must not be marked as passed.

## Test 001 — Initial motor-driver integration

**Date:** Not recorded  
**Status:** Failed / unresolved

### Purpose

Attempt to make one DC geared motor rotate using an Arduino Uno and an L298N motor driver.

### Setup recorded

| Item | Recorded configuration |
|---|---|
| Controller | Arduino Uno |
| Motor driver | L298N |
| Motor connection | Motor connected to OUT1 and OUT2 |
| Control inputs | Arduino D7 to IN1; Arduino D8 to IN2 |
| Power connection | Battery-holder positive to the driver's 12V terminal |
| Ground | Battery-holder negative to L298N GND; Arduino GND shared with driver GND |
| Jumper caps | Builder reported that the three jumper caps were installed |

The battery type, measured supply voltage, and measured motor-terminal voltage were not recorded.

### Observed result

The motor did not rotate during the attempted test. A basic Arduino motor-control test was also tried without a successful movement result.

### What this result tells us

- The attempted setup did not produce motor movement.
- The cause has not been isolated.
- It does not, by itself, prove that the Arduino, driver, motor, or battery holder is defective.

### What is not yet verified

- Actual supply voltage under load
- Whether the motor itself operates independently with a suitable verified supply
- Whether the driver is producing the expected output
- Whether the control signals reach the driver as intended

No specific component is labelled defective because the available evidence does not establish that.

## Future test records

| Test | Purpose | Completion evidence |
|---|---|---|
| Motor-only check | Establish whether the motor can run independently | Recorded result and supply details |
| Driver output check | Establish whether the driver switches the motor outputs | Recorded output measurement |
| Controller signal check | Confirm control signals are being generated | Serial output or measured signal |
| Distance sensor check | Record HC-SR04 readings at known distances | Small table of readings |
| Line sensor check | Compare readings over line and background | Calibration table |
| Wireless link check | Confirm commands are received correctly | Command log |
| Integration test | Confirm each mode controls the same drive system | Repeatable demonstration and notes |

A test is complete only when the setup and result are recorded. Do not fill in missing measurements from memory.
