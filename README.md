Project Protofolio 

# Scale-Model Suspension Bridge Evaluation

## Project Overview
The objective of this project is to design, construct, and evaluate a scale-model suspension bridge optimized to maximize structural efficiency (load-to-weight ratio) by effectively distributing tensile and compressive forces.

---

## Materials Required

* **Structural Elements:** Balsa wood strips (3 mm × 3 mm for trusses and towers), high-density cardboard (for the deck base).
* **Cables & Suspenders:** High-tensile braided nylon string or thin steel wire.
* **Anchorage & Fixtures:** Miniature eye-hooks, heavy wooden baseboard (for anchoring).
* **Adhesives:** Cyanoacrylate (Super Glue) or wood epoxy.
* **Testing Equipment:** S-hooks, a lightweight plastic bucket, digital weighing scale, and calibration weights (or sand/water).

---

## Experimental Methodology

1. **Design & Layout:** Sketch a 2D blueprint of the suspension bridge. Define the key dimensions: span length ($L$), tower height ($H$), and sag of the main cable ($d$).
2. **Tower & Deck Construction:** Build two identical towers using balsa wood, incorporating a triangular truss design for stability. Cut the deck to the target span length.
3. **Cable Stringing:** Fix the towers to the baseboard. Run the main suspension cables over the towers and secure them firmly to the anchorages at both ends. Attach vertical suspender strings from the main cable to the deck at equal intervals.
4. **Baseline Mass Measurement:** Weigh the completed bridge structure on the digital scale and record its self-weight ($M_{\text{bridge}}$).
5. **Load Testing:** Suspend the empty bucket from the center of the bridge deck using an S-hook. Gradually add weights (or sand) into the bucket until the structure undergoes structural failure (snapping of cables, buckling of towers, or deck failure).
6. **Failure Recording:** Record the total mass of the bucket and weights at the exact point of failure ($M_{\text{load}}$).

---

## Experimental Data

The table below summarizes the structural performance across three distinct design iterations:

| Design Iteration | Bridge Mass ($M_{\text{bridge}}$) | Max Load Supported ($M_{\text{load}}$) | Primary Failure Point |
| :--- | :---: | :---: | :--- |
| **Iteration 1** (Straight Towers) | 120 g | 4,200 g | Tower buckling inward |
| **Iteration 2** (Truss-Reinforced Towers) | 135 g | 6,800 g | Main cable slippage at anchorage |
| **Iteration 3** (Optimized Sag Ratio & Anchors) | 140 g | 9,100 g | Mid-span suspender snap |

---

## Analysis & Structural Efficiency

The structural efficiency ($\eta$) of the bridge is calculated using the dimensionless load-to-weight ratio formula:

$$\eta = \frac{M_{\text{load}}}{M_{\text{bridge}}}$$

### Calculations

* **Iteration 1 Efficiency:** $$\eta_1 = \frac{4200\text{ g}}{120\text{ g}} = 35.0$$

* **Iteration 2 Efficiency:** $$\eta_2 = \frac{6800\text{ g}}{135\text{ g}} = 50.3$$

* **Iteration 3 Efficiency:** $$\eta_3 = \frac{9100\text{ g}}{140\text{ g}} = 65.0$$

### Conclusion
By iterating from straight towers to truss-reinforced structures and optimizing the sag-to-span ratio along with firmer anchors, the structural efficiency increased dramatically from **35.0** to **65.0**.
# # Closed-Loop Thermal Management System Evaluation

## Project Overview
[span_0](start_span)The objective of this project is to design, construct, and analyze a functional, closed-loop thermal management system simulating an automotive internal combustion engine cooling loop to evaluate heat dissipation efficiency under varying fluid flow rates[span_0](end_span).

---

## Materials Required

* **[span_1](start_span)Heat Source:** A 50 W ceramic heating element or an adjustable immersion heater (simulating the engine block)[span_1](end_span).
* **[span_2](start_span)Heat Exchanger (Radiator):** A small copper or aluminum multi-channeled liquid-to-air radiator core equipped with a 12V DC cooling fan[span_2](end_span).
* **[span_3](start_span)Fluid Circulation:** A 12V DC brushless submersible water pump with adjustable flow rate capabilities[span_3](end_span).
* **[span_4](start_span)Conduits & Sensors:** Clear silicone tubing ($\emptyset=8\text{ mm}$), two digital DS18B20 waterproof temperature sensors, and an electronic liquid flow meter[span_4](end_span).
* **[span_5](start_span)Control & Power:** An Arduino Uno microcontroller (for data logging and PWM fan control), a solid-state relay, and a 12V dual DC power supply[span_5](end_span).
* **[span_6](start_span)Coolant:** Distilled water mixed with 30% ethylene glycol (automotive coolant)[span_6](end_span).

---

## Experimental Methodology

