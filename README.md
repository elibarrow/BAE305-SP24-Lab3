
# Lab Report 3 - Let's Switch: Transistors as Switches
Eli Barrow & Isaac Stevens      
Feb. 1, 2024

## Summary of Lab ##
There were multiple goals for this lab, with the main purpose being to learn how diodes and transistors work in an electric circuit. To understand this, we created a circuit in which the transistor behaved as a switch and measured the gain associated with the transistor. In these circuits diodes, LEDs, and transistors were used and allowed us to observe their behavior as the factors were changed such as resistance, voltage, and opening/closing of switches. Throughout the lab, measurements were taken at different points in each of the three circuits that were built. Voltage was measured in different test points in the circuits with voltage drop across all the components also being measured and recorded. Lastly, the current was measured and recorded across specific components of each circuit. The gain was calculated and not measured using a DMM. Our class was unable to complete the second part of the lab which involved using a motor in a basic electric circuit.

### Lab Objective: Learn to use Diodes, LEDs, and transistors in a basic circuit ###  

## Lab Assignment Specific Items ##

For Lab 3, the following materials are required:

• A Digital Multi-meter (DMM): Fluke 87

• A DC Power Supply: Global Specialties 1403

•	3 Resistors: 2.2Ω, 270Ω, 1kΩ

•	An LED (any type)

•	A sliding switch (from the Sparkfun inventor’s kit)

