You can find the data of the CATS flight computer here.

The plotted data can be found in the .html file.

The csv files of all sensors and flight data is available in this folder.

The CATS board records 3 Barometers (ms5067) and 3 IMU's (ICM20601), all of them with 100 Hz.

The barometer readings are in pascals, the temperature in °C, the linear acceleration in m/s^2, the gyro in dps. The state estimation height is in m and the velocity in m/s.

There is also the state estimation data (height, velocity) and the filtered barometer data (median filtered over 9 samples)all of them also sampled with 100 Hz.

Events are also recorded, for example Thrusting, Coasting, Apogee etc.

The rocket flew nominally until apogee where the CATS FC as well as the backup Altrus Mega both triggered the apogee event. Due to an unknown issue, the parachute was not triggered. After 30 more seconds of flight the rocket broke into pieces, cutting off the power to the CATS FC. At the end one can see huge vibrations, probably from the main body. The FC was placed in the main body.

Disclaimer: The state estimation from the CATS FC is not up to date. The software used is 5 month's old, so is the state estimation. The current estimation is a lot less fragile to. Additionally, the barometric pressure model was not implemented incorrectly, yielding an apogee of 7500 m this. Consequently, the velocity is also overestimated by quite a bit. Hence, the plots of the state estimation for this flight should be ignored/not be used to make any conclusions.

Flight Statistics:

```
Max height: 6200 m
Max velocity: 340 m/s
```
