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
9. THEORY

Single Sideband Suppressed Carrier (SSB-SC) modulation is a form of amplitude modulation in which only one sideband (either Upper Sideband or Lower Sideband) is transmitted while the carrier and the other sideband are suppressed.

Since only one sideband carries all the information of the message signal, SSB-SC requires less bandwidth and transmits power more efficiently than conventional AM and DSB-SC systems.

The message signal is given by:

em(t) = Am cos(2πfmt)

The carrier signal is given by:

ec(t) = Ac cos(2πfct)

The DSB-SC signal is given by:

edsbsc(t) = em(t) × ec(t)

Using the phase shift method, the Lower Sideband (LSB) and Upper Sideband (USB) signals are generated as:

LSB = edsbsc1 + edsbsc2

USB = edsbsc1 – edsbsc2

where,

Am = Amplitude of the message signal
Ac = Amplitude of the carrier signal
fm = Frequency of the message signal
fc = Frequency of the carrier signal

Advantages of SSB-SC:
• Reduced bandwidth requirement.
• Efficient utilization of transmitted power.
• Reduced interference and noise effects.

Thus, SSB-SC modulation transmits only one sideband, thereby improving bandwidth and power efficiency.


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

 TABULATION:
 
 <img width="642" height="347" alt="image" src="https://github.com/user-attachments/assets/8e47ad58-c559-4606-88fc-2308ae1530f4" />



Output Waveform:

<img width="742" height="691" alt="image" src="https://github.com/user-attachments/assets/ef6022a6-530a-4d59-9c2d-252e518c788a" />

RESULT:
Thus, the Single Sideband Suppressed Carrier (SSB-SC) signal is generated using the phase shift method and the corresponding Upper Sideband (USB) and Lower Sideband (LSB) waveforms are obtained and verified.
