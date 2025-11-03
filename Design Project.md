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

<img width="957" height="654" alt="image" src="https://github.com/user-attachments/assets/f608d67a-0ddf-429a-86ca-0b7399446994" />
