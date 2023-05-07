Diode Characteristics

The static characteristics of the diode plots the diode current against the voltage across the diode.
The operation of the diode can be broken down into 3 regions:
  1) Forward Biased Region: 
  When the diode voltage($V_{d}$) is positve($V_{d}$ > 0).
  The device is said to be conducting and diode current $I_{d}$ is positive.
  where, Id = $I_{s}(e^{V_{d}/nV_{T}}-1)$.
                      
  2) Reverse Biased Region: 
  When $V_{d}$ is negative($V_{d}$ < 0).
  $I_{d}$ ~ 0
  
  3) Breakdown Region: 
  When $V_{d}$ is more negative than knee voltage($V_{zk}$).
  Reverse current increases rapidly with reverse voltage.
                        
                        

Schematic:

![image](https://user-images.githubusercontent.com/46377316/236682458-08ad3526-53dc-4676-b596-5ba98c37f732.png)

The diode parameters are listed below:
Saturation Current Is = 1e-14 A
Reverse Breakdown Voltage bv = 0.8V
Parameter measurement temperature tnom = 20 degC

Note: The DC characteristics of the diode are determined by the parameters IS, N, and the ohmic resistance RS. Charge storage effects are modeled by a transit time, TT, and a nonlinear depletion layer capacitance which is determined by the parameters CJO, VJ, and M. The temperature dependence of the saturation current is defined by the parameters EG, the band gap energy and XTI, the saturation current temperature exponent. The nominal temperature at which these parameters were measured is TNOM, which defaults to the circuit-wide value specified on the .OPTIONS control line. Reverse breakdown is modeled by an exponential increase in the reverse diode current and is determined by the parameters BV and IBV (both of which are positive numbers). 

Simulation:
DC Analysis is run, with a voltage sweep of Vd from -1.15 to 1V, in steps of 50mV.

The plot below shows the result of the DC analysis.
![image](https://user-images.githubusercontent.com/46377316/236683214-3f161870-3f7a-40fd-b49e-3868fb4b85c1.png)

To verify the diode equation, we sample the plot at a point.
The diode current when Vd is 0.9V, is 38.76A

Substituting 0.9V into the diode equation, with n = 1, $V_{T}$ = 25mV,
we get Id = 43.11V

