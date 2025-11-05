Sample and Hold circuits :

Sample and hold architectures are basic building blocks of the data conversion systems.
Sample and hold circuits are used with ADC to sample input analog signal and hold sampled signals.
These are used at front end of ADC to relax sampling time requirements.
Sampling circuit samples an analog signal and stores the value in a memory element until next sampling instant.

Open loop architecture:

<img width="821" height="315" alt="image" src="https://github.com/user-attachments/assets/b251c2bc-fa11-4f0c-ab9a-8a750ddd6ec0" />


It is used for high speed data conversion. The speed is decided by acquisition time and hold settling time.
Drawbacks : Input dependent charge injection to thr capacitor through switch. It is not cancelled by dummy transistors and differential form S/H .

Circuit Design:

Design blocks : Buffer B1 , B2 and Switch

Buffer Design : 

Circuit Diagram 

<img width="540" height="405" alt="image" src="https://github.com/user-attachments/assets/3a60cde5-0072-4ac6-9b8f-62aeb22f2029" />


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

<img width="780" height="501" alt="image" src="https://github.com/user-attachments/assets/98c40d5e-493b-43e5-a060-8feb5431a7f6" />

 


Open loop architecture circuit 

<img width="821" height="315" alt="image" src="https://github.com/user-attachments/assets/87041545-2fa6-45dd-af20-9e7dd81d0ef3" />




Implementation of test circuit 

<img width="786" height="464" alt="image" src="https://github.com/user-attachments/assets/a46599b5-14ab-423d-bc83-55f519480342" />


Output waveform

<img width="995" height="564" alt="image" src="https://github.com/user-attachments/assets/dae7dca8-f92e-4fb6-92b3-7e3873e22675" />


Observation :  
Rise time=89.51E-9 s Fall time=89.51E-9 s




