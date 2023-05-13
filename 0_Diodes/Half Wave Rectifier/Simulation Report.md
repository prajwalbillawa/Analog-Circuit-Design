# Half Wave Rectifier

The Half wave rectifier circuit represents one of the blocks required for AC to DC signal conversion.
In a half wave rectifier, the negative half of the input sinusoid is blocked, whereas the positive half of the sinusoid is allowed to pass.
This behaviour is enabled due to the characteristics of the diode.

During the positive half cycle, the diode is forward biased. Thus, the load resistor sees a voltage of Vin - 0.65V of the diode.
During the negative half cycle, the diode is reverse biased. Since the reverse saturation current is negligible, the drop across the load is negligible adn therefore 0.

The circuit simulation below shows the operation of the Half wave rectifier circuit.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/7f0bbb5b-baec-451d-9150-0dc128e080eb)

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/b6212ff9-4c90-4782-acab-6852ebe68c3a)

Note: Care must be taken to ensure that the PIV(Peak Inverse Voltage) of the input sinusoid must not be greater than the reverse breakdown voltage, or else the diode conducts and the output waveform is not as expected
The below simulation shows the output of a half wave recitfier circuit that uses a diode with reverse breakdown voltage of 4V. As soon as Vin corsses the value, the diode conducts as it operates in the breakdown region.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/89a65280-7f47-48c2-b7c4-f4b32512fd7d)

