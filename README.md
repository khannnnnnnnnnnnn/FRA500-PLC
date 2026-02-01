# Bottle Filling Automation System

A dual-line PLC-controlled bottle filling and inspection system with Modbus RTU communication.

## Overview

This project implements an automated beverage bottling system with two parallel production lines. Each line detects bottles, fills them with liquid, verifies fill levels, and packages qualified bottles while rejecting defective ones.

## System Features

- **Dual Production Lines**: Two identical conveyor systems operating independently
- **Three Operation Modes**:
  - **Manual Mode**: Direct I/O control and monitoring
  - **Semi-Auto Mode**: Start/stop control with automatic cycle completion
  - **Auto Mode**: Fully autonomous operation with minimal operator intervention
- **Quality Control**: Automatic liquid level verification and defective bottle rejection
- **Master-Slave Architecture**: Remote control via Modbus RTU protocol
- **HMI Interface**: Touch screen for monitoring, control, and parameter adjustment

## Hardware Components

### System 1 (Inputs: X0-X6, Outputs: Y0-Y6)
### System 2 (Inputs: X10-X16, Outputs: Y10-Y16)

Each system includes:
- Bottle detection sensors
- Fluid level sensor
- Conveyor motor
- Stopper mechanism
- Fluid filling valve
- Ejector systems (recycle bin & completed box)
- Status indicators (Run, Error lights)

## Process Flow

1. Bottles enter via conveyor belt
2. Stopper halts bottle at filling station
3. Liquid dispensed for preset duration
4. Bottle proceeds to inspection station
5. Level sensor verifies fill quality
6. Good bottles → packaging station
7. Defective bottles → recycle bin
8. System counts and tracks production statistics

## Project Files

- `Final_Project_Master.gx3` - Master PLC program (control & monitoring)
- `Final_Project_Slave.gx3` - Slave PLC program (production line control)
- `FRA500-Class_Project_2568.pdf` - Project specifications (Thai)

## Technical Implementation

- Function blocks for modular bottle detection system
- Configurable parameters (fill time, bottles per box)
- Production counters (good bottles, rejected bottles, cycles)
- Error handling with sensor validation
- Emergency stop and pause functionality

## Development Environment

- PLC Programming Software: GX Works3
- Communication Protocol: Modbus RTU
- HMI: Touch screen interface

---

**Course**: FRA500 - PLC
**Academic Year**: 2025
