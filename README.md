# Project-Protofolio-
# Scale-Model Suspension Bridge Evaluation

## Aim
To design, construct, and evaluate a scale-model suspension bridge optimized to maximize structural efficiency (load-to-weight ratio) by effectively distributing tensile and compressive forces.

---

## Materials Required

### Structural Elements
- Balsa wood strips (3 mm × 3 mm for trusses and towers)
- High-density cardboard (for the deck base)

### Cables & Suspenders
- High-tensile braided nylon string or thin steel wire

### Anchorage & Fixtures
- Miniature eye-hooks
- Heavy wooden baseboard (for anchoring)

### Adhesives
- Cyanoacrylate (Super Glue) or wood epoxy

### Testing Equipment
- S-hooks
- Lightweight plastic bucket
- Digital weighing scale
- Calibration weights (or sand/water)

---

## Experiment Procedure

### 1. Design & Layout
Sketch a 2D blueprint of the suspension bridge. Define the key dimensions:
- Span length (L)
- Tower height (H)
- Sag of the main cable (d)

### 2. Tower & Deck Construction
Build two identical towers using balsa wood, incorporating a triangular truss design for stability. Cut the deck to the target span length.

### 3. Cable Stringing
Fix the towers to the baseboard. Run the main suspension cables over the towers and secure them firmly to the anchorages at both ends. Attach vertical suspender strings from the main cable to the deck at equal intervals.

### 4. Baseline Mass Measurement
Weigh the completed bridge structure on the digital scale and record its self-weight (`Mbridge`).

### 5. Load Testing
Suspend the empty bucket from the center of the bridge deck using an S-hook. Gradually add weights (or sand) into the bucket until the structure undergoes structural failure (snapping of cables, buckling of towers, or deck failure).

### 6. Failure Recording
Record the total mass of the bucket and weights at the exact point of failure (`Mload`).

---

# Experimental Data

| Design Iteration | Bridge Mass (`Mbridge`) | Max Load Supported (`Mload`) | Primary Failure Point |
|---|---|---|---|
| Iteration 1 (Straight Towers) | 120 g | 4,200 g | Tower buckling inward |
| Iteration 2 (Truss-Reinforced Towers) | 135 g | 6,800 g | Main cable slippage at anchorage |
| Iteration 3 (Optimized Sag Ratio & Anchors) | 140 g | 9,100 g | Mid-span suspender snap |

---

# Analysis

The structural efficiency (`η`) of the bridge is calculated using the dimensionless load-to-weight ratio formula:

\[
\eta = \frac{M_{load}}{M_{bridge}}
\]

### Efficiency Calculations

- **Iteration 1 Efficiency:**  
  `4200 / 120 = 35.0`

- **Iteration 2 Efficiency:**  
  `6800 / 135 = 50.3`

- **Iteration 3 Efficiency:**  
  `9100 / 140 = 65.0`
  # Closed-Loop Thermal Management System Evaluation

## Aim
To design, construct, and analyze a functional closed-loop thermal management system simulating an automotive internal combustion engine cooling loop to evaluate heat dissipation efficiency under varying fluid flow rates.

---

## Materials Required

- **Heat Source:** 50 W ceramic heating element or adjustable immersion heater  
- **Heat Exchanger (Radiator):** Copper/aluminum multi-channel radiator with 12V DC cooling fan  
- **Fluid Circulation:** 12V DC brushless submersible water pump with adjustable flow rate  
- **Conduits & Sensors:**  
  - Clear silicone tubing (8 mm diameter)  
  - Two DS18B20 waterproof temperature sensors  
  - Electronic liquid flow meter  
- **Control & Power:**  
  - Arduino Uno  
  - Solid-state relay  
  - 12V dual DC power supply  
- **Coolant:** Distilled water mixed with 30% ethylene glycol  

---

# Experiment Procedure

## 1. System Assembly
Mount the heat source inside an insulated aluminum reservoir representing the engine block.

Connect:
- Reservoir outlet → Radiator inlet
- Radiator outlet → Water pump → Reservoir

This completes the closed cooling loop.

---

## 2. Sensor Integration
Install:
- `Tin` sensor at radiator inlet
- `Tout` sensor at radiator outlet

Place the flow meter inline within the cold-side plumbing.

---

## 3. Initialization
- Fill the system with coolant mixture.
- Remove all trapped air bubbles.
- Power on the Arduino for continuous temperature and flow-rate logging.

---

## 4. Baseline Stabilization
- Turn on the 50 W heater.
- Keep the radiator fan OFF.
- Allow the system to stabilize at approximately **75°C**.

---

## 5. Flow Rate Testing
- Turn radiator fan to maximum speed.
- Set pump flow rate to **1.0 L/min**.
- Allow stabilization for **10 minutes**.
- Record:
  - `Tin`
  - `Tout`
  - Flow rate (`Q`)

---

## 6. Incremental Iterations
Repeat the experiment for:
- **2.0 L/min**
- **3.0 L/min**

Record stabilized thermal values for each condition.

---

# Experimental Data

Ambient air temperature was maintained at **25°C**.

| Flow Rate Setting | Volumetric Flow Rate (Q) | Radiator Inlet Temp (Tin) | Radiator Outlet Temp (Tout) | Temperature Drop (ΔT) |
|------------------|--------------------------|----------------------------|------------------------------|------------------------|
| Low Flow         | 1.0 L/min                | 72.4°C                     | 58.1°C                       | 14.3°C                 |
| Medium Flow      | 2.0 L/min                | 64.8°C                     | 54.2°C                       | 10.6°C                 |
| High Flow        | 3.0 L/min                | 61.2°C                     | 52.9°C                       | 8.3°C                  |

