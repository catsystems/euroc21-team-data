You can find the data of the CATS flight computer here.

The plotted data can be found in the .html file.

The raw data is in the .log file and needs to be parsed correctly. One can do so by running the jupyter notebook "vs_log_parser.ipynb" in https://github.com/catsystems/cats-logs/tree/main/log_parsing. Then the data is saved locally in csv files. 

The csv files are also available in this folder.

The CATS board records 3 Barometers (ms5067), 2 IMU's (ICM20601), 1 Magneto (mmc5983ma) and one high-G accelerometer (h3lis100dl), all of them with 100 Hz.

There is also the state estimation data (height, velocity), the filtered barometer data (median filtered over 9 samples) and an experimental orientation filter which unfortunately broke down after 1.3 seconds, all of them also sampled with 100 Hz.

Events are also recorded, for example Thrusting, Coasting, Apogee etc.

The rocket flew nominally for 1.3 seconds and after that the motor failed due to a faulty O-ring. The CATS flight computer was programmed with a machtimer of 20 seconds (as we expected nominal flight) and hence, the apogee was delayed by 20 seconds. Without a machtimer the CATS would have detected apogee at 3.3 seconds (30 samples after the velocity hits zero). The FC was placed in the main body.

Flight Statistics:

Max height: 170 m

Max velocity: 80 m/s

Motor thrust: 8 g's