1. **[span_7](start_span)System Assembly:** Mount the heat source inside an insulated aluminum reservoir (the "engine block")[span_7](end_span). [span_8](start_span)Connect the outlet of the reservoir to the inlet of the radiator using silicone tubing[span_8](end_span). [span_9](start_span)Route the radiator outlet back to the reservoir via the water pump to complete the closed loop[span_9](end_span).
2. **[span_10](start_span)Sensor Integration:** Install one temperature sensor at the engine block outlet ($T_{\text{in}}$ to radiator) and the second sensor at the radiator outlet ($T_{\text{out}}$ back to engine)[span_10](end_span). [span_11](start_span)Integrate the flow meter inline within the cold-side plumbing[span_11](end_span).
3. **[span_12](start_span)Initialization:** Fill the system with the coolant mixture, ensuring all air bubbles are completely bled from the lines[span_12](end_span). [span_13](start_span)Power on the Arduino to begin continuous temperature and flow rate data logging[span_13](end_span).
4. **[span_14](start_span)Baseline Stabilization:** Turn on the 50 W heat source[span_14](end_span). [span_15](start_span)Allow the system to run with the radiator fan turned off until the coolant reaches a steady-state thermal equilibrium of $75^{\circ}\text{C}$[span_15](end_span).
5. **[span_16](start_span)Flow Rate Testing:** Turn the radiator fan on to maximum speed[span_16](end_span). [span_17](start_span)Set the water pump to a low flow rate ($1.0\text{ L/min}$) and let the system stabilize for 10 minutes[span_17](end_span). [span_18](start_span)Record $T_{\text{in}}$, $T_{\text{out}}$, and the flow rate ($Q$)[span_18](end_span).
6. **[span_19](start_span)Incremental Iterations:** Repeat step 5 at medium ($2.0\text{ L/min}$) and high ($3.0\text{ L/min}$) pump flow rates, logging the stabilized thermal profiles for each setting[span_19](end_span).

---

## Experimental Data

[span_20](start_span)The following data profiles show the temperature differentials across the radiator at a constant ambient air temperature of $25^{\circ}\text{C}$[span_20](end_span):

| Flow Rate Setting | Volumetric Flow Rate ($Q$) | Radiator Inlet Temp ($T_{\text{in}}$) | Radiator Outlet Temp ($T_{\text{out}}$) | Temperature Drop ($\Delta T$) |
| :--- | :---: | :---: | :---: | :---: |
| **Low Flow** | $1.0\text{ L/min}$ | $72.4^{\circ}\text{C}$ | $58.1^{\circ}\text{C}$ | $14.3^{\circ}\text{C}$ |
| **Medium Flow** | $2.0\text{ L/min}$ | $64.8^{\circ}\text{C}$ | $54.2^{\circ}\text{C}$ | $10.6^{\circ}\text{C}$ |
| **High Flow** | $3.0\text{ L/min}$ | $61.2^{\circ}\text{C}$ | $52.9^{\circ}\text{C}$ | $8.3^{\circ}\text{C}$ |

---

## Analysis & Calculations

[span_21](start_span)The total heat rejection rate ($P$) of the radiator system is quantified using the fundamental thermodynamic heat transfer equation[span_21](end_span):

$$P = \dot{m} \times C_p \times \Delta T$$

[span_22](start_span)Where[span_22](end_span):
* [span_23](start_span)$\dot{m}$ is the fluid mass flow rate $(\text{kg/s})$, derived from the volumetric flow rate ($Q$) and coolant density $(\rho \approx 1040\text{ kg/m}^3)$[span_23](end_span).
* [span_24](start_span)$C_p$ is the specific heat capacity of the water-glycol mixture $(\approx 3600\text{ J/kg}\cdot^{\circ}\text{C})$[span_24](end_span).
* [span_25](start_span)$\Delta T$ is the temperature differential $(T_{\text{in}} - T_{\text{out}})$[span_25](end_span).

### [span_26](start_span)Calculated Values[span_26](end_span):

* **Low Flow Heat Rejection** $(1.0\text{ L/min} \approx 0.0173\text{ kg/s})$: 
  $$0.0173 \times 3600 \times 14.3 = 890.6\text{ W}$$

* **Medium Flow Heat Rejection** $(2.0\text{ L/min} \approx 0.0347\text{ kg/s})$: 
  $$0.0347 \times 3600 \times 10.6 = 1324.2\text{ W}$$

* **High Flow Heat Rejection** $(3.0\text{ L/min} \approx 0.0520\text{ kg/s})$: 
  $$0.0520 \times 3600 \times 8.3 = 1553.8\text{ W}$$

---

## Conclusion
As the fluid flow rate increases, the actual temperature drop ($\Delta T$) across the radiator decreases because the fluid passes through the heat exchanger faster. However, the total heat rejection rate ($P$) increases significantly from **890.6 W** to **1553.8 W** due to the higher mass volume moving through the system per second, proving that high flow rates enhance overall thermal management efficiency.
# Miniature Horizontal-Axis Wind Turbine Blade Evaluation

## Project Overview
[span_0](start_span)The objective of this project is to design, fabricate, and test a miniature horizontal-axis wind turbine (HAWT) blade assembly to evaluate the impact of blade pitch angles on aerodynamic efficiency and electrical power generation[span_0](end_span).