---

# Analysis

The heat rejection rate of the radiator system is calculated using:

```math
P = \dot{m} \times C_p \times \Delta T


# Miniature Horizontal-Axis Wind Turbine Blade Evaluation

## Aim
To design, fabricate, and test a miniature horizontal-axis wind turbine (HAWT) blade assembly to evaluate the impact of blade pitch angles on aerodynamic efficiency and electrical power generation.

---

# Materials Required

- **Rotor Blades**
  - 3D-printed or hand-carved balsa wood aerodynamic blades
  - NACA 4412 airfoil profile design
  - Blade length: 15 cm

- **Generator**
  - Low-friction, high-efficiency 3V–6V DC hobby motor
  - Used as an alternator

- **Hub Assembly**
  - Custom central rotor hub
  - Variable manual pitch angle locking screws

- **Support Structure**
  - Rigid PVC or aluminum pipe tower base
  - Height: 40 cm
  - Mounted securely to a heavy wooden baseboard

- **Measurement & Load**
  - Digital multimeter
  - 100 Ω breadboard resistor
  - Connecting alligator clips

- **Wind Source**
  - Variable-speed household electric fan
  - Digital anemometer for measuring wind velocity

---

# Experiment Procedure

## 1. Blade Configurations
Prepare three sets of identical three-blade assemblies.

Adjust the static pitch angles to:
- 0°
- 15°
- 30°

for each testing round.

---

## 2. Tower Setup
Fix the generator to the top of the tower housing.

Attach the hub assembly with the 0° pitch blades onto the generator drive shaft.

---

## 3. Circuit Assembly
Connect the generator terminal wires across the 100 Ω load resistor.

Attach the digital multimeter leads across the resistor to measure output DC voltage.

---

## 4. Wind Alignment
Position the fan exactly 50 cm away from the turbine hub.

Ensure that the wind path is perpendicular to the rotor plane.

Use the anemometer to calibrate the fan speed to:

```text
5.0 m/s
```

---

## 5. Data Collection
Turn on the fan.

Allow the turbine rotor to spin up to its maximum stable angular velocity.

Record the steady voltage output displayed on the multimeter.

---

## 6. Pitch Angle Iterations
Power down the system.

Replace or adjust the blade assembly pitch angle to:
- 15°
- 30°

Repeat the measurements while maintaining the same wind velocity.

---

# Experimental Data

The following data logs show the electrical performance profiles across different blade pitch configurations at a constant wind velocity of 5.0 m/s.

| Blade Pitch Angle | Voltage Output | Circuit Resistance | Calculated Current | Total Power Output |
|------------------|----------------|-------------------|-------------------|-------------------|
| 0° Pitch | 0.22 V | 100 Ω | 2.2 mA | 0.48 mW |
| 15° Pitch | 1.85 V | 100 Ω | 18.5 mA | 34.23 mW |
| 30° Pitch | 0.94 V | 100 Ω | 9.4 mA | 8.84 mW |

---

# Analysis

The electrical power output generated by the wind turbine model is determined using Ohm’s Law and the Joule-Lenz power relationship:

```math
P = \frac{V^2}{R}
```

Where:
- `V` = Measured voltage drop across the load resistor (V)
- `R` = Constant load resistance (100 Ω)

---

# Calculated Values

## 0° Pitch Power Generation

```math
P = \frac{0.22^2}{100}
```

```text
P = 0.00048 W = 0.48 mW
```

---

## 15° Pitch Power Generation

```math
P = \frac{1.85^2}{100}
```

```text
P = 0.03423 W = 34.23 mW
```

---

## 30° Pitch Power Generation

```math
P = \frac{0.94^2}{100}
```

```text
P = 0.00884 W = 8.84 mW
```

---

# Detailed Analysis

## 0° Pitch
At 0° pitch, the blades produced minimal lift force because the airflow passed almost parallel to the blade surface.

As a result:
- Rotor rotation speed remained low
- Generator output voltage was very small
- Power generation was only:

```text
0.48 mW
```

This configuration was inefficient for extracting wind energy.

---

## 15° Pitch
The 15° blade pitch configuration produced the highest voltage and power output.

Reasons:
- Improved angle of attack
- Better aerodynamic lift
- Higher rotational speed
- Efficient energy transfer to the generator

Measured power output:

```text
34.23 mW
```

This indicates that 15° provided the optimal balance between lift and drag for the turbine system.

---

## 30° Pitch
At 30° pitch:
- Drag forces increased significantly
- Airflow separation likely occurred
- Rotor efficiency decreased

Although the blades still generated power, the output dropped compared to the 15° configuration.

Measured power output:

```text
8.84 mW
```

This shows that excessive pitch angles reduce turbine performance due to aerodynamic losses.

---

# Conclusion

The experiment confirms that blade pitch angle has a major effect on wind turbine efficiency and electrical power generation.

| Pitch Angle | Power Output |
|-------------|--------------|
| 0° | 0.48 mW |
| 15° | 34.23 mW |
| 30° | 8.84 mW |

The optimal blade pitch angle for this miniature HAWT model was:

```text
15°
```

because it achieved the maximum electrical power output at a constant wind velocity of 5.0 m/s.
