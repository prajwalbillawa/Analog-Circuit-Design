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

![image](https://user-images.githubusercontent.com/46377316/236687354-8e1f771c-e7be-446d-bc6d-d9f2e597fa98.png)

The diode parameters are listed below:
Saturation Current Is = 1e-14 A
Reverse Breakdown Voltage bv = 0.8V
Parameter measurement temperature tnom = 20 degC

Note: The DC characteristics of the diode are determined by the parameters IS, N, and the ohmic resistance RS. Charge storage effects are modeled by a transit time, TT, and a nonlinear depletion layer capacitance which is determined by the parameters CJO, VJ, and M. The temperature dependence of the saturation current is defined by the parameters EG, the band gap energy and XTI, the saturation current temperature exponent. The nominal temperature at which these parameters were measured is TNOM, which defaults to the circuit-wide value specified on the .OPTIONS control line. Reverse breakdown is modeled by an exponential increase in the reverse diode current and is determined by the parameters BV and IBV (both of which are positive numbers). 

Simulation:
DC Analysis is run, with a voltage sweep of Vd from -1.15 to 1V, in steps of 50mV.

The plot below shows the result of the DC analysis.
![image](https://user-images.githubusercontent.com/46377316/236686131-88131816-b6fe-45b7-adeb-1bea0e46e5c7.png)

To verify the diode equation, we sample the plot at a point.
The diode current when Vd is 0.9V, is 29.71A

Substituting 0.9V into the diode equation, with n = 1, $V_{T}$ = 20mV,
we get Id = 29.93V


The Diode current is also a function of temperature as the Reverse Saturation Current(Is) doubles for every 5 degC rise in temperature.
The below plot shows the temperature dependence of the diode current.

Schematic:

![image](https://user-images.githubusercontent.com/46377316/236691508-bebbd89f-d724-4fad-86a1-2c5aa2b795f3.png)

Waveform:


![image](https://user-images.githubusercontent.com/46377316/236691671-6636e809-7b19-4f59-bdf3-f93c30b13fa5.png)


Thus, at a given constant diode current, the voltage drop across the diode decreases by approximately 2mV for every 1 degC increase in temperature.

  
