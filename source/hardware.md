# Hardware Description
The HiveWSN kit consists of 
1. a *brain* box contiaining the poser system, the microcontroller, the communication system and the connectivity to the sensors.
2. a set of sensors either commercially available or custom built at the [Department of Geosciences](https://www.mn.uio.no/geo/english/) at UiO as part of the [UiO Hive project](https://www.mn.uio.no/geo/english/research/projects/hive/).

**include a photo**

The kit is autonomous and packaged as a beam that can be installed on simple mast. The suite of sensors if customizable and depends on the puporse of the project. The main limitations in including new sensors are the communication protocol in between the microcontroller and the sensor, and the power management. 

Currently, there are two versions of the WSN system. These are based on the baord Wasmpote v15 which handle power, communication, and data brokerage. The firmware running all instances has been written as part of the project UiO Hive, and include a set of tools described in the software section.


## Sensors
The sensors used on teh stations are the following:

|Sensor name|Sensor type                    |I2C address|Arduino Library|
|-----------|-------------------------------|-----------|---------------|
|VL53L1     |Lidar                          |0x29       |[Sparkfun][vl53l1-sparkfun]|
|MLX90614 IR|Thermal IR                     |0x5A       |[Adafruit][mlx90614-adafruit] [Sparkfun][mlx90614-sparkfun]|
|VEML7700   |Ambient light                  |0x10       |[Adafruit][veml7700-adafruit]|
|ICM-20948  |Magnetometer, Acc, Gyro        |0x6B, 0x1E |[Adafruit][icm20948-adafruit]|
|AS7341     |Specrometer                    |0x39       |[Adafruit][as7341-adafruit]|
|VCNL-4040  |Proximity NIR sensor           |0x60       |[Sparkfun][vcnl4040-sparkfun]|
|BME280     |Temperature, humidity, pressure|0x77       |[Adafruit][bme280-adafruit] [Sparkfun][bme280-sparkfun]|
|TMP117     |Temperature                    |0x48       |[Adafruit][tmp117-adafruit] [Sparkfun][tmp117-sparkfun]|

[vl53l1-sparkfun]: https://learn.sparkfun.com/tutorials/qwiic-distance-sensor-vl53l1x-hookup-guide/arduino-library-overview
[mlx90614-adafruit]: https://learn.adafruit.com/using-melexis-mlx90614-non-contact-sensors/
[mlx90614-sparkfun]: https://learn.sparkfun.com/tutorials/mlx90614-ir-thermometer-hookup-guide#mlx90614-arduino-library
[veml7700-adafruit]: https://learn.adafruit.com/adafruit-veml7700/arduino
[icm20948-adafruit]: https://learn.adafruit.com/adafruit-tdk-invensense-icm-20948-9-dof-imu
[as7341-adafruit]: https://learn.adafruit.com/adafruit-as7341-10-channel-light-color-sensor-breakout/arduino
[bme280-adafruit]: https://learn.adafruit.com/adafruit-bme280-humidity-barometric-pressure-temperature-sensor-breakout/arduino-test
[bme280-sparkfun]: https://learn.sparkfun.com/tutorials/sparkfun-bme280-breakout-hookup-guide#i
[tmp117-adafruit]: https://learn.adafruit.com/adafruit-tmp117-high-accuracy-i2c-temperature-monitor
[tmp117-sparkfun]: https://learn.sparkfun.com/tutorials/qwiic-tmp117-high-precision-digital-temperature-sensor-hookup-guide
[vcnl4040-sparkfun]: https://learn.sparkfun.com/tutorials/qwiic-proximity-sensor-vcnl4040-hookup-guide


