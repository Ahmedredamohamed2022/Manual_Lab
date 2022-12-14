.. _settingup:


Design Analog Mixed Signal blocks Using Open Source Tools©
===============================================================

Objectives
------------

* **The main aim of the lab** is to propose an open source framework for a full-custom Integrated Circuit (*IC*) design, as shown in Figure 1. The framework relies on the cooperation of open resources; Xschem for schematic editing,NGspice for circuit netlisting/simulating,Python for data analysis. As a  result, the proposed open-source framework facilitates freely sharing and commercialization of the Integrated circuits design.

* A part of the presented framework is an xray tool which provides several benefits; It provides a deep automated analysis,a fully characterization of  analog IP blocks,improvementof productivity time, assessment of maturity design.

* Herein, a practical example for xray tool is :ref:`xray4ota<xray4ota>`.


.. figure:: /images/flowgraph.png
   :scale: 30%
   :align: center

   *Figure 1. Open-Source Framework for Full-Custom IC Design.*


Tools/Packages Installation  
-------------------------------

* Since the proposed framework relies on **open-source tools**, they can be installed freely on MS Windows or Linux operating system. In practice, the tools have been installed on a Linux server, and users can log in remotely.

Next, a short note about each  used tool.

* **XSCHEM** is a schematic capture program. It provides a graphical method to draw an electronic schematic circuit, easily. **XSCHEM**  can support main four netlist formats; SPICE netlist, VHDL netlist, VERILOG netlist, and tEDAx netlist. Consequently, once drawing the schematic circuit, a circuit netlist can be generated for simulation. Noted, the schematic circuit is saved with an extension of *“.sch”.*

* **NGSPICE** is an open-source spice simulator for electric and electronic circuits. It contains existing SPICE features with some extra analyses such as modeling methods and device simulation features. **NGSPICE** is mainly used for computer-based circuit simulations *(Analog, Digital, and Mixed-mode simulations).* Noted that,  **NGSPICE** can be executed using two different ways: batch mode or interactive mode. The latter model is preferred because it allows for running a script. The NGSPICE  can be saved with an extension of *“.cir”.* Moreover, a file including the netlist and NGSPICE is saved with an extension of *“.spice”*

* **SkyWater** Open Source Physical Design Kit *(PDK)* is a collaboration between **Google** and **SkyWater** technology foundry to provide fully open-source PDK and related resources, which can be used to create manufacturable designs at **SkyWater’s** facility.

* **Python** is widely powerful programming. It can be integrated with **NGSPICE** simulator for data manipulation/analysis and visualization. **Python** makes **NGSPICE** more powerful. Noted, the **python** script is saved with an extension of  *“.py”.* You have to import the following modules; import os, sys, import spice_read, import NumPy, and import matplotlib for well-data analysis and visualization.


.. admonition:: Open source tools

	Before  starting, You should double ckeck the required tools/packages if they were installed.


SkyWater Technology 
--------------------
* **SkyWater** open-source PDK provides a 130 nm CMOS process, SKY130, suitable for analog, digital, and mixed designs. As depicted in Figure 2, the **SKY130** layer stack consists of 5 metal layers (metal 1 to metal 5) with a local interconnect layer. The process includes deep n-well, Metal-insulator-Metal (MiM) capacitors, high and ultra-high sheet resistors, and isolated gate flash memory transistors. Moreover, **SkyWater** open-source PDK includes several libraries to serve the design of analog, digital, and mixed circuits

.. figure:: /images/SKY130stackup.png
   :scale: 60%
   :align: center
   :alt: Alternative text

   *Figure 2. SKY130 layer stackup.*


.. list-table:: SkyWater SKY130 Libraries
   :widths: 25 25 50
   :header-rows: 1

   * - Category 
     - Libraries 
     - Comment
   * - Digital standard cells
     - sky130_fd_sc_hd
     - High Density    
   * - 
     - sky130_fd_sc_hdll
     - High Density, Low Leakage
   * - 
     - sky130_fd_sc_hs
     - High Speed
   * - 
     - sky130_fd_sc_ms
     - Medium Speed
   * - 
     - sky130_fd_sc_ls
     - Low Speed
     
   * - 
     - sky130_fd_sc_lp
     - Low power
   * - 
     - sky130_fd_sc_hvl
     - High Voltage
      
   * - Primitive devices/analog
     - sky130_fd_pr
     - Primitive Cells

   * - I/O cells
     - sky130_fd_io
     - IO and Peripheral Cells
      

