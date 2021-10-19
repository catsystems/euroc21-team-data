# Lynx Flight Data (Euroc 2021)

## Logs from SRAD avionics ("Death Stack")

| File | Description |
| ----------- | ----------- |
| imu_accel_gyro.csv | BMX160 Accelerometer and Gyroscope (1600 Hz) |
| imu_compass.csv | BMX160 Magnetometer (100 Hz) |
| imu_temperature.csv | BMX160 Thermometer |
| pressure_ms5803.csv | MS5803 Digital Barometer (66.6 Hz) |
| pressure_static_port.csv | MPXHZ6130A analog Pressure sensor (connected to a static pressure port)  (42 Hz) |
| pressure_deployment_bay.csv | SSCDANN030PAA analog pressure sensor measuring pressure inside the deployment bay (42 Hz) |
| pitot.csv | Pressure and airspeed data from the SSCDRRN015PDA differential pressure sensor, connected to the pitot tube (42 Hz) |
| battery.csv | 3S LiPo voltage |
| apogeedetectionfilter.csv | Data from the Kalman filter used for apogee detection |
| statemachine.csv | Main computer state machine (9=Armed, 10=Ascent, 11=Drogue deployed, 12=Main chute deployed|
