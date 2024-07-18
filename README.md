# CMVDPC-ADS
This contains archive files for a custom varactor diode model created in Keysight ADS.

There are three separate files here: "SDD_varactor_realistic", "SDD_varactor_Parasitics" and "Freq_Dependent_Resistor".
The first file contains the code needed to implement the new capacitance equation introduced in the paper using an SDD. Note that the sign convention for applied voltage is reversed from the paper; in
terms of voltage magnitude (absolute value of bias voltage) "vl" signifies the **larger** boundary voltage of a subregion, and "vr" the **smaller** boundary voltage. Hence "vl" is the 
**left** endpoint of subregion in terms of positive bias voltage, and "vl" the **right** endpoint. 
The model is hard-coded to operate at a maximum reverse-bias voltage of 10 V with a variable sub-region step size. If your application or particular diode requires larger bias voltages,
the model can accomodate this by adding more "K_vrX" equations, editing the points of the main "Q(v)" equation and altering the values of the "Vmax" and "Vmin" parameters. Take care to make 
sure charge continuity is satisfied.

The second file contains the full diode model including parasitics, where the diode SDD and frequency-dependent resistance SDD (third file) are components.

For questions, please email

strohman@umich.edu  and/or
zfritts@umich.edu



Ryan Strohman 

July 2024
