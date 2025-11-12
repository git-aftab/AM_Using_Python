<h1>Amplitude-Modulation using python</h1>

<h2>EXP NO: 1 GENERATION AND DETECTION OF AM using python</h2>

<h3>AIM:</h3>

To generate and detect the amplitude modulation and demodulation using python code and to calculate modulation index of AM.

<h3>EQUIPMENTS REQUIRED</h3>

• Computer with i3 Processor

• colab

<h3>THEORY:</h3>

Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator. Need for modulation is as follows: • Avoid mixing of signals • Reduction in antenna height • long distance communication • Multiplexing • Improve the quality of reception • Ease of radiation. Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

1. Under modulation : m<1, Em < Ec
2. Critical modulation: m-1, Em = Ec
3. Over modulation: m>1, Em > Ec
   Algorithm:

1. Define Parameters First, define the parameters for your signals: • Carrier frequency (fc) • Modulating signal frequency (fm) • Sampling frequency (Fs) • Duration of the signal (T)

2. Create a time vector based on the sampling frequency and duration.

3. Create Modulating Signal Define the modulating signal (message signal).

4. Create Carrier Signal Define the carrier signal.

5. Perform Amplitude Modulation Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).

6. Plot the Signals Visualize the modulating, carrier, and modulated signals.

7. Demodulate the AM Signal To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

8. Plot the Demodulated Signal Visualize the demodulated signal.

9. Compare Signals Compare the original modulating signal with the demodulated signal. PROCEDURE • Refer Algorithms and write code for the experiment. • Open colab in System • Type your code in New Editor • Save the file • Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform

<h3>Program</h3>
```
import numpy as np
import matplotlib.pyplot as plt
Am = 3.2
Ac = 6.4
fm = 920
fc = 9200
fs = 92000
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.tight_layout()
plt.show()
```

<h3>Output Waveform</h3>
<img width="1536" height="898" alt="Figure_1" src="https://github.com/user-attachments/assets/6d34f252-e34b-4db8-b890-bf3d3199caf1" />


<h3>Calculation</h3>

ma (Theory) = am/ac =0.5
ma(Practical) = (Emax-Emin)/(Emax+Emin) =0.5

<h3>Model Graph</h3>
<img width="919" height="1290" alt="image" src="https://github.com/user-attachments/assets/55326c5b-7dd5-4873-aaf6-d219bb7c4420" />


<h3>Result</h3>
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
