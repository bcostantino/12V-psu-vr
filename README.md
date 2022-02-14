# Power Supply With Voltage Regulator
### Brian Costantino

###### Overview
This repository featured 3 designs, a 12V DC Power Supply (PSU), a 12V Fixed Linear Voltage Regulator (FIX-VR) and an Adjustable Linear Voltage Regulator (ADJ-VR). Each of these 3 designs are used in the main sheet (Sheet 1). The main module takes a 155V (60 Hz) AC input, and outputs two steady 12V DC supply voltages, one for each of the regulators.

###### Usage
To utilize the PSU and FIX-VR modules, no changes need to be made to the schematics. Keep in mind, the specs are fixed and the 12V output cannot be changed once this module is manufactured. On the other hand, when utilizing the ADJ-VR, the output can be changed simply by replacing a resistor. The variable resistor, RV, in sheet <ADJ-VR> can be selected using the following formula, where R1 is a constant 240 Ohms and Vref = 1.25V for the LM317P adjustable regulator.

Vout = Vref*(1+(RV/R1))

With RV = 2064 Ohms, the output voltage is 12V, however this can be changed to meet other supply voltage requirements.

