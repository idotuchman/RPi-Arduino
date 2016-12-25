## GPIO Serial to Arduino
Based on [this link](http://spellfoundry.com/sleepy-pi/setting-arduino-ide-raspbian/)

### Turn off RPi's serial monitor  
`sudo raspi-config`, Advanced Settings --> Serial Monitor --> Off

### Set up GPIO pins
If using a 5V Arduino, use a level shifter or voltage divider on RXD pin  
GPIO 14: TXD  
GPIO 15: RXD  
GPIO 22: Reset

### Link the Serial port to GPIO
In `/etc/udev/rules.d/`, create `80-pi-arduino.rules` file with the following:
```
KERNEL=="ttyAMA0", SYMLINK+="ttyS0",GROUP="dialout",MODE:=0666
KERNEL=="ttyACM0", SYMLINK+="ttyS1",GROUP="dialout",MODE:=0666
```
