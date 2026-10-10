# Li-Ion-Charger
Custom lithium ion charger that is small and does not blow up.

**The Problem** : In Indian market especially, TP4050 is available to charge lithium ion battery, but it sucks as it slowly damages the cell. But there are bigger alternatives which safely charge it. Buy those are bulky. This *Custom Li Ion charger* solves that.

![3D PCB](images/HERO_VIEW_PCB.webp)


# Features

1. 2A+ charging so you can charge with normal chargers.
2. Type C only.
3. Status LEDs (Red 🍒 - Charging, Green 🍏 - Charged)
4. Over Current protection with Mosfets

# BOM

| Ref | Value / Part | Description | Footprint | Qty |
|-----|--------------|-------------|-----------|-----|
| U1 | IP2312-4V35 | Switch-mode Li-ion charger IC, ESOP-8 | `easyeda2kicad:ESOP-8_L4.9-W3.9-P1.27-LS6.0-BL-EP` | 1 |
| U2 | DW01A | Battery protection IC, SOT-23-6 | `Package_TO_SOT_SMD:SOT-23-6` | 1 |
| Q1 | FS8205A | Dual N-channel MOSFET, SOT-23-6 | `Custom_Footprints:SOT-23-6_L2.9-W1.6-P0.95-LS2.8-BR` | 1 |
| L1 | 2.2 µH | Power inductor, ≥3A saturation | `Inductor_SMD:L_0805_2012Metric` | 1 |
| C1 | 22 µF | Ceramic capacitor, input decoupling | `Capacitor_SMD:C_0603_1608Metric` | 1 |
| C2 | 100 nF | Ceramic capacitor, DW01A bypass | `Capacitor_SMD:C_0603_1608Metric` | 1 |
| C3 | 100 nF | Ceramic capacitor, shield bypass | `Capacitor_SMD:C_0603_1608Metric` | 1 |
| C4 | 22 µF | Ceramic capacitor, output decoupling | `Capacitor_SMD:C_0603_1608Metric` | 1 |
| R1 | 1 kΩ | LED current limit (Red) | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R2 | 1 kΩ | LED current limit (Green) | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R3 | 68 kΩ | ICHG set resistor (≈2A) | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R4 | 1 kΩ | CS current sense resistor | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R5 | 5.1 kΩ | CC1 pull-down | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R6 | 5.1 kΩ | CC2 pull-down | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R7 | 1 kΩ | TEST pin resistor | `Resistor_SMD:R_0603_1608Metric` | 1 |
| R8 | 1 kΩ | VCC resistor for DW01A | `Resistor_SMD:R_0603_1608Metric` | 1 |
| D1 | LED_RED | Charging indicator | `LED_SMD:LED_0603_1608Metric` | 1 |
| D2 | LED_GREEN | Charge complete indicator | `LED_SMD:LED_0603_1608Metric` | 1 |
| FB1 | Ferrite bead | 120Ω @ 100MHz, shield filter | `Inductor_SMD:L_0603_1608Metric` | 1 |
| J1 | USB_C_Receptacle_PowerOnly_6P | USB-C power-only connector | `Connector_USB:USB_C_Receptacle_GCT_USB4135-GF-A_6P_TopMnt_Horizontal` | 1 |
| TH1 | 10 kΩ NTC | Thermistor for temperature sensing | `Resistor_SMD:R_0603_1608Metric` | 1 |
| TP1 | TestPoint | Bat+ | `TestPoint:TestPoint_Pad_D2.0mm` | 1 |
| TP2 | TestPoint | Bat− | `TestPoint:TestPoint_Pad_D2.0mm` | 1 |
| TP3 | TestPoint | Out+ | `TestPoint:TestPoint_Pad_D2.0mm` | 1 |
| TP4 | TestPoint | Out− | `TestPoint:TestPoint_Pad_D2.0mm` | 1 |

# Schematic 

![Schematic](images/S1.webp)
![Schematic](images/S2.webp)
![Schematic](images/S3.webp)
![Schematic](images/S4.webp)

# PCB 
![PCB](images/3D_VIEW_PCB.webp)
![PCB](images/HERO_VIEW_PCB.webp)
![PCB](images/3D_VIEW_PCB_B.webp)
![PCB](images/F.cu_PCB.webp)
![PCB](images/B.cu_PCB.webp)

# Credits 
Ki Cad for PCB design, downloaded some footprints through easy eda plugin (thanks to who ever made this). And used this for compression of screenshots (made by me btw).
https://ilovefilesbyhemanth.netlify.app/

# AI Usage 
Used AI for understanding datasheets and verifying components.

# Licence

Free to use gerbers and all, but not yet tested. Feel free to modify it. but don't burn your house :)

