# MOS_characteristics
This project has only one motive; that is to experiment with working of a Mosfet and understanding all the parameters involved with it. The design will utilise the models that are present under the skywater 130nm pdk and various open source tools such as Xschem, NGSPICE , Netgen, etc.
## 1.Analysis of Mosfet Models
### 1.1 General Mos Analysis

Starting the analysis with Mosfet Model in **sky 130pdk**. Below is the schematic created in **Xschem**. 
![Screenshot from 2023-12-03 20-07-22](https://github.com/K-shejuti/CMOS_characteristics/assets/152790020/0aca716b-b369-4448-8ab6-b641680b5afe)
The components used are:
nfet_01v8.sym - from xschem_sky130 library

vsource.sym - from xschem devices library

code_shown.sym - from xschem devices library
We will do Id vs Vgs characteristics for different values of vds and ids vs vds characteristics for different values of vds
Useful commands
1)Display:This would display all the vectors available for plotting and printing.
2)Setplot-This would list all the set of plots available for this simulation.
3)plot-to choose the vector to plot.
#### 1.1.1 DC sweep on Vgs source for different vds
![Screenshot from 2023-12-03 20-40-20](https://github.com/K-shejuti/CMOS_characteristics/assets/152790020/c73c799d-b47b-4333-8007-dcabf910810b)

We can see the threshold voltage lies between 600mv to 800mv, let us take the threshold to be 0.7v.

#### 1.1.2. Sweep vds for different vds

![Screenshot from 2023-12-03 20-29-02](https://github.com/K-shejuti/CMOS_characteristics/assets/152790020/976b6118-d0b0-4480-b22e-79cd8e5cf60e)

#### 1.1.3. Plot the transconductance of the Mosfet for different values of vds.
We use deriv() function to find the derivative of current
![Screenshot from 2023-12-03 20-49-40](https://github.com/K-shejuti/CMOS_characteristics/assets/152790020/d29911a8-501d-4021-8d77-adc796baa16a)
#### 1.1.4. plot the output resistance(rds) of the mosfet
![Screenshot from 2023-12-03 21-07-22](https://github.com/K-shejuti/CMOS_characteristics/assets/152790020/d9c01e2f-3381-45a0-8c3f-8bc1cbcbf49c)

### 1.2 Strong 0 Weak 1
![Screenshot from 2024-01-05 16-33-12](https://github.com/K-shejuti/MOSFET-_Characteristics/assets/152790020/ef76aefd-656d-47cf-a9e4-92df631c4284)

![Screenshot from 2024-01-05 16-32-56](https://github.com/K-shejuti/MOSFET-_Characteristics/assets/152790020/e6c016e3-6c90-4993-b528-92196e23d26d)

We can see that, when a square wave is applied to the input of NMOS, when it is LOW(0V), the output goes to HIGH(1.8V). But when the input is HIGH(1.8V), the output goes to a value that is much larger than 0V. This is due to the fact that when Vgs is 1.8V, the NMOS is in linear region. This is where the MOSFET acts as a voltage controlled resistor. At this point, the output is connected to a Voltage Divider Configuration. That is the output takes the value which is defined by the voltage across the resistance of the mosfet. Hence, NMOS is able to transmit STRONG 0, but not a STRONG 1. So NMOS is Strong 0 but a Weak 1












