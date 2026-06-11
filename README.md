# SSBSC-modulation

EXP NO: 3 SSBSC Modulation

Aim: To Simulate SSBSC modulation to verify its waveforms.

Equations Used:
1. em1 = Am cos ωmt
2. ec1 = Ac cos ωct
3. em2 = Am sin ωmt
4. ec2 = Ac sin ωct
5. eDSBSC1 = em1 * ec1
6. eDSBSC2 = em2 * ec2
7. eLSB = eDSBSC1 + eDSBSC2
8. eUSB = eDSBSC1 - eDSBSC2


Algorithm
1. Start the program.
2. Define Am, Ac, fm, fc, fs, and generate the time vector.
3. Generate cosine message and carrier signals.
4. Generate sine message and carrier signals.
5. Form two DSB-SC signals by multiplication.
6. Add the DSB-SC signals to obtain LSB.
7. Subtract the DSB-SC signals to obtain USB.
8. Plot the message, carrier, LSB, and USB signals.
9. Observe the waveforms.
10. Stop the program.



Program
```
Am=9.6;
fm=1540;
fc=15400;
fs=154000;
t=0:1/fs:2/fm;
Ac=14.4;

em1=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em1);

ec1=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec1);

em2=Am*sin(2*3.14*fm*t);

ec2=Ac*sin(2*3.14*fc*t);

edsbsc1=em1.*ec1;

edsbsc2=em2.*ec2;

elsb=edsbsc1+edsbsc2;
subplot(4,1,3);
plot(t,elsb);

eusb=edsbsc1-edsbsc2;
subplot(4,1,4);
plot(t,eusb);


```
MODEL GRAPH
 <img width="919" height="1290" alt="image" src="https://github.com/user-attachments/assets/55326c5b-7dd5-4873-aaf6-d219bb7c4420" />
 TABULATION:
<img width="637" height="332" alt="image" src="https://github.com/user-attachments/assets/7ff79056-9cf7-4ff0-a385-703060457972" />
Calculation
<img width="648" height="362" alt="image" src="https://github.com/user-attachments/assets/07db08ba-635e-410e-914a-efc758fa6b82" />

Output Waveform
<img width="760" height="580" alt="image" src="https://github.com/user-attachments/assets/3efbd926-dbb4-4692-9040-b72d6a7faf32" />

RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
