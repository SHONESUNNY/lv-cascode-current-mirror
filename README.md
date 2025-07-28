# 🔄 Low Voltage Cascode Current Mirror vs Conventional Current Mirror

This project presents the **design**, **simulation**, and **performance comparison** of two commonly used current mirrors in analog circuit design:

- ✅ **Basic (Conventional) Current Mirror**
- ✅ **Low Voltage Cascode Current Mirror (LVCCM)**

Both circuits are implemented and simulated using **LTspice** to analyze their performance across key analog parameters.

---

## 📚 Theoretical Background

### 📌 What is a Current Mirror?
A current mirror is a circuit designed to **copy (or mirror)** a current from one active device to another, maintaining a **constant current** regardless of the loading. Current mirrors are fundamental in analog integrated circuits for **biasing**, **active loads**, and **signal processing**.

### ⚠️ Why Improve the Basic Mirror?
The basic current mirror, while simple, suffers from **low output resistance** and is sensitive to **channel length modulation**, which leads to **inaccurate current copying**, especially in low-voltage or high-gain environments.

To address these issues, **cascode and low-voltage cascode structures** are used to improve accuracy, **reduce output conductance**, and make the mirror suitable for **modern low-voltage CMOS technologies**.

---

## 🔧 Simple (Conventional) Current Mirror

The conventional current mirror consists of **two NMOS transistors** (typically M1 and M2).

### ✅ Advantages
- Simple and compact
- Low power consumption
- Easy to implement

### ❌ Limitations
- Low output resistance (~tens of kΩ)
- Requires high voltage headroom: V<sub>GS</sub> + V<sub>DS(sat)</sub>
- Affected by channel length modulation (λ ≠ 0)
- Limited precision for analog applications

### 📷 Schematic
![Simple Mirror Schematic](https://github.com/user-attachments/assets/3ae72718-4e3f-44d0-ad52-0d0654cdde01)

### 📊 Output
![Simple Mirror Output](https://github.com/user-attachments/assets/2ec1b732-8d0e-4806-aa48-2447b7e9586e)

---

## ⚙️ Low Voltage Cascode Current Mirror (LVCCM)

The LV Cascode mirror enhances the basic structure by adding **two more NMOS transistors** and a **biasing voltage**, forming a cascode configuration.

### ✅ Benefits
- **High output resistance** (~hundreds of kΩ to MΩ)
- **Low voltage operation** (suited for modern CMOS tech)
- **Accurate current replication**
- **Minimized channel length modulation**
- Ideal for precision analog circuits

### ❌ Trade-offs
- Higher design complexity
- Slightly increased power consumption

### 📷 Schematic & Outputs

#### 🖼️ Schematic
![LVCCM Schematic](https://github.com/user-attachments/assets/6ab8211a-5364-4a29-ab8f-4c9ccc638119)

#### 📈 Output Waveform
![LVCCM Output](https://github.com/user-attachments/assets/c5353b65-1c7d-47f2-9696-c786e603f620)

#### 🔍 Zoomed-in Analysis
![LVCCM Zoomed Output](https://github.com/user-attachments/assets/a6edf337-26ef-4126-83f1-e93947362fcf)

---

## 📊 Comparison Table

| Feature                        | Conventional Current Mirror | LV Cascode Current Mirror |
|-------------------------------|-----------------------------|----------------------------|
| **Structure**                 | 2 NMOS                      | 4 NMOS + Biasing           |
| **Output Resistance**         | Low (10s of kΩ)             | High (100s of kΩ – MΩ)     |
| **Voltage Headroom Required** | High (V<sub>GS</sub> + V<sub>DS(sat)</sub>) | Low (better for LV CMOS)   |
| **Channel Length Modulation** | Significant                 | Strongly suppressed        |
| **Current Replication Accuracy** | Moderate                | High                       |
| **Power Consumption**         | Low                         | Moderate                   |
| **Design Complexity**         | Simple                      | Moderate                   |
| **Applications**              | General-purpose, low-precision | Precision analog, low-voltage |

---

## 📁 Files Included

- `Simple_Mirror.asc` – LTspice schematic of basic current mirror
- `LV_Cascode_Mirror.asc` – LTspice schematic of cascode mirror
- Simulation results (screenshots above)

---

## 📌 Conclusion

The **Low Voltage Cascode Current Mirror** significantly improves over the conventional current mirror in terms of output resistance, accuracy, and voltage compliance. It is an essential component in precision analog and low-voltage integrated circuit design.

---

**🛠️ Tools Used:** LTspice XVII

**🧠 Contributors:** [Your Name or GitHub ID]