DSBSC USING PYTHON

EX NO: 2 DSB-SC-AM MODULATOR AND DEMODULATOR USING PYTHON

AIM:

To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics.

EQUIPMENTS REQUIRED

• Computer with i3 Processor • CO LAB.

Note: Keep all the switch faults in off position

Algorithm:

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal. Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation. DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal. DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal. Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. PROCEDURE • Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file

• Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform
Model Waveform:

program:
```
import numpy as np
import matplotlib.pyplot as plt

Am = 3.9
Ac = 7.8
fm = 487
fc = 4870
fs = 48700

t = np.arange(0, 2/fm, 1/fs)

m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)

c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)

s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)

s = s1 - s2

plt.subplot(3, 1, 3)
plt.plot(t, s)

plt.tight_layout()
plt.show()
```
Output Graph:
![WhatsApp Image 2025-11-25 at 7 50 41 PM](https://github.com/user-attachments/assets/2234bf61-8eaa-4b06-9ba2-3fff8d365848)


Tablular Column:

![WhatsApp Image 2025-11-25 at 10 39 24 PM](https://github.com/user-attachments/assets/9c74dae9-8b07-491e-8a75-6f4c2b8add19)

Result:

Thus the DSB-SC-AM Modulation and Demodulation using python is generated.
