# Multi-Range DC Voltage Measurement Circuit Using LM741

A hardware mini project designed to measure DC voltages over multiple selectable ranges using an LM741 operational amplifier.

## Overview

The project implements a multi-range DC voltage measurement circuit using an LM741 op-amp in a non-inverting configuration with negative feedback.

A rotary selector switch is used to select different gain-setting resistors, allowing the circuit to operate across multiple voltage measurement ranges.

## Measurement Ranges

- 1 V
- 5 V
- 10 V
- 13 V

## Components Used

- LM741 Operational Amplifier
- 10 kΩ Feedback Resistor
- Gain-setting Resistors
- Rotary Selector Switch
- Potentiometer
- Analog Voltmeter
- ±15 V DC Power Supply
- Breadboard
- Connecting Wires

## Working Principle

The LM741 is configured as a non-inverting amplifier.

The closed-loop gain is:

Av = 1 + (Rf / Rg)

where:

- Rf = Feedback resistor
- Rg = Selected gain-setting resistor

By changing Rg using the rotary selector switch, different amplifier gains are obtained.

## Simulation

The circuit was simulated using Proteus. The output voltage varied linearly with the input voltage and the simulated gains were close to the theoretical values.

## Hardware Implementation

The circuit was implemented on a breadboard and tested for different voltage ranges. The measured outputs showed good agreement with the theoretical calculations.

## Applications

- Low-voltage DC measurement
- Instrumentation systems
- Educational laboratory experiments
- Data acquisition systems
- Analog signal conditioning

## Project Contributors

- Kishore Kumar A
- Dravid Anand D

## Tools Used

- Proteus
- LM741 Op-Amp
- Breadboard Hardware Setup

## Project Type

Hardware Mini Project – Electronics for Analog Signal Processing
