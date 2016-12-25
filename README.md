## GPIO Serial to Arduino
Heavily based on [this link](http://spellfoundry.com/sleepy-pi/setting-arduino-ide-raspbian/)

### Turn off RPi's serial monitor  
'sudo raspi-config', Advanced Settings --> Serial Monitor --> Off

### Set up GPIO pins
If using a 5V Arduino, use a level shifter or voltage divider on RXD pin  
GPIO 14: TXD  
GPIO 15: RXD  
GPIO 22: Reset
