# Power Supply With Voltage Regulator
##### Brian Costantino

### Overview
This repository featured 3 designs, a 12V DC Power Supply (PSU), a 12V Fixed Linear Voltage Regulator (FIX-VR) and an Adjustable Linear Voltage Regulator (ADJ-VR). Each of these 3 designs are used in the main sheet (Sheet 1). The main module takes a 155V (60 Hz) AC input, and outputs two steady 12V DC supply voltages, one for each of the regulators. To utilize either of these regulator modules, follow the usage outlined in the following section.

### Usage
Both devices are to be imported as hierarchical blocks. The sheets <em>\<FIX-VR\></em> and <em>\<ADJ-VR\></em> in the main design file <em>PowerSupplyWithVoltageRegulator.dch</em> represent the fixed and adjustable linear voltage regulators respectively. These sheets can be copied and pasted into your project, and imported as hierarchical blocks.

#### Fixed Regulator
To utilize the fixed regulator module, no changes need to be made to the schematics. Keep in mind, the L7812CV (regulator used in this design) produces a fixed 12V output, which cannot be changed without replacing it. If your project requires a non 12V supply voltage, you should opt for the adjustable regulator. Otherwise, as described above, import the sheet <em>\<FIX-VR\></em> to add it to your design.

#### Adjustable Regulator
On the other hand, when utilizing the adjustable regulator module, the output can be changed simply by replacing a resistor. The variable resistor RV, in sheet <em>\<ADJ-VR\></em> can be calculated using the following formula, where R1 is a constant 240 Ohms and Vref = 1.25V for the LM317P adjustable regulator.

Vout = Vref*(1+(RV/R1))

Letting RV = 2064 Ohms, we achieve an output voltage of 12V, however this can be changed to meet other supply voltage requirements. For example, to achieve a 5V DC output, replace RV with a 720 Ohm resistor. [This page](https://circuitdigest.com/calculators/lm317-resistor-voltage-calculator) is helpful when calculating the variable resistance for an adjustable linear regulator with a 1.25V reference voltage (like the LM317P used here). Then, as described above, import the sheet <em>\<ADJ-VR\></em> to add it to your design.

#### Datasheets
The following list contains refernces to the datasheets of each unique part used in these designs, as well as the total number of occurrences throughout each block.
- Adjustable Voltage Regulator \[1x\] - [LM317P](https://datasheets.diptrace.com/st_micro/CD00000455.pdf)
- Fixed Voltage Regulator \[1\] - [L7812CV](https://datasheets.diptrace.com/st_micro/CD00000444.pdf)
- Resistors \[2\]- [ALSR01](https://datasheets.diptrace.com/vishay/alsralvr.pdf)
- Capacitors \[6\]- [NEH220](https://datasheets.diptrace.com/nte/nev_neh.pdf)
- Diodes \[2\]- [1N4532](https://datasheets.diptrace.com/philips-nxp/1N4531.pdf)
- Transformer \[1\]- [166E12](https://datasheets.diptrace.com/transformers/5c0018-19.pdf)
- Rectifier \[1\] - [DBL202G](https://datasheets.diptrace.com/diodes_bridge/DBL201G%20SERIES_J15.pdf)