# Pulse oximeter and perfusion index acquisition system
Pulse oximeter and perfusion index acquisition system is a measurement system that provide Hart Rate HR, level of oxygen saturation SPO2, and Perfusion Index PI of observed person in real time. This system is based on embedded hardware device for sensing and Python source code for data processing. It is non invasive light reflective method with two wavelengths and could be used for development starting point.
## Hardware
![Hardware](/Pictures/Hardware.jpg)

Hardware is consist of two development boards from MikroElektronika.
[Hart rate click](https://www.mikroe.com/heart-rate-click) have MAX30100 pulse oximeter integrated circuit.
[PIC clicker](https://www.mikroe.com/clicker-pic18fj) is board that have microcontroller, micro BUS and USB port.
Firmware SPO2.hex must be downloaded to PIC clicker. It’s possible thru integrated Bootloader or with mikroProg for PIC programmer.
It’s send values of reflected Infra-Red and Red lights via USB that is defined like virtual COM-port. Frequency of acquisition is 50 Hz.
It is necessary that COM port name on PC match to COM port name “COM3”, or this could be changed, in SPO2.ipynb Python script.
This Firmware is develop using two libraries: “Virtual COM Port Demo” and “Heart rate click” form MIKROE libstock site.
## Measurement
![Measurement](/Pictures/Measurement.jpg)

Duration of measurement can be set in script in part 2. Appropriate connection of Hardware with PC must be done before starting script part 3. Before part 4 finger of observed person should be on sensor like in picture. Wait from starting, for time duration that is define in part 2, and remove finger on the end of part 4. Execute all parts of scripts to the end.
## Attention
This instrumentation is not calibrated.
