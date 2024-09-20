# Notes on Raspberry Pi Pico

* [Pinout](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf)
  * Pinout guide: https://deepbluembedded.com/raspberry-pi-pico-w-pinout-diagram-gpio-guide/
* [RPi Pico Arduino IDE Library Docs](https://arduino-pico.readthedocs.io/en/latest/)
  * [PIO functionality](https://arduino-pico.readthedocs.io/en/latest/piouart.html) 
  * [FreeRTOS](https://arduino-pico.readthedocs.io/en/latest/freertos.html)
  * [Multicore](https://arduino-pico.readthedocs.io/en/latest/multicore.html)
  * [SD](https://arduino-pico.readthedocs.io/en/latest/fs.html)
* Unlike 8-bit Arduino, Serial port should be opened at 115200 bps instead of 9600 bps.
* “Serial” is stated with numbers such as “Serial1” because multiple ones exist.
* Pins 1 (GP0) and 2 (GP1) are used for communication so don’t connect components to those ports unless its a communication component as it messes up serial port.
* Powering the pico from VBUS is not recommended. Use VSYS instead. Check https://penguintutor.com/electronics/pico-power
* ADC pins are noisy. Its only important for Pitot Tube air pressure sensor.
* Do not connect +3.3V to AGND. Do not use it.
* Drive servo using PIO functionality: https://www.hackster.io/naveenbskumar/raspberry-pi-pico-drive-servo-using-pio-d7a0e7
