# Phase-Modulation-using-NumPy-and-Matplotlib-Modulation-and-Demodulation

# __Aim__:

To implement and analyze phase modulation (PM) using Python's NumPy and Matplotlib libraries. 


# __Apparatus Required__:

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer
   
# __Theory__:

Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the 
instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency 
is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message 
signal. 


The general form of a PM signal can be represented as:

<img width="483" height="254" alt="image" src="https://github.com/user-attachments/assets/8d5a2e54-cf93-4ff0-b0a6-e2000e078682" />






# __Algorithm__: 

1. Initialize Parameters:
   
o Set values for carrier amplitude (Ac), carrier frequency (fc), message frequency
 
(fm), sampling frequency, and phase deviation sensitivity (kp). 

2. Generate Time Axis: 

o Create a time vector for the signal duration based on the sampling frequency. 

3. Generate Message Signal: 

o Define the message signal as a cosine wave. 

4. Generate PM Signal:
 
o Apply the PM modulation formula to obtain the modulated signal.

5. Plot the Signals:
 
o Use Matplotlib to plot the message signal, carrier signal, and phase-modulated signal.
# PROGRAM:
```
import numpy as np 
import matplotlib.pyplot as plt 
Ac = 24.8
fc = 720
Am = 12.4
fm = 7200 
fs = 720000 
t = np.arange(0, 2/fm, 1/fs) 
Wm = 2 * np.pi * fm 
Wc = 2 * np.pi * fc 
Em = Am * np.sin(Wm * t) 
Ec = Ac * np.sin(Wc * t) 
Edsbsc = ((Am / 2) * np.cos((Wc - Wm) * t)) - ((Am / 2) * np.cos((Wc + Wm) * t)) 
plt.figure(figsize=(10, 6)) 
plt.subplot(3, 1, 1) 
plt.plot(t, Em) 
plt.grid() 
plt.subplot(3, 1, 2) 
plt.plot(t, Ec)
plt.grid() 
plt.subplot(3, 1, 3) 
plt.plot(t, Edsbsc) 
plt.grid() 
plt.tight_layout() 
plt.show()
```


# __Output__:

![WhatsApp Image 2025-11-21 at 19 32 11_44b24bae](https://github.com/user-attachments/assets/6fd18114-b12c-4bd3-8919-ad186a09e09b)


# TABULATION

![WhatsApp Image 2025-11-23 at 00 45 55_5754a817](https://github.com/user-attachments/assets/66e66550-8690-4fdf-9255-b0f8e3b7dd2a)


# CALCULATION

![WhatsApp Image 2025-11-23 at 00 46 11_3784a1e0](https://github.com/user-attachments/assets/f69b33b9-d50f-4296-9abe-ec90ec4c39fb)


# __Result__:
The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.




