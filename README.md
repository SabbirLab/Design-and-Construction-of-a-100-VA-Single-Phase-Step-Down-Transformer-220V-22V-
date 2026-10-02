# ⚡ 100 VA Single-Phase Step-Down Transformer (220V/22V)

Design, construction, and performance testing of a 100 VA, 50 Hz single-phase step-down transformer.

**Course:** Energy Conversion Laboratory (EEE206)
**Department:** Electrical & Electronics Engineering, United International University
**Team:** Group 03

![Final transformer](images/final_transformer.jpg)

---

## 📌 Overview

This project covers the full workflow of building a transformer: calculating design parameters (turns, current ratings, VA capacity), winding and assembling the core, and verifying performance with standard laboratory tests (no-load, load, rated-load, short-circuit).

## 🔧 Specifications

| Parameter | Value |
|---|---|
| Rating | 100 VA |
| Primary voltage | 220 V AC |
| Secondary voltage | 22 V AC |
| Frequency | 50 Hz |
| Rated primary current | 0.455 A |
| Rated secondary current | 4.55 A |
| Type | Single-phase, step-down |
| Core | Laminated iron core |
| Cooling | Natural air |

## 🧰 Components

- Laminated iron core and bobbin (former)
- Enamel-coated copper wire (primary and secondary windings)
- Insulation paper / tape, core clamps / screws
- Varnish (insulation, noise and vibration reduction)
- Terminal block and connecting wires
- Variac, multimeters, wattmeter, ammeter, load resistor / load bank
- Digital storage oscilloscope (UNI-T UTD2072CL)

## 🏗️ Construction

1. Selected a laminated core to reduce eddy-current losses.
2. Wound the **primary (220 V)** first on the bobbin.
3. Wound the **secondary (22 V)** on top to minimize leakage flux.
4. Insulated between layers to prevent turn-to-turn shorts.
5. Assembled the core, clamped it, and applied varnish for insulation, reduced humming, and thermal stability.

## 🧪 Tests Performed

| Test | Purpose | Key readings |
|---|---|---|
| No-load | Core losses, voltage ratio | Vp = 220 V, Vs = 22 V |
| Load (100 Ω resistive) | Voltage, current, power under load | See report |
| Rated load | Behavior at design limit | Vp = 220 V, Vs = 20 V, Ip = 0.4 A, Is = 4.35 A, Pin = 70 W, Pout = 66 W |
| Short-circuit | Copper losses, equivalent impedance | Vsc = 26 V, Isc = *(add verified value)* |

The secondary output was verified on an oscilloscope as a clean sinusoid at ≈ 50 Hz.

![Oscilloscope output](images/oscilloscope_output.jpg)

## 📊 Results

**Voltage regulation**

```
VR = (V_no-load − V_full-load) / V_full-load × 100
   = (22 − 20) / 20 × 100 ≈ 10 %
```

**Efficiency**

```
η = P_out / P_in × 100 = 66 / 70 × 100 ≈ 94.3 %
```

| Metric | Result |
|---|---|
| Voltage regulation | ≈ 10 % |
| Efficiency (rated load) | ≈ 94.3 % |
| Output frequency | ≈ 50 Hz |

## 🛡️ Safety Precautions

- Supply voltage applied gradually using a variac to avoid inrush current.
- Reduced voltage only during the short-circuit test.
- Tight, secure connections; instruments with suitable ranges.
- Transformer kept within rated limits and cooled between tests.

## 💡 Applications and Limitations

**Applications:** power supplies, battery chargers, control circuits.
**Limitations:** natural air cooling limits power density; manual winding can cause slight flux imbalance.

## 📁 Repository Structure

```
.
├── README.md
├── report/
│   └── Energy_project_report.pdf
└── images/
    ├── final_transformer.jpg
    ├── oscilloscope_output.jpg
    ├── rated_load_test.jpg
    └── short_circuit_test.jpg
```

## 👥 Team (Group 03)

| Name | ID |
|---|---|
| Hasan Rayhan Rabbe | 0212410026 |
| Sabbir Ahmed | 0212410034 |
| Ashikur Rahman | 0212410009 |
| Md. Mahbubur Rahman | 0212410013 |
| Faysal Mahmud | 0212410014 |
| Jannatun Mawa Simu | 0212410012 |

## 📄 Full Report

See [`report/Energy_project_report.pdf`](report/Energy_project_report.pdf).

## 📜 License

Released for educational purposes under the [MIT License](LICENSE).
