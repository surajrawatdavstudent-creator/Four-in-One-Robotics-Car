# System Architecture

The robot is planned as one platform with separate operating modes. Each mode uses the same drive system but has a different source of control.

## Main subsystems

| Subsystem | Responsibility | Current state |
|---|---|---|
| Controller | Read inputs and select actions | Arduino Uno used in initial experiments |
| Drive electronics | Control motor direction and speed | L298N test attempted; result unresolved |
| Drive mechanism | Move the chassis | DC geared motors available; reliable movement not demonstrated |
| Distance sensing | Measure distance to obstacles | HC-SR04 available; car integration pending |
| Line sensing | Detect a contrasting track | Planned; sensor selection pending |
| Wireless input | Send movement commands | Planned; ESP32-based approach under consideration |
| Mode manager | Prevent conflicting commands | Planned |

## Intended control flow

1. The selected mode determines which input source is active.
2. The controller reads sensor values or a wireless command.
3. The controller converts the input into a movement decision.
4. The motor driver receives direction and speed-control signals.
5. The controller repeats the process.

The motor-control layer should be shared by all modes. Obstacle avoidance, line following, and wireless control should call the same movement functions rather than each implementing unrelated motor logic.

## Mode concepts

### Obstacle avoidance
The distance sensor provides a reading. The controller can decide whether to continue, stop, or choose another direction. The final turning method has not been selected.

### Line following
Reflective sensors can distinguish a marked line from its background. The controller uses the sensor pattern to decide whether to move straight or correct its direction. Sensor count, spacing, and calibration remain to be determined.

### Wireless control
A separate controller sends movement requests. The vehicle-side controller receives a command and passes it to the shared motor-control layer. The communication method is not final.

### Combined operation
A mode-selection mechanism chooses which source controls the car. Only one mode should issue movement commands at a time. Stop behaviour should take priority over movement commands.

## Proposed firmware organisation

This is a proposed structure, not a description of finished code:

```text
firmware/
├── main/
├── motor_control/
├── obstacle_avoidance/
├── line_following/
└── wireless_control/
```

## Open design decisions

- Final chassis and motor arrangement
- Verified motor power and control setup
- Line-sensor type and placement
- Obstacle response and steering method
- Wireless protocol and controller arrangement
- Mode-selection interface
- Power distribution design

These decisions will be updated when supported by actual tests.
