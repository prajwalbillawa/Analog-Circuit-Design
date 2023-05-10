# Voltage Regulation

Diodes can also be used for voltage regulation, wherein a constant output voltage can be mantained, even in the presence of:
  1) Changes in load current drawn.
  2) Changes in DC voltage supply.

Voltage regulation can be achieved owing to the fact that the diode maintains a forward bias drop of approximately 0.7V(cut-in voltage).
From the static characteristics, we see that there is a very small variation in voltage for large change in diode current, after the cut-in voltage.

Thus a constant voltage of ~0.7V can be achieved using a single diode. For voltages greater than this, multiple diodes in series can be used.

Simulation:
The below schematic consists of 3 similar diodes placed in series.
The cut-in voltage for each of the diodes is ~0.65V.
Resistor R1 is valued at 1k ohm, which is used to fix the forward bias voltage for the diode chain.
The voltage source is 10VDC.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/84ca8097-f153-4df4-8e1a-f68b1656e5bc)

Running a transient analysis, we see that the output voltage when Vdd is 10V is 2.04V.
The current drawn from the voltage source is 7.9mA.
Since all 3 diodes are similar, the voltage drop across a single diode is 2.04/3 = 0.68V.
![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/95808aa5-4c0d-4154-b844-f7ec63fc5bcc)

For case 2, consider that the voltage supply Vdd fluctuates by +/- 1V.
Running a DC analysis with a voltage sweep of Vdd from 9V to 11V, we observe the below result.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/b52747fd-6e86-4f6a-8cb9-ad0353ad9b45)

From KVL, $\Delta V_{o} = \Delta V_{i}\times \left ( \frac{r_{d}}{r_{d} + R} \right )$
where $r_{d}$ is the diode small signal resistance.
$r_{d} = \frac{nV_{T}}{I_{d}}$ , or simply the slope of the Id vs Vd curve at the operating point.

Substituating the vlues, we get $ r_{d} $ = 6.3 ohm.
Thus, for a voltage variation of 2V, we expect an output voltage variation of approximately 37mV.
From the plot, we see an output voltage variation of 20mV, which is reasonably close to our calculated approximation.

For case 3, we consider a load with resistance of 1k ohm.
The schematic below shows the modified circuit.
![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/b876e0ba-676c-416e-9c7d-b684d462efee)

The simulation results show that Vout has now dropped from 2.04 from the previous case, to 2.02V. Thus, even when a load is connected, the diode maintains the voltage across its terminals(as long as all diodes are forward biased).
We can estimate this by assuming the current drawn by the load is 2.04mA (2.04/1k)
Thus, $\Delta V_{o} =$ -2.04 x 18.9 = 38mV.
Thus Vout = 2.04 - 0.038 = 2.002V, which is as per the simulation result.
![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/e77e5013-1e31-43b1-8180-d27fc96b790d)

Note: A 38mV reduction would mean a 13V reduction in diode voltage across each diode. Thus, the small signal model does not apply as diode small signal resistance is no longer linear. But since the bounds of operation is reasonably small, the approximation still holds.

Therefore, we conclude that the diode can be used for voltage regulation when operated in the forward bias mode.

