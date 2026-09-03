# Multi-Range DC Voltage Measurement Circuit Using LM741

## 📌 Project Overview

This project presents the design and implementation of a **Multi-Range DC Voltage Measurement Circuit using an LM741 (IC 741) operational amplifier**.

The circuit uses a non-inverting amplifier configuration with negative feedback and provides selectable voltage measurement ranges of:

* **1 V**
* **5 V**
* **10 V**
* **13 V**

A rotary selector switch is used to select different gain-setting resistors, allowing the circuit to operate in different measurement ranges.

The circuit was validated through both **Proteus simulation** and **hardware implementation**.

---

## 🎯 Aim

To design and implement a multi-range DC voltage measurement circuit using an operational amplifier (IC 741) in a non-inverting configuration with negative feedback, providing selectable measurement ranges of **1 V, 5 V, 10 V and 13 V**, and to validate the circuit through simulation and hardware testing.

---

## 🛠️ Components Required

| Component              | Specification            |    Quantity |
| ---------------------- | ------------------------ | ----------: |
| Operational Amplifier  | IC 741                   |           1 |
| Potentiometer          | 10 kΩ                    |           1 |
| Resistor (R2)          | 15 kΩ                    |           1 |
| Feedback Resistor (R1) | 10 kΩ                    |           1 |
| Gain-setting Resistors | 1 kΩ, 7 kΩ, 10 kΩ, 13 kΩ |      1 each |
| Rotary Selector Switch | 4-position               |           1 |
| Analog Voltmeter       | 0–20 V DC                |           1 |
| DC Power Supply        | ±15 V, 1 A               |           1 |
| Breadboard / PCB       | —                        |           1 |
| Connecting Wires       | —                        | As required |

---

## ⚙️ Working Principle

The circuit uses the **LM741 operational amplifier in a non-inverting configuration with negative feedback**.

The DC input voltage is applied to the non-inverting terminal of the op-amp through resistor R2.

The output is fed back to the inverting terminal through the feedback resistor R1. The inverting terminal is connected to ground through one of the selectable gain-setting resistors using the rotary switch.

The closed-loop voltage gain of a non-inverting amplifier is:

```text
Av = 1 + Rf / Rg
```

where:

* `Rf` = Feedback resistor (R1)
* `Rg` = Selected gain-setting resistor

The output voltage is:

```text
Vout = Av × Vin
```

Changing the selected resistor changes the gain of the amplifier and therefore allows different voltage measurement ranges.

---

## 🔄 Measurement Ranges

| Range | Selected Resistor (Rg) |  Gain | Output Relation    |
| ----- | ---------------------: | ----: | ------------------ |
| 1 V   |                   1 kΩ | 11.00 | Vout = 11.00 × Vin |
| 5 V   |                   7 kΩ |  2.43 | Vout = 2.43 × Vin  |
| 10 V  |                  10 kΩ |  2.00 | Vout = 2.00 × Vin  |
| 13 V  |                  13 kΩ |  1.77 | Vout = 1.77 × Vin  |

The meter scale is calibrated for each selected range so that the amplified output corresponds to the actual input voltage range.

---

## 🔌 Circuit Operation

1. The DC input voltage is applied using the potentiometer.
2. The input is fed to the non-inverting terminal (pin 3) of the IC 741 through R2.
3. The output is fed back to the inverting terminal (pin 2) through R1.
4. The inverting terminal is connected to ground through one of the gain-setting resistors using the rotary switch.
5. Negative feedback provides the required closed-loop voltage gain.
6. Selecting different resistors changes the gain.
7. The amplified output is measured using the analog voltmeter.
8. Input voltage is varied and readings are recorded for each selected range.

---

## 💻 Simulation

The circuit was simulated using **Proteus**.

The simulated output varied linearly with the input voltage for the selected ranges, and the obtained gains matched the theoretical calculations.

### Simulation Results

| Range |    Rg |     Vin | Simulated Vout |  Gain |
| ----- | ----: | ------: | -------------: | ----: |
| 1 V   |  1 kΩ | 0.100 V |         1.10 V | 11.00 |
| 5 V   |  7 kΩ | 1.000 V |         2.43 V |  2.43 |
| 10 V  | 10 kΩ | 1.000 V |         2.00 V |  2.00 |
| 13 V  | 13 kΩ | 1.000 V |         1.77 V |  1.77 |

---

## 🔧 Hardware Implementation

The circuit was implemented on a **breadboard** and tested using different voltage ranges.

The measured output values showed good agreement with the theoretical/reference values.

### Hardware Results

| Range | Applied Vin | Measured Vout | Calculated Vout | Error |
| ----- | ----------: | ------------: | --------------: | ----: |
| 1 V   |     0.000 V |        1.09 V |          1.10 V | 0.91% |
| 5 V   |     1.000 V |        2.41 V |          2.43 V | 0.82% |
| 10 V  |     1.000 V |        1.98 V |          2.00 V | 1.00% |
| 13 V  |     1.000 V |        1.77 V |          1.77 V | 1.13% |

---

## 📊 Results

The multi-range DC voltage measurement circuit was successfully designed, implemented and tested.

The circuit provided selectable measurement ranges of:

```text
1 V → 5 V → 10 V → 13 V
```

The simulation and hardware results confirmed the operation of the designed circuit.

---

## ✅ Advantages

* Simple and low-cost design
* Selectable measurement ranges using a rotary switch
* High input impedance
* Good stability due to negative feedback
* Easy calibration
* Wide range of applications

---

## ⚠️ Limitations

* Accuracy depends on resistor tolerance and op-amp offset
* Output is limited by the supply voltage and op-amp swing
* Manual range selection is required
* Suitable only for DC voltage measurement

---

## 📍 Applications

* Low-voltage DC measurement systems
* Educational and laboratory measurement setups
* Instrumentation and data acquisition systems
* Analog signal conditioning applications

---

## 📁 Project Structure

```text
Multi-Range-DC-Voltage-Measurement/
│
├── README.md
│
├── docs/
│   └── Multi_Range_DC_Voltage_Measurement_Circuit_Report.pdf
│
├── circuit/
│   └── circuit-diagram.png
│
├── simulation/
│   ├── proteus-simulation.png
│   └── Multi_Range_Voltage_Measurement.pdsprj
│
└── hardware/
    ├── hardware-setup.jpg
    ├── final-circuit.jpg
    └── output-reading.jpg
```

*The files shown in the structure should be added only if they are available.*

---

## 👥 Project Contributors

### Kishore Kumar A

Department of Instrumentation Engineering
Madras Institute of Technology Campus
Anna University, Chennai

### Dravid Anand D

Department of Instrumentation Engineering
Madras Institute of Technology Campus
Anna University, Chennai

---

## 👩‍🏫 Project Guide

**Dr. Sabitha Ramakrishnan**
Professor
Department of Instrumentation Engineering
Madras Institute of Technology Campus
Anna University

---

## 📄 Project Report

The complete project report is available in the [`docs`](docs/) folder.

---

## 🏷️ Project Type

**Hardware Mini Project**

**Subject:** Electronics for Analog Signal Processing – 2

**Project:** Multi-Range DC Voltage Measurement Circuit Using LM741
