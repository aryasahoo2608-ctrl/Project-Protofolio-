# Project 1: Scale-Model Suspension Bridge Evaluation

## Aim
To design, construct, and evaluate a scale-model suspension bridge optimized to maximize structural efficiency (load-to-weight ratio) by effectively distributing tensile and compressive forces.

---

## Materials Required
- **Structural Elements:** Balsa wood strips (3 mm x 3 mm for trusses and towers), high-density cardboard (for the deck base).
- **Cables & Suspenders:** High-tensile braided nylon string or thin steel wire.
- **Anchorage & Fixtures:** Miniature eye-hooks, heavy wooden baseboard (for anchoring).
- **Adhesives:** Cyanoacrylate (Super Glue) or wood epoxy.
- **Testing Equipment:** S-hooks, lightweight plastic bucket, digital weighing scale, calibration weights (or sand/water).

---

## Experiment Steps
1. **Design & Layout:** Sketch a 2D blueprint of the suspension bridge. Define span length (L), tower height (H), and sag of the main cable (d).
2. **Tower & Deck Construction:** Build two identical towers using balsa wood with triangular truss design. Cut the deck to target span length.
3. **Cable Stringing:** Fix towers to baseboard. Run main suspension cables over towers and secure to anchorages. Attach vertical suspenders from cable to deck at equal intervals.
4. **Baseline Mass Measurement:** Weigh the completed bridge structure and record its self-weight (M_bridge).
5. **Load Testing:** Suspend bucket from center of deck using S-hook. Gradually add weights until structural failure occurs.
6. **Failure Recording:** Record total mass at failure point (M_load).

---

## Experimental Data

| Design Iteration                  | Bridge Mass (M_bridge) | Max Load Supported (M_load) | Primary Failure Point            |
|-----------------------------------|-------------------------|------------------------------|----------------------------------|
| Iteration 1 (Straight Towers)     | 120 g                  | 4,200 g                     | Tower buckling inward            |
| Iteration 2 (Truss-Reinforced)    | 135 g                  | 6,800 g                     | Main cable slippage at anchorage |
| Iteration 3 (Optimized Sag Ratio) | 140 g                  | 9,100 g                     | Mid-span suspender snap          |

---

## Analysis

Structural efficiency (n) is calculated using the load-to-weight ratio:

\[
n = \frac{M_{load}}{M_{bridge}}
\]

- **Iteration 1 Efficiency:** 4200 / 120 = **35.0**
- **Iteration 2 Efficiency:** 6800 / 135 = **50.3**
- **Iteration 3 Efficiency:** 9100 / 140 = **65.0**

---

## Conclusion
- Reinforcing towers with trusses improved stability and efficiency.
- Optimizing sag ratio and anchorage design yielded the highest efficiency (65.0).
- The primary limiting factor shifted from tower buckling → cable slippage → suspender snapping, showing progressive improvement in design iterations.
# Project 2: Closed-Loop Thermal Management System Evaluation

##  Aim
To design, construct, and analyze a functional closed-loop thermal management system simulating an automotive internal combustion engine cooling loop, and evaluate heat dissipation efficiency under varying fluid flow rates.

---

##  Materials Required
- **Heat Source:** 50 W ceramic heating element or adjustable immersion heater (simulating engine block)  
- **Heat Exchanger (Radiator):** Copper/aluminum multi-channeled liquid-to-air radiator core with 12V DC cooling fan  
- **Fluid Circulation:** 12V DC brushless submersible water pump (adjustable flow rate)  
- **Conduits & Sensors:** Clear silicone tubing (Ø = 8 mm), two DS18B20 waterproof temperature sensors, electronic liquid flow meter  
- **Control & Power:** Arduino Uno (data logging + PWM fan control), solid-state relay, 12V dual DC power supply  
- **Coolant:** Distilled water + 30% ethylene glycol mixture  

---

##  Experiment Procedure
1. **System Assembly:**  
   - Mount heat source inside insulated aluminum reservoir ("engine block").  
   - Connect reservoir outlet → radiator inlet via silicone tubing.  
   - Route radiator outlet → reservoir via water pump (closed loop).  

2. **Sensor Integration:**  
   - Place one sensor at engine block outlet (to radiator).  
   - Place second sensor at radiator outlet (back to engine).  
   - Install flow meter inline on cold-side plumbing.  

3. **Initialization:**  
   - Fill system with coolant mixture.  
   - Bleed air bubbles.  
   - Power Arduino for continuous temperature & flow logging.  

4. **Baseline Stabilization:**  
   - Turn on 50 W heat source.  
   - Run system with fan **off** until coolant stabilizes at **75℃**.  

5. **Flow Rate Testing:**  
   - Turn fan **on (max speed)**.  
   - Set pump to **low flow (1.0 L/min)**.  
   - Stabilize for 10 minutes.  
   - Record temperatures and flow rate.  

6. **Incremental Iterations:**  
   - Repeat step 5 at **medium (2.0 L/min)** and **high (3.0 L/min)** flow rates.  
   - Log stabilized thermal profiles.  

