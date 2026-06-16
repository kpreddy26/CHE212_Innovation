# CHE212 Innovation Project
# Natural Convection Analysis of Enhanced Cylindrical Fins

This repository contains the experimental methodology, analytical calculations, and thermal profiles for the **CHE212 Innovation Project (Group 19)**. The project investigates the transient and steady-state thermal behavior of conventional solid fins compared against smart Phase Change Material (PCM)-embedded hollow fins under natural convection.

## 📌 Project Objectives
* Design and construct a vertical cylindrical fin test-rig utilizing automated data acquisition.
* Integrate an organic PCM (candle wax, $T_m \approx 55^\circ\text{C}$) to act as a passive thermal energy storage core.
* Evaluate spatial temperature decay along the fin length to determine efficiency ($\eta_f$) and effectiveness ($\epsilon_f$).
* Characterize transient heating and cooling kinetics to assess thermal stabilization performance.

---

## 🛠️ Experimental Setup & Instrumentation
* **Extended Surface:** Aluminum Rods (Length $\approx 180\text{ mm}$, Diameter $\approx 10\text{ mm}$).
* **Thermal Core:** Paraffin Candle Wax ($55^\circ\text{C}$ phase transition threshold).
* **Heat Source:** 12V DC Cartridge Heater powered by a constant-voltage DC Power Supply.
* **Sensors & DAQ:** 5 Spatially distributed K-type Thermocouples multiplexed to an Arduino Data Logger.

---

## 📊 Key Findings & Parameters
* **Fin Performance:** Both configurations match 1D exponential temperature decay models, achieving a steady-state **Fin Efficiency $\approx 83\%$** and a **Fin Effectiveness $\approx 60$**.
* **Thermal Buffering Capability:** The wax-filled fin demonstrated distinct phase-change latent heat plateaus between $50^\circ\text{C} - 55^\circ\text{C}$, resulting in a **13% longer cooling duration**. 
* **Application Focus:** While conventional fins maximize raw steady-state heat dissipation, PCM-enhanced configurations function as excellent thermal buffers to smooth out rapid temperature fluctuations in electronics or battery cooling systems.

---

## ⚙️ Sources of Experimental Deviation
To optimize future iterations, the following parameter vectors were identified for refinement:
1. Neglected radiative heat transfer losses in basic convection equations.
2. Variable contact resistance between the thermocouple beads and the aluminum surface.
3. Minor air pocket voids formed during the liquid-state wax filling process.
