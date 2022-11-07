.. _xray4ldo:

Case Study (2)  
===============================================

xray4ldo ©
------------

* Power Management ICs (PMICs) are widely used for several kinds of autonomous and wearable devices to manage and monitor the provided power, especially for which use energy harvesting mechanisms. That is why the PMIC become promising recently. In autonomous devices, PMIC can be used in Electrical Vehicles (EVs) since a battery with certain power is provided to supply low/high power integrated circuits. On the other hand, PMIC is utilized broadly for  wearable’s/portable devices which are a significant part of the Internet of Things (IoT) systems. Consequently,  long-time and stable operation can be guaranteed significantly while using PMIC. 

* Since the growth of developing autonomous and wearable devices increased, the demand for using PMICs which is the main part of Power ICs, increased dramatically. As depicted in Figure 1, the Power Management IC Market is expected to reach US$ 51.13 Bn. by 2027, at a CAGR of 8.10% during the forecast period [1]. PMIC as a circuit can include different kinds of sub-circuits such as battery chargers, DC-DC converters, and linear regulation circuits to reduce the number of extra components and silicon area [2].

 
.. figure:: /images/fig1ldo.png
   :scale: 50%
   :align: center

   *Figure 1. Global Power Management IC Market.*

* Low-dropout regulator (LDO) is a DC (Direct Current) voltage linear regulator which regulates the output voltage smoothly at a certain level, according to its  application. This kind of regulators provide a "dropout" which can be defined as a difference between  the input and the  output voltage of less than 0.3V, typically. Recently, the LDO is widely used in different industries based on its characteristics such as LDO’s dropout voltage, line/load regulation, quiescent current, stability, and speed. Therefore, globally increasing demand for LDOs is expected due to the major growth of the usage of electronic devices. As depicted in Figure 2, the Global LDO Market Size is expected to grow at a CAGR of 6.03% during the forecast period of 2021-2030.


.. figure:: /images/fig2ldo.png
   :scale: 50%
   :align: center

   *Figure 2. Global Low Dropout Linear Regulator Market Size, Forecast and Y-o-Y Growth, 2019-2030.*


* Herein, an automated analysis of LDO is depicted. The  LDO is considered a  circuit under test as shown in Figure 3. The outer terminals should be defined as 6x-ports; vin, vref, vf, vss, vout, and vref wherever, the internal structure of LDO be.  Several kinds of analysis are used such as DC, transient, and AC analysis to define district parameters. Hence, the maturity of the design can be estimated.  

.. figure:: /images/fig3ldo.png
   :scale: 50%
   :align: center

   *Figure 3. LDO under test.*

 

* The developed tool is utilized to test a  designed LDO. After using the xray4ldo tool, the electrical characteristics of LDO are listed in table 1 and 2 @TT corner and Temp=27C.


.. list-table:: Table 1 : Results of xray4ldo tool
   :widths: 50 50 50 50
   :header-rows: 1

   * - Analysis
     - Paramter
     - LDO Topology
     - Unit  
   * - DC/DC Sweep
     - Total Current @ No Load
     - 9.13568E-05
     - (A)
   * - 
     - Total Power @ No Load and Vin=2V
     - 0.000182714
     - (W)
   * - 
     - line regulation @ Il=0.1mA and Vin=1.8V:3.5V                   
     - 0.005958
     - (V/V)
   * - 
     - load regulation @ Vin=2V and IL=0.1mA:10mA                   
     - 0.32
     - (V/I)
   * - 
     - Dropout voltage                   
     - 0.032483 
     - (V)
   * - AC Analysis 
     - Loop Gain   
     - 63.07
     - (dB) 
   * -  
     - Gain Bandwidth  Product  
     - 1814.47 
     - (Hz) 
   * -  
     - Phase Margin   
     - 80
     - (Deg)
   * -  
     - PSR @ 1KHz  
     - -42.4
     - (dB)

   * -  
     - PSR @ 1MHz                    
     - -94.3
     - (dB))

   * - Transient Analysis 
     - Load transient @vin=2V and Il=0mA:10mA      
     - 7.983
     - (mV)

   * - 
     - Line transient @ Il=0.1mA and Vin=2V:3.5V      
     - 9.553
     - (mV)
   * - 
     - Startup-time     
     - 26
     - (usec)

   * - Temp.
     - Temperature Coeff. @Vin=2V, Il=0.1mA, and Temp.=-40:85C   
     - 54.7
     - (ppm/C)
  

* Mismatch and process analysis for loop gain, gain bandwidth product, and phase margin are considered as shown in Figure 4 and 5.


.. figure:: /images/fig4ldo.png
   :scale: 50%
   :align: center

   *Figure 4. Mismatch and process analysist.*
   
.. figure:: /images/fig5ldo.png
   :scale: 50%
   :align: center

   *Figure 5. Mismatch and process analysist,Cont.*
