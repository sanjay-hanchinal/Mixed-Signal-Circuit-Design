Documentation of the design project titlted "ANALYSIS OF DIFFERENT KINDS OF SAMPLE AND HOLD ARCHITECTURES IN 180nm TECHNOLOGY".

A Sample and Hold (S/H) Circuit is primarily used in conjunction with Analog-to-Digital Converters (ADC) to sample and maintain 
an analog input signal for conversion. 
It is employed at the front-end of the ADC to relax the sampling time constraints, allowing for more accurate signal processing. 
Acts as an interface between the analog world and digital signal processing systems, ensuring precise signal acquisition and conversion.


Types of Sample and Hold architectures:
1) Open loop architecture
2) Closed loop architecture
3) Closed loop with pedestal error cancellation
4) Switched capacitor architecture
5) Current mode architecture

 Performance metrics 
• Acquisition time, tacq – time taken to stabilize the output. 
• Hold settling time, ths – time taken to stabilize sampled output 
• Dynamic range           - ratio between the maximum and minimum signal 
levels that a system can process without distortion or significant loss of 
information. 
• Non-linearity error     - non linear shift in the curve 
• Aperture jitter – time window for the output to settle after clock transition. 
•Pedestral error voltage - offset that appears in the signal, often due to system 
imperfections or drift. It results in the output signal being incorrectly displaced 
from the true baseline (zero or expected reference point). 
•Gain error      - 1-tan(𝜃) 
•Hold mode feedthrough  
•Droop rate   - the rate at which capacitor’s stored voltage value is reducing. 
•Signal to noise ratio (SNR) – signal power/rms of noise 
•Signal to (noise+distortion) ratio (SNDR) – signal power / signalpower – 1st harmonic amplitude

