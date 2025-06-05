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

#### Case 1: **Dark and Cold (Worst Case)**  
- The **photoresistor's resistance increases in the dark**, lowering the input voltage to the Op-Amp.
- The **thermistor's resistance increases when cold**, also lowering its input voltage.
- When both sensor voltages drop below their respective reference voltages, both Red and White LEDs turn on.
- The Blue LED is activated through the NAND gates when **both** of the above conditions are met.

---

### 📷 Images

> *(Note: V⁺ = Vp, V⁻ = Vn in diagrams)*

| Case 1: **Dark and Cold** | Case 2: **Bright and Warm (Best Case)** |
|---------------------------|-----------------------------------------|
| <img src="https://github.com/user-attachments/assets/3daacb60-1ff8-4983-b1aa-2d64ca3f7a41" width="400" alt="Case 1: Dark and Cold" /> | <img src="https://github.com/user-attachments/assets/a67d3e14-e22c-474d-87e0-79d8b2700535" width="400" alt="Case 2: Bright and Warm" /> |

---

### 🧪 LTspice Simulation

To simulate the circuit behavior, use **LTspice** from Analog Devices:

🔗 [Download LTspice](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html)

![LTspice Simulation](https://github.com/user-attachments/assets/528c2254-a97c-41c2-aee3-84eee54c8d0e)

---

🗓️ *Created for ECE-1245 Final Project*  
📅 **Date:** 2025-05-17
