# 5.Design-implement-and-simulate-Active-low-pass-High-pass-and-Band-pass-filter

**AIM:**
To design and obtain the frequency response of i)	First order Low Pass Filter (LPF) ii)	First order High Pass Filter (HPF) iii)	Band pass filter and also simulate it using LT-Spice.

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range
1.	Function Generator	3 MHz
2.	DSO	30 MHz
3.	Dual RPS	(0 – 30) V
4.	Op-Amp	µA741
5.	Bread Board	
6.	Resistors	1.6K,10K,5.86K,38.8K,7.9K
7.	Connecting wires and probes	As required
8.  LT SPICE software

**THEORY:**

**LOW PASS FILTER**

A LPF allows frequencies from 0 to higher cut of frequency, fH. At fH the gain is 0.707 Amax, and after fH gain decreases at a constant rate with an increase in frequency. The gain decreases 20dB each time the frequency is increased by 10. Hence the rate at which the gain rolls off after fH is 20dB/decade or 6 dB/ octave, where octave signifies a two fold increase in frequency. The frequency f=fH is called the cut off frequency because the gain of the filter at this frequency is down by 3 dB from 0 Hz. Other equivalent terms for cut-off frequency are -3dB frequency, break frequency, or corner frequency.
 
**HIGH PASS FILTER**

The frequency at which the magnitude of the gain is 0.707 times the maximum value of gain is called low cut off frequency. Obviously, all frequencies higher than fL are pass band frequencies with the highest frequency determined by the closed –loop band width all of the op-amp.

**BAND PASS FILTER**

A band pass filter has a pass band between two cutoff frequencies fH and fL such that fH > fL. Any input frequency outside this pass band is attenuated. There are two types of band-pass filters. Wide band pass and Narrow band pass filters. We can define a filter as wide band pass if its quality factor Q <10. If Q>10, then we call the filter a narrow band pass filter. A wide band pass filter can be formed by simply cascading high-pass and low-pass sections. The order of band pass filter depends on the order of high pass and low pass sections.

**DESIGN:LPF & HPF**

Given: fH = 1 KHz = 1/ (2πRC)
Let C = 0.1 µF, R = 1.6 KΩ
For n = 2, α (damping factor) = 1.414, Passband gain = Ao = 3 - α =3 – 1.414 = 1.586.
Transfer function of second order butterworth LPF as:
H(s) = 1.586/S2 + 1.414 s + 1
Now	Ao = 1 + (Rf / R1) = 1.586 = 1 + 0.586
Let Ri = 10 KΩ, then Rf = 5.86 KΩ

**DESIGN: BAND PASS FILTER**

Design a BPF to pass a band of 400Hz to 2KHz with a pass band gain of 4.
1.	Select the highest cut-off frequency of LPF as fH = 10 KHz and the lowest cut-off frequency of HPF as fL = 1 KHz.
2.	Design the HPF first by taking fL = 1KHz. Assume the value of C < 1μf.
3.	 Let C = 0.1μf.
4.	Calculate R from the expression. Given: fH = 2KHz = 1/ (2πR1C1)
5.	Let C1 = 0.1 µF, R1 = 7.9 KΩ
Given: fL = 400Hz = 1/ (2πR2C2)
Let C2 = 0.1 µF, R2 = 39.8 KΩ
Pass band Gain=4
Now		Ao = 1 + (Rf / R1) 2-1=(Rf / Ri)
Ri = Rf
Let Ri = Rf = 10 KΩ


**PROCEDURE - (LPF & HPF):**

1.	Connect the circuit as shown in the circuit diagram.
2.	Select the corresponding cut-off frequency (higher or lower) and determine the value of C&R. select the value of R1 & Rf depending on desired passband gain Af..
3.	Apply a constant voltage input sinusoidal signal to the non-inverting terminal of op-amp.
4.	Tabulate the output voltage Vo with respect to different values of input frequency.
5.	Calculate passband gain and plot the graph of frequency versus voltage gain & check the graph to get approximately the same characteristic as shown in the model graph.
 
**BAND PASS FILTER**

1.	Select the lower and higher cut-off frequency and calculate the value of R & C for the given frequencies.
2.	Design for LPF & HPF separately and then combine the circuit by first placing the HPF followed by a LPF (i.e) HPF in series with LPF.
3.	Connect the circuit as shown in the circuit diagram.
4.	Apply a constant voltage input sinusoidal signal to the non-inverting terminal of op-amp.
5.	Tabulate the output voltage Vo with respect to different values of input frequency.
6.	Calculate passband gain and plot the graph of frequency versus voltage gain & check the graph to get approximately the same characteristic as shown in the model graph.
 

**LPF:**
  **CIRCUIT DIAGRAM AND TABULATION:**
 <img width="954" height="1600" alt="image" src="https://github.com/user-attachments/assets/a1d7fba6-1d12-40bc-97e7-a75647b7383d" />

<img width="1087" height="1599" alt="image" src="https://github.com/user-attachments/assets/f3de9b51-1f16-4813-b4c8-cdbacccc6e46" />

<img width="1600" height="1164" alt="image" src="https://github.com/user-attachments/assets/86ed15f4-24e2-46fc-9322-3801f785d1bf" />


**HPF:**
  **CIRCUIT DIAGRAM AND TABULATION:**
<img width="1018" height="1600" alt="image" src="https://github.com/user-attachments/assets/3daa6ca2-2c99-46f8-8107-5bf85e04aedd" />

<img width="1073" height="1599" alt="image" src="https://github.com/user-attachments/assets/240e33ff-628e-4dc3-bf63-b901ba796d6a" />

<img width="1600" height="1188" alt="image" src="https://github.com/user-attachments/assets/516ddc79-fd86-4421-8f02-4d4205c8b21d" />


  **BPF:**
  **CIRCUIT DIAGRAM AND TABULATION:**
<img width="964" height="1600" alt="image" src="https://github.com/user-attachments/assets/92186f00-00a2-449d-9953-77cdf2e10f41" />

<img width="1144" height="1600" alt="image" src="https://github.com/user-attachments/assets/9a587de9-acb4-4cc4-85f1-1f89e0c695e7" />

<img width="1578" height="1134" alt="image" src="https://github.com/user-attachments/assets/d03e889f-75c0-4089-9280-7bb1fa0a7fff" />


**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  <img width="1600" height="823" alt="image" src="https://github.com/user-attachments/assets/5157c3e2-08df-4daf-a077-afd354e5971c" />

<img width="1600" height="821" alt="image" src="https://github.com/user-attachments/assets/4043bcf9-bd54-4bdc-813b-1573dca60755" />

<img width="1600" height="848" alt="image" src="https://github.com/user-attachments/assets/b7e5b2da-6d50-4b58-b2fb-73d16098651d" />


**RESULT:**
Thus the Active Low pass, High pass and Band Pass Filters are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
 
