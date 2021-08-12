# Hardware Description
The HiveWSN kit consists of 
1. a *brain* box containing the powser system, the microcontroller, the communication system and the connectivity to the sensors.
2. a set of sensors either commercially available or custom built at the [Department of Geosciences](https://www.mn.uio.no/geo/english/) at UiO as part of the [UiO Hive project](https://www.mn.uio.no/geo/english/research/projects/hive/).

[include a photo]

The kit is autonomous and packaged as a beam that can be installed on simple mast. The suite of sensors if customizable and depends on the puporse of the project. The main limitations in including new sensors are the communication protocol in between the microcontroller and the sensor, and the power management. 

Currently, there are two versions of the WSN system: v1 from 2019, and v2 from 2021. Both are based on the board Wasmpote v15 which handle power, communication, and data brokerage. The firmware running all instances has been written as part of the project UiO Hive, and include a set of tools described in the software section.

## Version 1, 2019
Version 1 is the first formalized version of the Hive system. It includes a range of solution in terms of sensors, communication protocol, and embedded resilience system. 

[include photo]

## Version 2, 2021
Version 2 is an upgraded version which includes a number of improvements like new sensors, larger solar panel and enclosure, an added microcontroller to control sensors only. This version was made compatible with the Lora radio network solution, with its own libraries to perform tree topology with Lora radios. 

[include photo]

## Sensors
The sensors used on the stations are the following:

|Sensor name|Sensor type                    |Version|Datasheet|
|-----------|-------------------------------|----|-----------|
|VL53L1     |Lidar                          |v1, v2|[Datasheet][vl53l1-sheet]|
|MLX90614 IR|Thermal IR                     |v1, v2|[Datasheet][mlx90614-sheet]|
|VEML7700   |Ambient light                  |v2|[Datasheet][veml7700-sheet]|
|AS7341     |Spectrometer                    |v2|[Datasheet][as7341-sheet]|
|VCNL-4040  |Proximity NIR sensor           |v2|[Datasheet][vcnl4040-sheet]|
|BME280     |Temperature, humidity, pressure|v1, v2|[Datasheet][bme280-sheet]|
|TMP117     |Temperature                    |v2|[Datasheet][tmp117-sheet]|
|TMP102     |Temperature                   |v1|[Datasheet][tmp102-sheet]|
|SHT31	|Temperature, humidity |v2|[Datasheet][sht31-sheet]|
|ATMOS 22|Wind, temperature|v1, v2| [Datasheet][atmos22-sheet]|
|CTD 10|Water temperature, pressure, conductivity|v1, v2| [Datasheet][ctd10-sheet]|
|DS18B20|Temperature|v1, v2| [Datasheet][ds18b20-sheet]|
|MB7389|Temperature|v1, v2| [Datasheet][MB7289-sheet]|

[vl53l1-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/veml7700.pdf
[mlx90614-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/MLX90614-Datasheet-Melexis.pdf
[veml7700-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/veml7700.pdf
[as7341-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/AS7341_DS.pdf
[vcnl4040-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/vcnl4040.pdf
[bme280-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/bst-bme280-ds002.pdf
[tmp117-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/tmp117.pdf
[tmp102-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/tmp102.pdf
[sht31-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/sht31_datasheet.pdf
[atmos22-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/ATMOS%2022.pdf
[ds2-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/DS2_Web.pdf
[ctd10-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/CTD-10.pdf
[ds18b20-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/DS18B20.pdf
[MB7289-sheet]:https://github.com/UiOHive/Hive-Wireless-Sensor-Network/blob/main/attachments/HRXL-MaxSonar-WR_Datasheet.pdf

All sensors use digital comminucation protocols such as [I2C](https://en.wikipedia.org/wiki/I%C2%B2C), [SDI-12](https://en.wikipedia.org/wiki/SDI-12), or [One-Wire](https://en.wikipedia.org/wiki/1-Wire).

Sampling can be set to any time intervals, though in most cases all sensors are sampled every 10 minutes as a trade of for temporal granularity and power saving. All data is associated to its ampling time.