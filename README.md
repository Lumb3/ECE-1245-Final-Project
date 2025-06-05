# 🔧 ECE-1245 Final Project

## 💡 Project Title: ThermoLight-Activated LED System

---

### 📘 Description

This project showcases a **ThermoLight-Activated LED System** using two comparator Op-Amps, a thermistor (temperature sensor), and a photoresistor (light sensor). It is designed to detect environmental conditions (light and temperature) and respond using LEDs.

---

### 🔑 Key Features

- **Red LED (Light Sensor - Photoresistor):**  
  Turns on in the dark to indicate a lighting issue.

- **White LED (Temperature Sensor - Thermistor):**  
  Turns on in cold conditions to indicate a temperature issue.

- **Blue LED (Combined Condition - NAND Logic):**  
  Connected to the outputs of the Red and White LEDs through two NAND gates, which replicate AND logic. This LED turns on *only* when **both** Red and White LEDs are on (i.e., dark **and** cold conditions — worst-case scenario).

---

### 🚀 System Logic

#### Comparator Logic:
- `If V⁺ > V⁻ → Output = 5V (LED ON)`  
- `If V⁺ < V⁻ → Output = 0V (LED OFF)`

#### Explanation:
Both the photoresistor and thermistor are connected to comparator Op-Amps through voltage dividers.  
- The **photoresistor circuit** uses a reference voltage (**V⁻**) of **2.2V**. If the voltage at **V⁺** (from the voltage divider) drops below this in the dark, the output is 5V, turning on the red LED.  
- The **thermistor circuit** uses a reference voltage (**V⁻**) of **2.0V** (can be adjusted by a potentiometer in the voltage divider). In cold conditions, the thermistor’s resistance rises, dropping the voltage at **V⁺**, causing the output to go high and turning on the white LED.

When both conditions are true (dark and cold), the red and white LEDs are both ON. Their outputs are fed into two NAND gates, which behave as an AND gate followed by a NOT gate — lighting up the **blue LED** only in the worst-case scenario.

📝 *Refer to the 1. Preliminary, 2. Critical, and 3. Final design reports for more details.*
---

### 📷 Images

> *(Note: V⁺ = Vp, V⁻ = Vn in diagrams)*

| Case 1: **Dark and Cold** | Case 2: **Bright and Warm (Best Case)** |
|---------------------------|-----------------------------------------|
| <img src="https://github.com/user-attachments/assets/bc770578-7713-4740-969c-a72ab7f5a08d" width="400" alt="Case 1: Dark and Cold" /> | <img src="https://github.com/user-attachments/assets/83c8aac8-4f73-4e1b-b9ea-aea87b87dfd3" width="400" alt="Case 2: Bright and Warm" /> |

---

### 🧪 LTspice Simulation

To simulate the circuit behavior, use **LTspice** from Analog Devices:

🔗 [Download LTspice](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html)

![LTspice Simulation](https://github.com/user-attachments/assets/528c2254-a97c-41c2-aee3-84eee54c8d0e)

---

🎥 **Circuit in Action:**  
[Watch the YouTube Demo](https://www.youtube.com/watch?v=bgkjT5ubVag)

---

🗓️ *Created for ECE-1245 Final Project*  
📅 **Date:** 2025-05-17