•	An electric motor (from the Sparkfun inventor's kit)

•	A NTE 125 diode

•	A 1kΩ trimmer potentiometer

•	A TIP31C transistor

No code is required to complete Lab 3

## Part 1 - LED Driving Circuits ##

 The first 2 questions of Part 1 of this lab were based on the circuit in the picture shown below.


<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab3/blob/main/Figure%203%20Schematic.png width=25%>
</p>
 



_**Step 1**_   
We began by measuring the true values of the resistors and comparing them to the expected resistance using the Fluke 87 Digital Multimeter. 

Table 1. Real Values of the Resistors
 |Resistor (Expected Value)| Actual Value |
|---|---|
|270   &Omega;|  269.30   &Omega;  |
|1  k&Omega;|  985   &Omega;  |
|2.2   &Omega;|  2.5   &Omega;  |


*Figure 1

_**Step 2**_  
After building the circuit and verifying the resistor values, we then measured the voltages at each test point that is shown on the schematic above. We were then given the table below and filled it out with the values we measured in the lab. 

Table 2. Measurements in a circuit with an LED directly connected to a switch
 |Test Point| Voltage (Switch On)| Voltage Switch (Off) |
|---|---|---|
|T1|  4.989 V | 4.991 V|
|T2| 1.902 V  |1.902 V|
|T3|  0.008 V | 3.690 V |
|T4|  0.000 V | 0.000 V|
|**Component**| **Voltage (Switch On)**| **Voltage Switch (Off)**|
|R1|  3.089 V  | 0.000 V |
|LED1|  1.893 V  | 0.150 V|
|S1|  0.000 V  | 0.000 V|
||  **Current Through (Switch On)** |**Current Through (Switch Off)**|
|LED1|  10.010 mA  | 0.010 mA|  


*Figure 2

In step 2 we were also asked to calculate the current through R1 by using Ohm's law. When using V=IR, where V = 5V, R = 270&Omega;, I = ?. We found the current (I) through R1 equal to 18.518 mA.

_**Step 3**_  
For step 3 we built a new circuit, the one shown below, and measured the test points again, similar to step 2 above. We connected point T7 to the 5VDC output and T1 to the main output. We then filled out a similar table to Figure 2 to complete this step of part 1.

<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab3/blob/main/FIgure%204%20Schematic.jpeg width=25%>
</p>


Table 3. Measurements on a circuit with an LED connected through a transistor
 |Test Point| Voltage (Switch On)| Voltage Switch (Off) |
|---|---|---|
|T1|  4.979 V | 4.979 V|
|T2| 1.912 V  |4.979 V|
|T3|  0.022 V | 3.679 V |
|T4|  0.000 V | 0.000 V|
|T5|  0.696 V | 0.000 V |
|T6|  4.983 V | 0.000 V|
|T7|  4.983 V | 4.983 V |
|**Component**| **Voltage (Switch On)**| **Voltage Switch (Off)**|
|R1|  3.062 V  | 0.000 V |
|LED1|  1.895 V  | 0.020 V|
|R2|  4.285 V | 0.000 V |
|S1|  0.000 V  | 4.515 V|
||  **Current Through (Switch On)** |**Current Through (Switch Off)**|
|LED1|  11.200 mA  | 0.000 mA|  
|R2|  4.320 mA | 0.020 mA |
|R1|  18.519 mA | 18.519 mA |

*Figure 3

**Discussion Question 1: How does the current through the LED compare between circuits 1 & 2?**
When comparing the current that is flowing through the LED in circuits one and two we can easily see from the values in our table that the current running through the LED in the second circuit is about 1 mA greater than that of circuit 2 with the switch in the on position. When the switch is off, the current running through the LED in circuits 1 & 2 is equal to approximately zero. 

**Question a: What is the voltage drop ( $V_C$ ) across the transistor (Q1) when the LED is on?**    
 The voltage drop across the transistor is **0.02V** when the LED is on and **3.7V** when the LED is off.

 **Discussion Question 2: The datasheet mentions a maximum voltage drop (VCE) of 1.2V at saturation. We would like a much smaller value, such as the fraction of a volt that you measured in the first circuit across the switch, S1 when it is on. How does your measured VCE compare to the one listed in the datasheet? Do you think we are operating this transistor in the saturation region? The data sheet given is pictured below.**

 <p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab3/blob/main/Data%20sheet.jpeg width=75%>
</p>

 The value given in the data sheet is equal to 1.2V, the value that we measured was 0.022 V. We believe that we are in the saturation period because the value 0.022 is close to zero.

 **Question b:	Use the fine control in the power supply to make sure the transistor is in the saturation region. What should you see happen to the IC as you change the voltage?**  
 As you decrease the $V_C$ then the $I_C$ also decreases until there is no longer enough voltage to activate the transistor, thus putting the $I_C$ to zero.


_**Step 4**_  
For step 4 we built a new circuit, the one shown below, and measured the test points again, similar to step 3 above. We then filled out a similar table to Figure 2 to complete this step of part 1.

We also took measurements of the current running through the LED when the light was barely visible and when the LED was bright. The dim LED had a current of 0.68 mA and the bright LED had a current of 11.31 mA.

Table 4. Controlling LED current using a transistor
|Test Point | Voltage (Dim LED) |Voltage (Bright LED) | Voltage (Point 1) |Voltage (Point 2) |Voltage (Point 3)|
|---|---|---|---|---|---|
|T1|4.980 V|4.975 V|4.976 V|4.976 V|4.976 V |
|T2|4.890 V|1.916 V|3.440 V|4.261 V|4.602 V |
|T3|3.280 V|0.028 V|1.538 V|2.521 V|2.900 V |
|T4|0.002 V|0.028 V|0.005 V|0.004 V|0.003 V |
|T5|0.536 V|0.669 V|0.609 V|0.587 V|0.572 V |
|T6|0.537 V|0.671 V|0.610 V|0.586 V|0.572 V |
|**Component** | **V. Across (Dim LED)** |**V. Across (Bright LED)**|**V. Across (Pt. 1)**|**V. Across (Pt. 2)**|**V. Across (Pt. 3)**|
|R1|0.095 V|3.058 V|1.632 V|0.683 V|0.395 V|
|LED1|1.612 V|1.888 V|1.815 V|1.717 V|1.696 V|
|R2|0.000 V|0.004 V|0.003 V|0.002 V|0.001 V|
|**Component**|**Current Across (Dim LED)**|**I. Across (Bright LED)**|**I. Across (Pt. 1)**|**I. Across (Pt. 2)**|**I. Across (Pt. 3)**|
|LED1|0.13 mA|11.23 mA|6.00 mA|2.50 mA|1.42 mA|
|R2|0.01 mA|3.57 mA|0.07 mA|0.03 mA|0.02 mA|
|Gain|13 |3.14|85.7|83.33|71.3|


Graph 1: IB and IC with respect to change in Voltage BE
 <p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab3/blob/main/IB%20and%20IC.png width=75%>
</p>

Graph 2: Gain with respect to change in Voltage BE
 <p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab3/blob/main/Gain.png width=75%>
</p>

Graph 3: Voltage CE with respect to change in Voltage BE
 <p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-Lab3/blob/main/Voltage%20CE.png width=75%>
</p>


**Unfortunately we outlasted the time of the lab and were not able to complete the entire lab that was written for us. We only got as far as this lab report shows.**

## Conclusion of Lab ##
The lab's outcome was using semiconductors such as diodes and switches that do not allow current to flow through a circuit and adding too much voltage into a transistor can create a semiconductor that also blocks current from flowing as well. In the first circuit, when the switch was flipped off current was unable to flow through the LED leading to the light not turning on despite the incoming voltage from the power supply. Voltage was measured in test spots, through components, and current was measured when the switch was on and off. For the second circuit, a transistor was added and the switch was added to a different branch in the circuit. When the switch was turned off, the current would not flow through the LED on the transistor side once again and also prevented voltage from the power supply from traveling through many of the components on the transistor side. This is caused by Ohm's law V = IR since current is zero so is the voltage drop along those components. Voltage was measured in test spots, through components, and current was measured when the switch was on and off. For the third circuit, there was no switch in the circuit but a transistor was still present.  By changing the resistance in the potentiometer, the voltage was changed throughout the circuit. Five voltage points were taken with the lowest voltage having a dim LED light and the highest having a bright LED light and the three other points being in between. Voltage was measured in test spots, through components, and current was measured as well. The gain was calculated using the current running through LED1 and R2 in the circuit. The gain continued to increase as voltage was increased until the highest point in which it decreased. This was caused by a property in transistors in which after a certain voltage, transistors' gain begins to decrease, and the component could break. Lab 3 helped quantify the behavior of switches, diodes, and transistors and helped create a better understanding for our group when it came to using these components in a real-world circuit.
 
