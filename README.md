## Overview

In analog and mixed-signal integrated circuits, generating a stable reference voltage against time, temperature, and supply variations is critical to ensuring precise system performance. This repository focuses on the design, simulation, and optimization of **Bandgap Reference (BGR)** circuits.

### How it Works
A Bandgap Reference achieves a zero-temperature-coefficient ($TC = 0$) voltage by canceling out two temperature-dependent components with opposite slopes:
* **PTAT (Proportional To Absolute Temperature):** Positive TC, typically derived from the thermal voltage difference ($\Delta V_{BE}$) between two bipolar transistors operating at different current densities.
* **CTAT (Complementary To Absolute Temperature):** Negative TC, derived from the base-emitter voltage ($V_{BE}$) of a bipolar junction transistor (BJT).

By precisely scaling and summing these two components, the circuit generates a stable reference voltage that remains virtually independent of temperature fluctuations over a wide operating range.

### Why Bandgap Reference Matters
Modern analog designs heavily rely on stable DC current and voltage references that exhibit high immunity to **PVT (Process, Voltage, and Temperature)** variations:
* **Biasing:** Crucial for setting precise tail currents in differential pairs, which directly impact gain and noise performance.
* **Data Converters:** Serves as the voltage baseline to define the exact full-scale range for ADCs and DACs.
* **Amplifiers:** Provides accurate common-mode voltages for Operational Amplifiers (Op-Amps).

### Modern Advancements
As technology scales, this project also explores **Low-Voltage Bandgap** topologies capable of operating under sub-1V supply voltages, meeting the stringent low-power requirements of modern energy-efficient IC designs.
