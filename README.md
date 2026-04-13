## Single-Phase H-Bridge Inverter with SPWM Control
# Project Overview

This project focuses on the design, simulation, and harmonic optimization of a single-phase H-bridge power inverter. The system is implemented in MATLAB/Simulink using a custom SPWM (Sinusoidal Pulse Width Modulation) control algorithm. The primary goal was to achieve a high-quality output voltage waveform that meets international standards for grid connection.

# Key Technical Features

## Control Strategy
Sinusoidal PWM with a carrier frequency of $30\text{ kHz}$.
## Dead-Time Implementation
A robust safety interval was integrated directly into the MATLAB control function to prevent shoot-through currents in the H-bridge legs.
## Filter Design
A high-order LC low-pass filter ($L=20\text{ mH}$, $C=100\text{ }\mu\text{F}$) was designed and tuned to suppress switching noise and low-order harmonics.
## Harmonic Performance
Achieved a THD (Total Harmonic Distortion) of 2.57%, significantly surpassing the standard 5% requirement.

# System Components
Power Stage: MOSFET-based H-bridge inverter.  
Controller: Custom MATLAB Function block for gate signal generation.  
Load: Resistive load with output filtering.

# How to Run
Clone the repository:
git clone https://github.com/jovanovicnatalijaa/Inverter-Design
Open the .slx file in MATLAB/Simulink (R2024 or later recommended).
Ensure the powergui block is set to Discrete mode.

Run the simulation and observe the clean sine wave on the output Scope.
