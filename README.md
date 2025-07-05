  # Low Voltage CascodeCurrent vs Conventional Current Mirror


This project presents the design, simulation, and comparison of a Low Voltage Cascode Current Mirror (LVCCM) 
and a Basic (Conventional) Current Mirror using LTspice

## Simple cascode current mirror
he conventional current mirror is simple in structure, using only two NMOS transistors. It offers ease of design and low power consumption, making it suitable for applications where precision is not critical. However, it suffers from low output resistance, typically in the tens of kilo-ohms, which makes it sensitive to variations in the output voltage. Additionally, its voltage headroom requirement is relatively high, approximately equal to the gate-source voltage (
 ) plus the saturation drain-source voltage (
 ), limiting its usability in low-voltage environments.
 # schematic
![Screenshot 2025-07-03 115715](https://github.com/user-attachments/assets/3ae72718-4e3f-44d0-ad52-0d0654cdde01)
# output 
![Screenshot 2025-07-03 125216](https://github.com/user-attachments/assets/2ec1b732-8d0e-4806-aa48-2447b7e9586e)

## LV cascode Current mirror
the low-voltage cascode current mirror uses four NMOS transistors and a biasing technique to achieve significantly higher output resistance—often in the hundreds of kilo-ohms or more—while still allowing for lower output voltage swing. This structure maintains excellent current replication accuracy due to reduced channel length modulation effects. Although it adds moderate design complexity and slightly increases power consumption, its ability to operate effectively in low-voltage scenarios makes it ideal for modern CMOS technologies. It is especially well-suited for analog circuits that require precise current sources, such as op-amps, ADCs, and biasing networks.
![Screenshot 2025-07-05 210725](https://github.com/user-attachments/assets/6ab8211a-5364-4a29-ab8f-4c9ccc638119)
![Screenshot 2025-07-05 210712](https://github.com/user-attachments/assets/c5353b65-1c7d-47f2-9696-c786e603f620)

![Screenshot 2025-07-05 210340](https://github.com/user-attachments/assets/a6edf337-26ef-4126-83f1-e93947362fcf)