---

##  Experimental Data
Ambient air temperature: **25℃**

| Flow Rate Setting | Volumetric Flow Rate (Q) | Radiator Inlet Temp (Tin) | Radiator Outlet Temp (Tout) | Temperature Drop (ΔT) |
|-------------------|--------------------------|---------------------------|-----------------------------|-----------------------|
| Low Flow          | 1.0 L/min                | 72.4℃                     | 58.1℃                       | 14.3℃                 |
| Medium Flow       | 2.0 L/min                | 64.8℃                     | 54.2℃                       | 10.6℃                 |
| High Flow         | 3.0 L/min                | 61.2℃                     | 52.9℃                       | 8.3℃                  |

---

##  Analysis
The radiator heat rejection rate **P** is calculated using:

\[
P = \dot{m} \cdot C_p \cdot \Delta T
\]

Where:  
- \(\dot{m}\) = fluid mass flow rate (kg/s), derived from volumetric flow rate (Q) and coolant density (\(\rho = 1040 \, kg/m^3\))  
- \(C_p\) = specific heat capacity of coolant (~3600 J/kg·℃)  
- \(\Delta T\) = temperature differential (Tin - Tout)  

### Calculated Heat Rejection
- **Low Flow (1.0 L/min = 0.0173 kg/s):**  
  \(0.0173 \times 3600 \times 14.3 = 890.6 \, W\)  

- **Medium Flow (2.0 L/min = 0.0347 kg/s):**  
  \(0.0347 \times 3600 \times 10.6 = 1324.2 \, W\)  

- **High Flow (3.0 L/min = 0.0520 kg/s):**  
  \(0.0520 \times 3600 \times 8.3 = 1553.8 \, W\)  

---

##  Conclusion
- Increasing flow rate reduces the **temperature drop (ΔT)** across the radiator.  
- However, higher flow rates increase the **overall heat rejection capacity (P)**.  
- The system demonstrates effective thermal management, with optimal balance between flow rate and cooling efficiency.

# Project 3: Miniature Horizontal-Axis Wind Turbine Blade Evaluation

## Aim
To design, fabricate, and test a miniature horizontal-axis wind turbine (HAWT) blade assembly to evaluate the impact of blade pitch angles on aerodynamic efficiency and electrical power generation.

---

## Materials Required
- **Rotor Blades:** 3D-printed or hand-carved balsa wood blades (NACA 4412 airfoil, 15 cm length)
- **Generator:** Low-friction, high-efficiency 3V–6V DC hobby motor
- **Hub Assembly:** Custom rotor hub with variable pitch angle locking screws
- **Support Structure:** PVC/aluminum pipe tower (40 cm) on a wooden baseboard
- **Measurement & Load:** Digital multimeter, 100 Ω resistor, alligator clips
- **Wind Source:** Variable-speed household fan + digital anemometer

---

## Experiment Procedure
1. **Blade Configurations:** Prepare three sets of blades with pitch angles of 0°, 15°, and 30°.
2. **Tower Setup:** Mount generator and hub assembly with blades at chosen pitch.
3. **Circuit Assembly:** Connect generator output across 100 Ω resistor, measure voltage with multimeter.
4. **Wind Alignment:** Place fan 50 cm from hub, calibrate wind speed to 5.0 m/s.
5. **Data Collection:** Record steady voltage output at each pitch angle.
6. **Pitch Iterations:** Repeat for 15° and 30° blade pitch angles.

---

## Experimental Data

| Blade Pitch Angle | Voltage Output | Circuit Resistance | Current | Power Output |
|-------------------|----------------|--------------------|---------|--------------|
| 0° Pitch          | 0.22 V         | 100 Ω              | 2.2 mA  | 0.48 mW      |
| 15° Pitch         | 1.85 V         | 100 Ω              | 18.5 mA | 34.23 mW     |
| 30° Pitch         | 0.94 V         | 100 Ω              | 9.4 mA  | 8.84 mW      |

---

## Analysis
The electrical power output is calculated using:

\[
P = \frac{V^2}{R}
\]

- **0° Pitch:** \( \frac{0.22^2}{100} = 0.48 \, \text{mW} \)  
- **15° Pitch:** \( \frac{1.85^2}{100} = 34.23 \, \text{mW} \)  
- **30° Pitch:** \( \frac{0.94^2}{100} = 8.84 \, \text{mW} \)  

**Conclusion:** The optimal pitch angle for maximum power generation at 5.0 m/s wind velocity is **15°**, producing ~34 mW, which is significantly higher than both 0° and 30° configurations.

---

## Key Takeaways
- Blade pitch angle strongly influences turbine efficiency.  
- Too low (0°) or too high (30°) pitch reduces performance.  
- Moderate pitch (15°) balances aerodynamic lift and drag, maximizing power output.  

---

## Future Improvements
- Test at varying wind speeds (3–10 m/s).  
- Experiment with different airfoil profiles.  
- Scale up blade length for higher energy capture.
