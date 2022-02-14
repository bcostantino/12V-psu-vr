# Power Supply With Voltage Regulator
###### Brian Costantino

#### Overview
This repository featured 3 designs, a 12V DC Power Supply (PSU), a 12V Fixed Linear Voltage Regulator (FIX-VR) and an Adjustable Linear Voltage Regulator (ADJ-VR). Each of these 3 designs are used in the main sheet (Sheet 1). The main module takes a 155V (60 Hz) AC input, and outputs two steady 12V DC supply voltages, one for each of the regulators. To utilize either of these regulator modules, follow the usage outlined in the following section.

#### Usage
Both devices are to be imported as hierarchical blocks. The sheets __\<FIX-VR\>__ and __\<ADJ-VR\>__ in the main design file __PowerSupplyWithVoltageRegulator.dch__ represent the fixed and adjustable linear voltage regulators respectively.

##### Fixed Regulator
To utilize the fixed regulator module, no changes need to be made to the schematics. Keep in mind, the specs are fixed and the 12V output cannot be changed once this module is manufactured. 

##### Adjustable Regulator
On the other hand, when utilizing the adjustable regulator module, the output can be changed simply by replacing a resistor. The variable resistor, RV, in sheet ADJ-VR can be selected using the following formula, where R1 is a constant 240 Ohms and Vref = 1.25V for the LM317P adjustable regulator.

Vout = Vref*(1+(RV/R1))

With RV = 2064 Ohms, the output voltage is 12V, however this can be changed to meet other supply voltage requirements.

#### Datasheets
- Adjustable Voltage Regulator - [LM317P](https://datasheets.diptrace.com/st_micro/CD00000455.pdf)
- Fixed Voltage Regulator - [L7812CV](https://datasheets.diptrace.com/st_micro/CD00000444.pdf)
- Resistors - [ALSR01](https://datasheets.diptrace.com/vishay/alsralvr.pdf)
- Capacitors - [NEH220](https://datasheets.diptrace.com/nte/nev_neh.pdf)
- Diodes - [1N4532](https://datasheets.diptrace.com/philips-nxp/1N4531.pdf)
- Transformer - [166E12](https://datasheets.diptrace.com/transformers/5c0018-19.pdf)
- Rectifier - [DBL202G](https://datasheets.diptrace.com/diodes_bridge/DBL201G%20SERIES_J15.pdf)