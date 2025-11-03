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


1) Open loop architecture :
 

   <img width="753" height="296" alt="image" src="https://github.com/user-attachments/assets/90ffd698-8d77-42aa-aa2d-cf37c95155be" />






   Used for high speed data conversion- stable if B1 and B2 are stable. The speed is decided by acquisition time and hold settling time.

2) Closed loop architecture :

   <img width="816" height="365" alt="image" src="https://github.com/user-attachments/assets/398ee543-c140-402d-af70-a60efea6198a" />


3) Closed loop with pedestal error cancellation :

Pedestal error cancellation is a technique used in closed-loop systems to correct low-frequency errors in the system’s output signal. 
In a closed-loop system, a feedback mechanism continuously monitors the output and adjusts the input to reduce any errors. Pedestal errors, which are 
unwanted shifts in the signal baseline, can be subtracted out through feedback and correction circuits.



4) Switched capacitor architecture :

<img width="636" height="304" alt="image" src="https://github.com/user-attachments/assets/b2be9fa3-0f6f-4812-aff5-e9eead9fe985" />


Consists of transconductance amplifier, sampling capacitor CH, s1-s3 switches. 
Widely used configuration- in ADC for capacitive load-Used in Pipelined AD

5) Current mode architecture :

Current Mode Architecture refers to a system design where current, rather than voltage, is used as the primary signal parameter. This approach is commonly 
used in high-speed analog circuits and communication systems.


<img width="726" height="233" alt="image" src="https://github.com/user-attachments/assets/09c43e0e-0e3c-47af-8e0f-0b465a0621ea" />
