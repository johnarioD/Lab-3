# Lab-3  

Computer Architecture Lab 3  
This report was written by Ioannis Diamantaras (9387) and Dimosthenis Mpounarelis (9431).  

## Answer 1:
_Leakage_ and _Dynamic Power Consumption_ are both contributing factors to a CPU's total energy/power consumption. They, along with any _Short-Circuit Power Consumption_ define the overall energy needs of a processor. Nowadays, _Short-Circuit Power Consumption_ is ignored as it is relatively small and can be considered as part of the dynamic power consumption.  
  
Dynamic Power Consumption, specifically is the power required by the capacitors of the logic gates within the CPU. It is generally calculated as **_Pdyn = a*Σ(Ci*Vdd^2*f)_** where _Ci_ is the capacity of the individual capacitors that changed state, **_f_** is the frequency and and **_Vdd_** is the supply voltage and **_a_** is a switching factor (it represents the percentage of gates that actually switch within a clock cycle). A more accurate formula would be **_Pdyn = a*f*(ci*li+hi*ki*Co)*Vdd^2_**  
  
Leakage power is the static "leakage" of power through components normally percieved as insulating, such as a diode or any gradual losses from components such as charged capacitors. This type of power consumption is usually separated into two different categories: Subthreshold leakage and gate leakage. The first of the two refers to currents that continue to exist in components that are in their cutoff regions while the second refers to currents passing through the gate's oxides. Its value is **_Ple = hi*ki*Vdd*(Isub+Ig)_**  
  
Dynamic power consumption is going to increase in a "per program" basis and should scale more with the amount of the CPU operations than the actual time it takes for them to happen, of course, longer programs usually gave more instructions/operations so it would be expected that program execution time also indirectly affects this metric. Leakage is a more static power draining component which should only be related to CPU usage duration rather than instruction count.

_(Sources: )_

When dealing with the problem of optimizing power usage for a 40Watt battery compared to a 4Watt battery we should consider the following:  
