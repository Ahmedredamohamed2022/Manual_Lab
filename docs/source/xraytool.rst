.. _xraytool:

X-Ray Tool for Analog/Mixed Circuit
======================================

Abstract
----------------------------------

* An automated open-source tool has been developed to provide an electrical characterization of the Analog/Mixed IP Blocks. The tool is able to assess the maturity of the design according to process and mismatching analysis. Moreover, a cost evaluation of the design is reported according to the figure of merit (FOM). Hence, design productivity time improves effectively.

Xray tool
----------

* As depicted  in Figure 1, xray tool can provide a full checklist for a given Circuit Under Test (CUT) which could be Trans-Conductance Amplifier (OTA), reference bandgap, Low Dropout Regulator (LDO), Digital-Analog Converter (DAC), Analog-Digital Converter (ADC), comparator,  ..etc. Xray tool provides distinct features;  It is a fully open source tool, provides a deep automated analysis, lists electrical  characteristics  of  the IP blocks, improves the  productivity time, indicates the design maturity, eases troubleshooting for the Sign-off.

.. figure:: /images/xraytool.png
   :scale: 50%
   :align: center

   *Figure 1. X-ray Tool for Analog/Mixed Circuit.*

* Just the user/designer should provides only 3x files to submit; Netlist of the circuit, configuration file, and  design specification file. Consequently, checklist and visualization figures are released. Figure 2 is an example for xray4ota tool.

.. figure:: /images/heirachyflow.png
   :scale: 50%
   :align: center

   *Figure 2. Hierarchy Flow Of X-ray4ota tool.*