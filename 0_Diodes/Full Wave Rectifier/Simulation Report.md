# Full Wave Rectifier

## Center Tap Full Wave Rectifier
The center tap full wave rectifier works on both positive and negative cycles of the input sinusoidal wave.
It makes use of a center tap transformer whose turn ratio is 2. 
The center tap from the secondary coil is grounded to provide a reference point.

Both legs of the secondary coil are connected to a diode.
During each half cycle, only 1 diode conducts and half the voltage of the secondary coil is seen across the load.
In the next cycle, as the input sinusoid reverses in polarity, the 2nd diode conducts while the first goes to reverse biased state.
In this cycle too, the load sees the input voltage across its terminals.

The schematic below depicts a center tap full wave rectifier.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/f6dcf2b3-3bc3-4c21-a2b0-b66d400b3d41)

When Vin is positive, D1 is forward biased and D2 is reverse biased.
Thus the load sees a voltage of Vin - 0.65V across its terminals.

During the negative cycle, D1 is reverse biased and D2 is forward biased.
The load sees a voltage of -(-Vin) - 0.65V across its terminals.

The below simulation plot reaffirms the theory.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/e6bfb574-363f-41d1-97f2-5ccb78325c8e)


## Bridge Rectifier

The Bridge rectifier is also a full wave rectifier.
It used a simple transformer with a primary and secondary.
The number of diodes used is 4.

The circuit below depicts a Bridge rectifier.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/5df074ae-ca15-4162-8359-e0da0ad4781a)

When the input is in its positive cycle, D4 and D5 are forward biased, whereas D3 and D6 are reverse biased.
The load sees a voltage of Vin - 0.65V - 0.65V.
Thus, there is an dditional diode drop in a bridge recitfier when compared to center tap full wave rectifier.

The below simulation depicts this action.

![image](https://github.com/prajwal-billawa/Analog-Circuit-Design/assets/46377316/09c6fb69-db67-4498-b0c1-02533d5689d4)
