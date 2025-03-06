# Differential-amplifier-

# Introduction
This report presents the design and analysis of a CMOS differential amplifier using LTspice.
The objective is to analyze the DC operating point, transient response, and frequency response under three configurations:

1.Current Source Biasing (ISS)

2.Resistor Biasing (RSS)

3.Additional MOSFET (M3) Biasing


# 2. Circuit Design Parameters
# MOSFET Dimensions
# Resistor-biased MOSFET
Width 𝑊=180
Length 𝐿=8.176𝜇m
![radai](https://github.com/user-attachments/assets/e87508b9-d182-481f-954c-b1c52e0ae10a)

# Current Source-biased MOSFET
Width W=180nm
Length L=7.637μm
![cureentdai](https://github.com/user-attachments/assets/67603d08-a3db-4379-bb6d-2ddb30341817)

# Additional CMOSN (M3) for biasing
Width W=180nm
Length L=13.0607μm
![m3op](https://github.com/user-attachments/assets/2295997b-03f1-43f4-993a-d7df45328012)

# Resistors & Current Source
𝑅1=𝑅2=1.8kΩ
R3 =416Ω (for RSS)

# Current source 
ISS=1.2mA

# 1. DC Operating Point Analysis

![image](https://github.com/user-attachments/assets/7c152e33-ccc8-41a2-a188-f4c0b74a2fec)

1.The differential pair operates in saturation mode.

2.The tail current source is correctly splitting between the two branches.

3.Common-mode voltage is stable at around 1.4V.

![image](https://github.com/user-attachments/assets/994ce8cb-1a44-4944-abf2-3d0a69a73377)
![image](https://github.com/user-attachments/assets/7a26d87c-6aef-41ff-90c4-51d84ffc4a70)
![image](https://github.com/user-attachments/assets/8b0a0733-d6b5-4749-b6fb-4e0b8ef0e661)
![image](https://github.com/user-attachments/assets/21fc1789-2101-495a-9650-0a6cc408598c)


# 2. Transient Analysis
Input Signal: 1V AC, 1kHz sinusoidal
The transient response shows a differential amplification with expected phase shifts.
Output voltages 𝑉𝑜1 and 𝑉𝑜2 oscillate with equal magnitude but opposite phase.

![m3tvocm](https://github.com/user-attachments/assets/43927df0-c50b-4b66-9e84-26ac5ea1c2a1)



# 3. Frequency Response Analysis
AC Gain Calculation
       # Gain (dB)=20log10(Vo2/vin)
At 1kHz, gain = 12.3dB
Bandwidth: The cutoff frequency is at 99.5MHZ Hz.
Gain-Bandwidth Product: 12.3 MHz

![WhatsApp Image 2025-03-06 at 22 39 28_70972413](https://github.com/user-attachments/assets/1e887d7e-b6ae-4b56-9b19-667871a39fb5)

# 4. AC Analysis
![AC DB OUTPUT](https://github.com/user-attachments/assets/4142e6be-e4c5-4375-841a-f861ab00c853)
![m3acop](https://github.com/user-attachments/assets/dfda6b81-a60e-41a1-a7b7-882c89fe1fcb)
![m3vcom](https://github.com/user-attachments/assets/60d9420e-3578-43db-9d82-6e2bf1a759ef)
![racvcom](https://github.com/user-attachments/assets/20a139ac-4948-4bdd-b165-6d90b16af68e)
![DC SWEEP2](https://github.com/user-attachments/assets/73aac451-c432-423b-b4c8-723078871202)
![m3vp](https://github.com/user-attachments/assets/74ffa2c3-55b2-4300-960c-8ae14983fb6c)









# 4. Comparison of Configurations
ISS provides better gain stability but requires an active current source.
RSS is simpler but introduces variations due to resistor mismatch.
M3 biasing improves tail current mirroring.
![image](https://github.com/user-attachments/assets/961af154-4e8e-47d8-bb9a-0f7c7e808b21)


# 5. Conclusion

The differential amplifier successfully amplifies differential signals while rejecting common-mode noise.

The current source (ISS) biasing offers better performance, but resistor (RSS) biasing is simpler.

Adding M3 enhances bias stability.
The differential amplifier operates correctly in saturation mode.

The ISS configuration is best for high gain and bandwidth.

M3 biasing enhances current mirroring, making the design more robust.

The simulated results match theoretical expectations, confirming the correctness of the design
