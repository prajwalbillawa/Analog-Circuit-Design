# Diode based Logic Gates

Diodes can also be used to design logic gates due to their switching behaviour.
The schematic below shows the diode based circuit for an AND Gate and OR Gate.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/e2559f25-0efe-4788-be7a-3bcf46891c13)

In the Diode based AND Gate, any low voltage seen at the input, pulls the output voltage low. Else the output remains high.
In the Diode based OR Gate, any high voltage seen at the input, pulls the output voltage high. Else the output remains low.

Simulation:
As we have 3 inputs, there are $2^{3}$ logic test cases.
We make use of a Pulsed DC voltage source with varying frequency for each of the 3 inputs.
Va > Ts = 1ms
Vb > Ts = 0.5ms
Vc > Ts = 0.25ms
All pulsed sources have 50% duty cycle.

A transient analysis is run to get both outputs. The results are shown below.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/455e863e-7062-4712-9855-4fc080b441b1)
![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/c70868a0-6d30-4fec-8580-ad69dba2fc01)
![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/62f3ce69-e019-4286-b7c8-46b0f8c9ab31)

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/098fb825-bb4c-4a64-8143-36cad4bc86e0)

From the simulation, we see that the diode based logic gate does work as expected, but it does have limitations like:
  1) The output is not rail to rail voltage, but instead has a 0.7V drop.
  2) The behaviour of the gate during switching transient is not controlled.
