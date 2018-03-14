# Brushless Motor Controller
This repository contains the hardware and software implementation of a brushless 
motor controller based on the [Espressif ESP32 module].

The schematic and PCB was designed using de EDA tool [KiCad] and all C++ 
code was compiled using the [Espressif ESP32 toolchain].


## Brushless Motor Controller Schematic
![][bm_controller_sch]

[bm_controller_sch]: https://github.com/fabriziotappero/Brushless_motor_controller/blob/master/PCB/bm_controller_sch.png ""
[Espressif ESP32 module]: https://www.espressif.com/en/products/hardware/development-boards
[Espressif ESP32 toolchain]: https://dl.espressif.com/doc/esp-idf/latest/index.html
[KiCad]: http://kicad-pcb.org/

## Hardware And Software Tools

Install **Kicad 5** on Debial-like Linux systems:
```
sudo add-apt-repository --yes ppa:js-reynaud/kicad-5
sudo apt-get update
sudo apt-get install kicad kicad-libraries
```

Install **ESP32 Espressif** compiler with its dependencies:
```
sudo apt-get install git wget make libncurses-dev flex bison gperf python python-serial

wget https://dl.espressif.com/dl/xtensa-esp32-elf-linux64-1.22.0-80-g6c4433a-5.2.0.tar.gz

tar -xvf xtensa-esp32-elf-linux64-1.22.0-80-g6c4433a-5.2.0.tar.gz
sudo mv xtensa-esp32-elf /opt
export PATH=/opt/xtensa-esp32-elf/bin:$PATH
```
Install the **ESP32 Espressif** developing environment IDF:
```
mkdir /opt/eps32 
cd /opt/eps32
git clone --recursive https://github.com/espressif/esp-idf.git
cd esp-idf
git submodule update --init
export IDF_PATH=/opt/esp32/esp-idf
```

Begin from a simple example:
```
git clone https://github.com/espressif/esp-idf-template.git myapp
cd myapp
make menuconfig
```
A lot of code examples in ```/opt/esp32/esp-idf/examples```. For more information refer to the [Espressif ESP32 Programming Guide]

[Espressif ESP32 Programming Guide]: https://dl.espressif.com/doc/esp-idf/latest/index.html

## References

[Espressif ESP32 Programming Guide](https://dl.espressif.com/doc/esp-idf/latest/index.html)

[Digi-Key An Introduction to Brushless DC Motor Control](https://www.digikey.com/en/articles/techzone/2013/mar/an-introduction-to-brushless-dc-motor-control)

## More Information
For any enquiry contact:

fabrizio.tappero@gmail.com
