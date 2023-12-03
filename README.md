# CMOS_characteristics
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



