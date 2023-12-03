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
