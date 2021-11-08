# Install i2c-tools
1. Run the following commands in terminal
```
sudo apt-get install python-smbus
```
```
sudo apt-get install i2c-tools
```
2. Make sure enable the I2C interface in Jetson Nano
3. Reboot Jetson Nano
```
sudo reboot
```
# Connection of sensor(using bus1)
1. Vcc connects to 3.3V
2. GND onnects to GND
3. TX connects to pin3
4. RX connects to pin5  
# Check the connection of sensor
```
sudo i2cdetect -y -r -a 1
```
Here, 1 represents the I2C-bus1 (pin3 for SDA and pin5 for SCL). 0 represents I2C-bus 0 (pin27 for SDA and pin28 for SCL)
Default address of tempearture sensor is 0x66
# Usage of Sensor
```
python3 i2c.py
```
Note: only python3 can be used, python2 will cause the error of "No module of board"
