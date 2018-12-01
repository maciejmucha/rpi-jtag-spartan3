# Raspberry PI JTAG for Spartan3
This project was created to be able to download the bitstream to a FPGA board with 2 chips in the JTAG chain (XFC01S PROM and XC3S200 FPGA). Like this one:  

![FPGA](https://www.picclickimg.com/d/l400/pict/202418248319_/XILINX-SPARTAN-3-XC3S200-FPGA-module-FPGA-kit-Development.jpg).

<YOUTUBE LINK>

The prohect proves 2 utilites the firstone **idcode** is to test reading the IDCODES in a chain, and **fpga_program** to load the bitstream inot the fpga. Is super simple to extend the functionalities.

Raspberry PI JTAG programmer for Spartan3 FPGA. This project is written in a poorly but working C/C++ mix for a RPI v1. So **Choose proper JTAG pins wirings for your RPI version in main cpp file. Pin numbers use wiringPI numeration** 

# Prerequisites
wiringPI library

# Usage
1. [Install wiringPI library](http://wiringpi.com/download-and-install/)
2. Clone repository `git clone https://github.com/yuyomagico/rpi-jtag-spartan3`
3. Check your RPI Version and check pin numbers for JTAG port in "idcode.cpp"
4. `./idcode_build.sh` to build the **idcode** and `./build.sh` to build **fpga_program**.
5. Outputs will be written into `bin/`
6. Usage: `./bin/idcode` and `./bin/fpga_program <filename>`
