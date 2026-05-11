# ArduSub — Custom Frame for AUV Ai Apaec

This ArduPilot fork contains the ArduSub firmware modifications developed for the 
AUV Ai Apaec, an autonomous underwater vehicle built from scratch using 3D printing 
in Latin America.

## What does this fork modify?

A custom `SUB_FRAME_CUSTOM` was defined to match the unique actuator configuration 
of the Ai Apaec:

- 2 horizontal thrusters for surge and yaw
- 1 vertical thruster for depth control
- 2 servomotors configured as *elevons* for pitch and roll control

This configuration is not available in standard ArduSub frames, so direct 
source code modification was required to define the corresponding actuator mixing.

## Active branch

`version_0.2` — full manual control achieved in Stabilize mode with all axes 
responding correctly (surge, yaw, pitch and roll).

## Full project documentation

Complete documentation of the AUV Ai Apaec — hydrodynamic design, mechanical 
structure, control electronics, battery pack and waterproof sealing — is available at:

**[solid-mechanix.com/vehiculo-submarino-autonomo-aiapaec](https://solid-mechanix.com/vehiculo-submarino-autonomo-aiapaec/)**

The specific article covering the control electronics and this firmware:

**[Control Electronics for AUV: Raspberry Pi and Pixhawk](https://solid-mechanix.com/auv-ai-apaec-electronica-de-control-del-auv/)**

## Hardware

- Pixhawk (with modified ArduSub firmware)
- Raspberry Pi 5 (mission computer)
- 3x Bidirectional ESC 35A/6S
- 2x Waterproof servo D30
- Depth sensor MS5837
- GPS module UBX NEO-M9N
- 3D printed underwater thrusters

## Author

Pedro Boada — [Solid Mechanix](https://solid-mechanix.com) | Peru 🇵🇪
