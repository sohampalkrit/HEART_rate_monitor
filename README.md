# Heart Rate Monitor

## Table of Contents
- [Introduction](#introduction)
- [Functionality](#functionality)
- [Printed Circuit Board](#printed-circuit-board)
- [Enclosure Design](#enclosure-design)
- [Contributors](#contributors)

## Introduction
An electrocardiogram (ECG) is a diagnostic technique used to analyze the heart’s electrical activity by detecting the signals generated during each heartbeat through electrodes placed on the skin. The voltage difference between the right arm and left arm is amplified, incorporating a feedback mechanism through the right leg. ECG leads measure these voltages from the right arm, left arm, and right leg.  

The signal amplitude typically ranges from 0.001 mV to 100 mV (average ~1 mV) and spans a frequency range of 0.01 Hz to 250 Hz. Amplifying such a weak signal is challenging due to interference from multiple sources such as noise, power line interference, RF interference, electrode contact noise, stray capacitance, and motion-induced artifacts.  

In this project, I designed and implemented an **analog signal conditioning circuit** to amplify and filter the ECG signal using only fundamental electronic components such as resistors, capacitors, and operational amplifiers. The system provides clean ECG waveform acquisition suitable for heart rate monitoring.  

The block diagram below illustrates the various stages of the signal conditioning system implemented in the design.  
<img src="ECG_circuit_diagram.png" alt="ECG circuit diagram">

The circuit was simulated and verified using **LTSpice** and **Multisim** prior to PCB design and implementation.

## Functionality
The Heart Rate Monitor provides the following key features:
- Real-time heart rate detection and display.  
- Simple and user-friendly operation.  
- High accuracy through analog filtering and noise suppression.  
- Adjustable filtering parameters for different test scenarios.  
- Data logging capability for further analysis.  
- Fully documented design and workflow for ease of replication.  

## Printed Circuit Board
The PCB for the Heart Rate Monitor was **designed by me using EasyEDA**. To ensure minimal interference and compact design, I used a **4-layer PCB** structure consisting of two signal layers, one ground layer, and one power layer.  

The layout integrates the **ESP32 Dev Module** directly on the same PCB, reducing the need for external wiring. The display and sensor connections are routed internally within the PCB.  

After fabrication, all components were **hand-soldered**. To simplify troubleshooting and replacement, I used **IC bases** and **JST connectors** for modularity and reusability.  

<img src="Media/real PCB.png" alt="Printed Circuit Board Design" width="300">

## Enclosure Design
The **enclosure was designed using SolidWorks CAD software** to provide both protection and accessibility. It features a **removable top lid**, allowing easy access for component replacement or upgrades.  

Ventilation holes are strategically placed for proper airflow and heat dissipation. The top panel hosts the **display, filter-tuning knobs**, and **indicator LEDs**, while the **power switch**, **adapter input**, and **3.5mm electrode jack** are positioned on the sides for convenient use.  


## Contributors
- **Soham Palkrit** – Circuit Design, Simulation, PCB Design (EasyEDA), and Enclosure Modeling.  

