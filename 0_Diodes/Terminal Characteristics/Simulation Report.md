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

Simulation:
DC Analysis is run, with a voltage sweep of Vd from -1.15 to 1V, in steps of 
