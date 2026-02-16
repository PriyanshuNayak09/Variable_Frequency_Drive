# ⚡ V/F Controlled Induction Motor Drive using PWM & SVPWM (MATLAB/Simulink)

## 📌 Project Overview
This project models a **Variable Frequency Drive (VFD)** for a three-phase induction motor using MATLAB/Simulink.  
It implements **V/f control** and compares:

- Sinusoidal PWM (SPWM)  
- Space Vector PWM (SVPWM)

The simulation demonstrates how voltage is adjusted proportionally with frequency to control motor speed.

---

## 🎯 Objectives
- Build a rectifier–inverter VFD model  
- Implement constant V/f control  
- Compare SPWM and SVPWM  
- Observe motor speed response  
- Smooth inverter output using LC filter  

---

## 🧰 Tools Used
- MATLAB  
- Simulink  
- Simscape Electrical  

---

## 🏗️ System Architecture

Main blocks in the model:

- Three-phase source  
- Diode rectifier  
- DC link  
- Inverter  
- PWM/SVPWM controller  
- LC filter  
- Induction motor  

---

## 🖥️ Main Simulink Model

![Main Model](docs/main_model.png)

---

## 🔁 PWM Modulation Subsystem

![PWM Subsystem](docs/pwm_subsystem.png)

This subsystem generates:
- Frequency signal  
- Modulation index  
- 3-phase sine references  
- PWM/SVPWM switching pulses  

---

## ⚙️ V/f Control Principle

\[
V \propto f
\]

When frequency decreases from **50 Hz → 10 Hz**,  
the inverter voltage also decreases proportionally.

This keeps motor flux constant and prevents saturation.

---

## 📉 Simulation Inputs

| Parameter | Value |
|----------|------|
Initial frequency | 50 Hz  
Final frequency | 10 Hz  
Step time | 1 s  
Load torque | 10 Nm  
PWM frequency | 5 kHz  

---

## 📊 Simulation Results

### 🟢 Rotor Speed
![Rotor Speed](docs/rotor_speed.png)

---

### 🔵 Three-Phase Voltage
![Voltage](docs/phase_voltage.png)

---

### 🟡 Frequency Input
![Frequency](docs/frequency.png)

---

## 🔄 SPWM vs SVPWM

| Feature | SPWM | SVPWM |
|--------|------|------|
Voltage utilization | Lower | Higher |
THD | Higher | Lower |
Efficiency | Moderate | Better |

SVPWM gives smoother output and better DC bus utilization.

---

## 🔧 Output Filter Used

Series RL:
- R = 0.5 Ω  
- L = 0.1 mH  

Shunt C:
- C = 600 µF  

This reduces switching ripple.

---

## 📁 Project Structure (Inside Repository)
VFD_Simulink_Project/
│
├── VFD.slx # Main Simulink model
├── PWM_Modulation.slx # PWM subsystem model
├── README.md # Documentation
│
└── docs/ # Images used in README
├── main_model.png
├── pwm_subsystem.png
├── rotor_speed.png
├── phase_voltage.png
└── frequency.png


## ▶️ How to Run
1. Open MATLAB  
2. Open `VFD.slx`  
3. Run simulation  
4. Change frequency step values  
5. Toggle between PWM & SVPWM  
6. Observe scopes  

---

## 🧠 Learning Outcomes
- V/f motor control  
- PWM & SVPWM comparison  
- Induction motor modeling  
- Power electronics simulation  

---

## 🚀 Future Improvements
- Closed-loop speed control  
- Field-oriented control  
- Hardware prototype  
- EV motor drive integration  

---

## 👨‍💻 Author
Priyanshu Nayak  
B.Tech Electrical Engineering  

---

## 📜 License
For academic and educational use.