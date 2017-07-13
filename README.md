*Copyright UBC Formula Electric 2017. All rights reserved.*

![TSDM_2017 - Rev. A 3D Render (Top)](https://github.com/UBCFormulaElectric/TSDM_2017-Board/blob/master/Photos%20%26%20Renderings/TSDM_2017%20-%20Rev.%20A%203D%20Rendering%20(Top).jpg)
*TSDM_2017 - Rev. A 3D Render (Top)*

# Overview

The Tractive System Discharge Module (TSDM_2017) discharges the tractive system in accordance with the 2017 Formula SAE rules. It uses two MOSFETs and a power resistor to discharge the repackaged inverter filtering capacitors below 60V in <1.5 seconds (to meet EV5.1.3). The power resistor is connected across the two poles of the tractive system whenever the AIR shutdown circuit is open, even when the vehicle is off.

# Features & Specifications

- The TSDM is separated into GLV (low-voltage) and tractive system (high-voltage) sections by a 10mm isolation boundary as per EV4.1.7. The GLV section contains the AIR shutdown circuit input and the tractive system section contains the MOSFETs and power resistor. The two halves are bridged by an optoisolated MOSFET driver.
- The board is mounted directly onto the power resistor using two M4 bolts. The power resistor is itself mounted to the inverter enclosure using two M3 studs and thermal compound. This design reduces the number of fasteners required for mounting and improves reliability by eliminating the use of additional wires and connectors.
- The AIR shutdown input uses a TE Micro MATE-N-LOK connector and is protected against reverse polarity by a Schottky diode and overcurrent by a PTC fuse. 
- The tractive system input uses a TE Mini-Universal MATE-N-LOK connector and is protected against reverse polarity by a 600V diode. Fusing is not allowed in the discharge circuit as per EV4.11.6.
- Each channel of the MOSFET driver has a red LED placed in series to provide a visual indicator of when the power resistor is disconnected from the tractive circuit.
- The power resistor is switched in and out of the system using two depletion-mode MOSFETs placed in series. The use of depletion-mode devices eliminates the need for conventional relays and allows the resistor to remain connected across the circuit when no power is applied to the system. The two MOSFETs are placed in series for redundancy, as a failure to discharge the tractive system quickly could pose a serious safety hazard when working on the vehicle.
