## Low Voltage Cascode Current Mirror vs Conventional Current Mirror

This project presents the **design**, **simulation**, and **performance comparison** of two commonly used current mirrors in analog circuit design:

- **Basic (Conventional) Current Mirror**
- **Low Voltage Cascode Current Mirror (LVCCM)**

---
  Tools Used: LTspice XVII
-

## What is a Current Mirror?
A current mirror is a circuit designed to **copy (or mirror)** a current from one active device to another, maintaining a **constant current** regardless of the loading. Current mirrors are fundamental in analog integrated circuits for **biasing**, **active loads**, and **signal processing**.

## Why Improve the Basic Mirror?
The basic current mirror, while simple, suffers from **low output resistance** and is sensitive to **channel length modulation**, which leads to **inaccurate current copying**, especially in low-voltage or high-gain environments.

To address these issues, **cascode and low-voltage cascode structures** are used to improve accuracy, **reduce output conductance**, and make the mirror suitable for **modern low-voltage CMOS technologies**.

---

##  Conventional cascode Curent Mirror

The conventional current mirror consists of **three NMOS transistors** (typically M1 and M2).
- Simple and compact
, Low power consumption
, Easy to implement
- Low output resistance (~ kΩ)
, Requires high voltage headroom: V<sub>GS</sub> + V<sub>DS(sat)</sub>
, Affected by channel length modulation (λ ≠ 0) ,
Limited precision for analog applications

##  Schematic
![Simple Mirror Schematic](https://github.com/user-attachments/assets/3ae72718-4e3f-44d0-ad52-0d0654cdde01)

##  Output
![Simple Mirror Output](./cascodemirror_outputw.png)

---

##  Low Voltage Cascode Current Mirror (LVCCM)

The LV Cascode mirror enhances the basic structure by adding **two more NMOS transistors** and a **biasing voltage**, forming a cascode configuration.

## Benefits
- **High output resistance** (~hundreds of kΩ)
- **Low voltage operation** (suited for modern CMOS tech)
- **more Accurate current replication**
- **Minimized channel length modulation**
##  **cons**:
- Higher design complexity
- Slightly increased power consumption


#  Schematic
![LVCCM Schematic](https://github.com/user-attachments/assets/6ab8211a-5364-4a29-ab8f-4c9ccc638119)

## Output Waveform
<img src="./wideswing_cascode_outputwaveform.png" alt="LVCCM Output" width="600" height="550"/>
---

##  Comparison Table

| Feature                        | Conventional Current Mirror | LV Cascode Current Mirror |
|-------------------------------|-----------------------------|----------------------------|
| **Structure**                 | 3 NMOS                      | 4 NMOS + Biasing           |
| **Output Resistance**         | Low ( ~kΩ)                 |             ~120kohms    |
| **Voltage Headroom Required** | High (V<sub>GS</sub> + 2V<sub>OV</sub>) | 2V<sub>OV</sub>   |
| **Channel Length Modulation** | Significant                 | Strongly suppressed        |
| **Current Replication Accuracy** | Moderate                | High                       |
| **Power Consumption**         | Low                         | Moderate                   |
| **Design Complexity**         | Simple                      | Moderate                   |
| **Applications**              | General-purpose, low-precision | Precision analog, low-voltage |

---

# Files Included

- `Simple_Mirror.asc` – LTspice schematic of basic current mirror
- `LV_Cascode_Mirror.asc` – LTspice schematic of cascode mirror
- Simulation results (screenshots above)
-**References** - Bezaad Razavi
---