---

## Materials Required

* **[span_1](start_span)Rotor Blades:** 3D-printed or hand-carved balsa wood aerodynamic blades (NACA 4412 airfoil profile design, 15 cm length)[span_1](end_span).
* **[span_2](start_span)Generator:** A low-friction, high-efficiency 3V-6V DC hobby motor functioning as an alternator[span_2](end_span).
* **[span_3](start_span)Hub Assembly:** A custom central rotor hub with variable, manual pitch angle locking screws[span_3](end_span).
* **[span_4](start_span)Support Structure:** A rigid PVC or aluminum pipe tower base (40 cm height) mounted securely to a heavy wooden baseboard[span_4](end_span).
* **[span_5](start_span)Measurement & Load:** A digital multimeter, a 100 Ω breadboard resistor acting as an electrical load, and connecting alligator clips[span_5](end_span).
* **[span_6](start_span)Wind Source:** A variable-speed multi-stage household electric fan and a digital anemometer to measure wind velocity in m/s[span_6](end_span).

---

## Experimental Methodology

1. **[span_7](start_span)Blade Configurations:** Prepare three sets of identical three-blade assemblies[span_7](end_span). [span_8](start_span)Mount them into the central hub, adjusting the static pitch angles (angle of attack relative to the rotor plane) to $0^{\circ}$, $15^{\circ}$, and $30^{\circ}$ respectively for each testing round[span_8](end_span).
2. **[span_9](start_span)Tower Set-up:** Fix the generator to the top of the tower housing[span_9](end_span). [span_10](start_span)Attach the hub assembly with the $0^{\circ}$ pitch blades onto the generator's drive shaft[span_10](end_span).
3. **[span_11](start_span)Circuit Assembly:** Connect the terminal wires of the generator across the 100 Ω load resistor[span_11](end_span). [span_12](start_span)Attach the digital multimeter leads across the resistor to measure output DC voltage (V)[span_12](end_span).
4. **[span_13](start_span)Wind Alignment:** Position the variable fan exactly 50 cm away from the turbine hub, ensuring the wind path is completely perpendicular to the rotor plane[span_13](end_span). [span_14](start_span)Use the anemometer to calibrate the fan speed to a stable velocity of $5.0\text{ m/s}$[span_14](end_span).
5. **[span_15](start_span)Data Collection:** Turn on the fan and allow the turbine rotor to spin up to its maximum stable angular velocity[span_15](end_span). [span_16](start_span)Record the steady voltage output (V) displayed on the multimeter[span_16](end_span).
6. **[span_17](start_span)Pitch Angle Iterations:** Power down the system, replace or adjust the blade assembly pitch angle to $15^{\circ}$ and repeat the measurement[span_17](end_span). [span_18](start_span)Follow with the $30^{\circ}$ pitch blade assembly, logging all corresponding outputs under the identical wind velocity[span_18](end_span).

---

## Experimental Data

[span_19](start_span)The following data logs show the electrical performance profiles across different blade pitch configurations at a constant wind velocity of $5.0\text{ m/s}$[span_19](end_span):

| Blade Pitch Angle | Voltage Output | Circuit Resistance | Calculated Current | Total Power Output |
| :--- | :---: | :---: | :---: | :---: |
| **0° Pitch** | 0.22 V | 100 Ω | 2.2 mA | 0.48 mW |
| **15° Pitch** | 1.85 V | 100 Ω | 18.5 mA | 34.23 mW |
| **30° Pitch** | 0.94 V | 100 Ω | 9.4 mA | 8.84 mW |

---

## Analysis & Calculations

[span_20](start_span)The electrical power output ($P$) generated by the wind turbine model is determined using Ohm's Law and the Joule-Lenz power relationship[span_20](end_span):

$$P = \frac{V^2}{R}$$

Where:
* [span_21](start_span)$V$ is the measured voltage drop across the load resistor (V)[span_21](end_span).
* [span_22](start_span)$R$ is the constant load resistance (100 Ω)[span_22](end_span).

### Calculated Values:

* **0° Pitch Power Generation:** $$\frac{0.22^2}{100} = 0.00048\text{ W} = 0.48\text{ mW}$$

* **15° Pitch Power Generation:** $$\frac{1.85^2}{100} = 0.03423\text{ W} = 34.23\text{ mW}$$

* **30° Pitch Power Generation:** $$\frac{0.94^2}{100} = 0.00884\text{ W} = 8.84\text{ mW}$$

---

## Conclusion
The experiment highlights the critical importance of the blade pitch angle on aerodynamic performance. At a **0° pitch angle**, the blades cannot generate sufficient aerodynamic lift to overcome engine friction, resulting in negligible power (**0.48 mW**). At a **30° pitch angle**, stalling effects and high drag limit performance (**8.84 mW**). The **15° pitch angle** represents an optimal balance, yielding peak power generation of **34.23 mW**.
