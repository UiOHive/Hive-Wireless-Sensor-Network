# Hardware Description
The HiveWSN kit consists of 
1. a *brain* box contiaining the poser system, the microcontroller, the communication system and the connectivity to the sensors.
2. a set of sensors either commercially available or custom built at the [Department of Geosciences](https://www.mn.uio.no/geo/english/) at UiO as part of the [UiO Hive project](https://www.mn.uio.no/geo/english/research/projects/hive/).

[include a photo]

The kit is autonomous and packaged as a beam that can be installed on simple mast. The suite of sensors if customizable and depends on the puporse of the project. The main limitations in including new sensors are the communication protocol in between the microcontroller and the sensor, and the power management. 

Currently, there are two versions of the WSN system: v1 from 2019, and v2 from 2021. Both are based on the board Wasmpote v15 which handle power, communication, and data brokerage. The firmware running all instances has been written as part of the project UiO Hive, and include a set of tools described in the software section.

## Version 1, 2019

## Version 2, 2021

## Sensors

The sensors used on the stations are the following:

|Sensor name|Sensor type                    |Version|Datasheet|
|-----------|-------------------------------|----|-----------|
|VL53L1     |Lidar                          |v1, v2|[Datasheet][vl53l1-sheet]|
|MLX90614 IR|Thermal IR                     |v1, v2|[Datasheet][mlx90614-sheet]|
|VEML7700   |Ambient light                  |v2|[Datasheet][veml7700-sheet]|
|AS7341     |Specrometer                    |v2|[Datasheet][as7341-sheet]|
|VCNL-4040  |Proximity NIR sensor           |v2|[Datasheet][vcnl4040-sheet]|
|BME280     |Temperature, humidity, pressure|v1, v2|[Datasheet][bme280-sheet]|
|TMP117     |Temperature                    |v2|[Datasheet][tmp117-sheet]|
|TMP102     |Temperature                   |v1|[Datasheet][tmp102-sheet]|
|SHT31	|Temperature, humidity |v2|[Datasheet][sht31-sheet]|
|ATMOS 22|Wind, temperature|v1, v2| [Datasheet][atmos22-sheet]|
|CTD 10|Water temperature, pressure, conductivity|v1, v2| [Datasheet][ctd10-sheet]|
|DS18B20|Temperature|v1, v2| [Datasheet][ds18b20-sheet]|
|Maxbotix|Temperature|v1, v2| [Datasheet][ds18b20-sheet]|

[vl53l1-sheet]:/attachments/vl53l1x.pdf
[mlx90614-sheet]:file:./attachments/MLX90614-Datasheet-Melexis.pdf
[veml7700-sheet]:file:./attachments/veml7700.pdf
[as7341-sheet]:file:./attachments/AS7341_DS.pdf
[vcnl4040-sheet]:file:./attachments/vcnl4040.pdf
[bme280-sheet]::file:./attachments/bst-bme280-ds002.pdf
[tmp117-sheet]:file:./attachments/tmp117.pdf
[tmp102-sheet]:
[sht31-sheet]:
[atmos22-sheet]:
[ds2-sheet]:
[ctd10-sheet]:
[ds18b20-sheet]:

