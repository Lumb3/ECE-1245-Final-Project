# 🔧 ECE-1245 Final Project

## 💡 Project Title: ThermoLight-Activated LED System

---

### 📘 Description

This project implements a **ThermoLight-Activated LED System** using two comparator Op-Amps, a thermistor (temperature sensor), and a photoresistor (light sensor). The final LED turns **ON** only when it is **too dark** or **too cold**. When conditions are bright and warm, the LED stays **OFF**.

---

### 🔑 Key Features

- Uses a **thermistor** and **photoresistor** to monitor environment  
- **Three LEDs:**  
  - Two show individual sensor states  
  - One final LED controlled by a **NAND gate** lights up if either condition is bad  
- Circuit analysis with node-voltage method and optimal resistor selection  
- Comparator Op-Amps output 0V or 5V depending on sensor voltages  

---

### 🛠️ Tools Used

- **LTspice** for simulation and validation  
- Hardware components:  
  - Thermistor  
  - Photoresistor  
  - 2 Comparator Op-Amps  
  - 5 Resistors  
  - 3 LEDs  
  - NAND Gate  
  - 3.3V Power Supply  

---

### 🚀 System Logic

Two cases are analyzed:

#### Case 1: Dark and Cold (Worst Case)  

The photoresistor's resistance increases in darkness, lowering the voltage at the Op-Amp input. The comparator outputs 5V if the sensor voltage is below the reference voltage (**V⁻**), turning the LED on. Similar logic applies to the thermistor.  

Ideal comparator output:  
- If V⁺ > V⁻ → Output = 5V  
- If V⁺ < V⁻ → Output = 0V  

The NAND gate combines outputs to control the final LED.

---

### 📷 Images
(Note that V⁺ -> Vp, V⁻ -> Vn)

**Case 1: Dark and Cold**  


  <img src="https://github.com/user-attachments/assets/3daacb60-1ff8-4983-b1aa-2d64ca3f7a41" width="500" alt="Case 1: Dark and Cold" /><br/>


**Case 2: Bright and Warm (Best Case)**  


  <img src="https://github.com/user-attachments/assets/a67d3e14-e22c-474d-87e0-79d8b2700535" width="500" alt="Case 2: Bright and Warm" /><br/>


---

### 🧪 LTspice Simulation

**Worst Case (Dark and Cold):**  


  <img src="https://github.com/user-attachments/assets/72d0fac1-5c99-44b5-8bc2-2cf6aed9d2e0" width="600" alt="LTspice Simulation Worst Case" /><br/>


**Best Case (Bright and Warm):**  


  <img src="https://github.com/user-attachments/assets/344780c3-9fb3-46f9-9d56-d7d71f0719e2" width="600" alt="LTspice Simulation Best Case" /><br/>


---

🗓️ *Created for ECE-1245 Final Project*  
📅 **Date:** 2025/05/17
