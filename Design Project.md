Sample and Hold circuits :

Sample and hold architectures are basic building blocks of the data conversion systems.
Sample and hold circuits are used with ADC to sample input analog signal and hold sampled signals.
These are used at front end of ADC to relax sampling time requirements.
Sampling circuit samples an analog signal and stores the value in a memory element until next sampling instant.

Open loop architecture:

<img width="821" height="315" alt="image" src="https://github.com/user-attachments/assets/b251c2bc-fa11-4f0c-ab9a-8a750ddd6ec0" />


It is used for high speed data conversion. The speed is decided by acquisition time and hold settling time.
Drawbacks : Input dependent charge injection to thr capacitor through switch. It is not cancelled by dummy transistors and differential form S/H .

Implementation :


First we implemented a normal Sample and hold circuit using nmos , pmos and cmos as switch. The observations are as follows:

PMOS as a switch


![22 50 28 ರಲ್ಲಿ WhatsApp ಇಮೇಜ್ 2025-11-04_8e9a33bb](https://github.com/user-attachments/assets/eaa3c749-4a6a-498d-b3ce-29dd0ed04da0)





Ouput waveform 



![22 50 29 ರಲ್ಲಿ WhatsApp ಇಮೇಜ್ 2025-11-04_7b501f65](https://github.com/user-attachments/assets/cb56ab85-42dd-42c4-8b7f-360067847c88)







NMOS as a switch 




![22 50 30 ರಲ್ಲಿ WhatsApp ಇಮೇಜ್ 2025-11-04_536631f1](https://github.com/user-attachments/assets/ce8c56c6-0cc8-4406-9e0b-079cba81f60b)



Ouput waveform 



![22 50 30 ರಲ್ಲಿ WhatsApp ಇಮೇಜ್ 2025-11-04_01c995ad](https://github.com/user-attachments/assets/e4bf3efe-9f7d-4a53-9bdd-db876b06f3cd)






CMOS as a switch



![22 50 28 ರಲ್ಲಿ WhatsApp ಇಮೇಜ್ 2025-11-04_b5bd5194](https://github.com/user-attachments/assets/dde5220f-34c0-43e5-991d-367ac7de4f8b)




Output waveform


![22 50 30 ರಲ್ಲಿ WhatsApp ಇಮೇಜ್ 2025-11-04_c359afb8](https://github.com/user-attachments/assets/28e0b009-c907-4edf-82fb-c28300074d83)





1) Open loop architecture:





   As this architecture uses buffers , the buffer design is provided below.
CMOS buffer

CMOS buffer is a digital circuit used to strengthen or restore logic signals without altering their logical value
It acts as an intermediary between circuits to provide current drive, isolation, or signal regeneration.


 


Open loop architecture circuit 

<img width="821" height="315" alt="image" src="https://github.com/user-attachments/assets/87041545-2fa6-45dd-af20-9e7dd81d0ef3" />




OPEN LOOP ARCHITECTURE 

Circuit diagram 
<img width="2431" height="1135" alt="image" src="https://github.com/user-attachments/assets/bde5b4e8-315b-4c79-ac4b-198fa8c1ee5e" />

Design of Opamp(for Buffer)

<img width="1384" height="767" alt="image" src="https://github.com/user-attachments/assets/bd4c9f0d-2355-4a8d-808f-9144a1b749db" />
Design procedure
<img width="756" height="1045" alt="image" src="https://github.com/user-attachments/assets/7ad6a21e-bc1f-4f1f-b4af-ab7d9eb881bb" />
specifications of opamp
<img width="581" height="613" alt="image" src="https://github.com/user-attachments/assets/aa47fdd9-8b45-468c-aa73-b98919590f24" />
Test circuit
<img width="1889" height="1482" alt="image" src="https://github.com/user-attachments/assets/2b0c6362-d6f6-4b2a-be6e-ebe0e83a0c48" />
AC analysis of opamp
<img width="3039" height="1370" alt="image" src="https://github.com/user-attachments/assets/edc3c891-2afb-4e5e-92d0-2365ae811ce2" />

Test circuit--opamp as buffer
<img width="1178" height="778" alt="image" src="https://github.com/user-attachments/assets/2e13979d-4d6f-4891-89c5-6bd52d88c906" />

Transient analysis of opamp as buffer

<img width="1436" height="623" alt="image" src="https://github.com/user-attachments/assets/bf612fd0-262f-4c7c-815f-1c6ad90c7c6a" />

Transient analysis of openloop S&H:

<img width="1324" height="532" alt="image" src="https://github.com/user-attachments/assets/b05e2776-99d2-41ac-a92c-4dcd0f25d173" />

Open loop S/H ckt spectrum analysis

<img width="933" height="518" alt="image" src="https://github.com/user-attachments/assets/abda817c-758b-4898-a324-d40c4df0d583" />

This kind of sample and hold architecture uses two opamp based buffers. The open-loop S/H is a simple sampling system where the input is directly connected to the hold capacitor during the sampling phase, without any feedback amplifier to correct errors.

Working :
Sampling Phase (φ = ON)
The MOS switch conducts. The input voltage charges the hold capacitor and CH tracks Vin.

Hold Phase (φ = OFF)

The switch opens. The capacitor retains the sampled voltage , output remains constant.

Limitations of Open loop architecture

Gain error
Voltage on CH depends on switch resistance and input source impedance.

Droop (voltage decay)
Leakage of switch + capacitor ESR causes voltage change during hold.

Charge injection & clock feedthrough
When the MOS switch turns OFF, channel charge is dumped into C_H.

Nonlinearity
Switch resistance varies with Vin → distortion.

Not suitable for high-resolution ADCs
Typically limited to ~6–8 bits accuracy.

Advantages:
Very simple architecture

Low power

No amplifier complexity

High speed (limited only by RC time constant)


Design Outcome:

Opamp with gain of 62 dB and Phase margin of 80 degrees.

Open loop architecture with less distortions in the ouput side.

Designed the circuit for all three switches -  NMOS , PMOS and CMOS.

Summary/Novelty:
Open loop S/H provides:
Very High Speed,
Lower Power Consumption,
Compact Area,
Less Sensitive to Op-Amp Stability Issues.





