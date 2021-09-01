## Description
The aim of this part is to make nrf52840 generate a square wave as an enable signal, and send it to the sensor.
After that, I apply the saadc function to sample the measurement signals that come from the sensor. 
However ,there are some limitations on the square wave : 
* pulsewidth    0.8ms - 1.2ms
* peak voltage  0.5V  - 4.5V

Unfortunately, nrf52840 doesn't have the hardware DAC,and it causes difficulties in providing the square wave with different voltage peak value.
To solve this problem, mcp4725 module, an I2C controlled Digital-to-Analog converter, is appiled.
Finally, we could control the pulse within the limitations via third party software Putty. 

## Techniques in use
* DAC
* ADC 
* UART
* I2C

