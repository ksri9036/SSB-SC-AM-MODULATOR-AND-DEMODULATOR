# SSB-SC-AM-MODULATOR-AND-DEMODULATOR
# AIM:
To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics
# EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

# ALGORITHM:

1.	Define Parameters:

  	•	Fs: Sampling frequency.

  	•	T: Duration of the signal.

  	•	Fc: Carrier frequency.

  	•	Fm: Frequency of the message signal.

  	•	Amplitude: Maximum amplitude of the message signal.

2.	Generate Signals:

  	•	Message Signal: The baseband signal that will be modulated.

  	•	Carrier Signal: A high-frequency signal used for modulation.

  	•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.

3.	SSBSC Modulation:

  	•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.

4.	SSBSC Demodulation:

  	•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.

  	•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.

5.	Visualization:

  	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.

# PROCEDURE

•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file
 
•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform
# PROGRAM:
```
Am=13.2;
fm=1888;
fs=188800;
t=0:1/fs:3/fm;
Ac=22.44;
fc=18880;
em1=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em1);
ec1=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec1);
em2=Am*sin(2*3.14*fm*t);
ec2=Ac*sin(2*3.14*fc*t);
eDSBSC1=em1.*ec1;
eDSBSC2=em2.*ec2;
eLSB=eDSBSC1+eDSBSC2;
subplot(4,1,3);
plot(t,eLSB);
eUSB=eDSBSC1-eDSBSC2;
subplot(4,1,4);
plot(t,eUSB);
```
# MODEL GRAPH: 
<img width="747" height="338" alt="image" src="https://github.com/user-attachments/assets/1293e0fa-4b3a-45f6-9514-294977ddaf36" />

# OUTPUT WAVEFORM:
<img width="1525" height="981" alt="image" src="https://github.com/user-attachments/assets/1d711f0e-e2ce-4e31-8946-acdbbbb2c688" />

# TABULATION:
<img width="1600" height="960" alt="image" src="https://github.com/user-attachments/assets/8a3d852e-1b04-4860-8323-07ff7989fa55" />

# RESULT:
Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.
